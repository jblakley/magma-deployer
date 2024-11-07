# Multipass Setup

Start multipass if it's not running:
```bash
sudo snap restart multipass.multipassd
```

Start a new multipass instance with the following command:
```bash
multipass launch jammy \
  --name orc8r \
  --disk 100G \
  --memory 8G \
  --cpus 4
```

Check if instance has started:
```bash
multipass ls
```

Get access to the shell:
```bash
multipass shell orc8r
```

Add your public SSH key to the instance:
```bash
vim .ssh/authorized_keys
```

### Uninstall

Delete Instance
```bash
multipass delete --purge orc8r
```
