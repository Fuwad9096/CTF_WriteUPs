
## The Real Admin

Find the real admin's ip address

## Steps

**1.** Use the following display filter to exclude packets with the IP address `192.168.1.9` and focus on `http` packets:

```bash
!(ip.addr == 192.168.1.9) && http
```

**2.** Press `CTRL + F` to open the search bar and type the keyword `admin` in the search bar.

**3.** This process will filter out HTTP packets that do not belong to `192.168.1.9`. Searching for **admin** will highlight packets containing the string `admin`. If `192.168.1.3` appears in the packet data, it is likely the actual ip address of the admin.

**4.** The flag is:

```bash
KCTF{192.168.1.3}
```




