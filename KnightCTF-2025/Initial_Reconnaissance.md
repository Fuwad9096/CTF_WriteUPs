
## Initial Reconnaissance

Find the basic web enumeration tool that is used by the attacker.


## Steps

**1.** Filter out the attacker's ip which is `192.168.1.9` and the `http` requets in `Wireshark`. Use the following display filter.

```bash
ip.addr == 192.168.1.9 && http
```

**2.** Find the name of the common web enumeration tools like `Nmap`, `Nikto`. Use `CTRL+F` to open the find tab.

**3.** We will be able to see a tool name in one of the `http` request like the one below:



**4.** We find that the tool `Nikto` has been used by the attacker. So, the flag is:

```bash
KCTF{nikto}
```




