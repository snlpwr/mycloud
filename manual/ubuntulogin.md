# Set ubuntu server cloud image user password

Launch an instance and in post creation insert following script

```
#cloud-config
password: ubuntu
chpasswd: { expire: False }
ssh_pwauth: True
```
