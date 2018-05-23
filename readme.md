This script from https://doub.io/vpnzy-7/

Installation:

```
wget https://github.com/ky0ncheng/one-key-ocserv/raw/master/ocserv.sh && chmod +x ocserv.sh && ./ocserv.sh
```

SSL certificate by letsencrypt with [acme.sh](https://acme.sh)

```
export CF_Key="CF_API_KEY"
export CF_Email="yourmail@mail.com"

curl https://get.acme.sh | sh

~/.acme/acme.sh --issue --dns dns_cf -d yourdomain.xyz -d yoursubdomain.yourdomain.xyz --keylength ec-384

cp youdomain.key /etc/ocserv/ssl/server-key.pem
cp fullchain.cer /etc/ocserv/ssl/server-cert.pem
```

Restart ocserv and enjoy~

More function you can `./ocserv.sh` to use.

