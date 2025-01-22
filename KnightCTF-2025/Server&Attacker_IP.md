
## Server & Attacker IP

Find the ip of the `server` and the `attacker`


## Steps

**1.** Filter out the `http` requests

**2.** We see the `http` requests as follows:

![Server_Attacker](https://github.com/user-attachments/assets/c919989e-d34d-46df-b5e8-8995d97d457f)


**3.** We see that the `source` and `destination` ip where the `http` requests are sent and recieved.

```bash
source ip: 192.168.1.9
destination ip: 192.168.1.10
```

**4.** Here, we can see that, the `source` is the `attacker` and the `destination` is the `server`. So, the flag is:

```bash
KCTF{192.168.1.10_192.168.1.9}
```




