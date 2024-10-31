# magma-deployer
Quick deployer of the Magma Orchestrator based mostly on ansible.

Docs: https://magma.github.io/magma/docs/next/orc8r/deploy_using_ansible

Quick Install:
```bash
sudo bash -c "$(curl -sL https://github.com/magma/magma-deployer/raw/main/deploy-orc8r.sh)"
```

CMU Controlled Install:
```bash
git clone https://github.com/jblakley/magma-deployer
cd magma-deployer
git checkout cmu
bash ./deploy-orc8r.sh
```



Switch to `magma` user after deployment has finsished:
```bash
sudo su - magma
```

Once all pods are ready, setup NMS login:
```bash
cd ~/magma-deployer
ansible-playbook config-orc8r.yml
```

You can get your `rootCA.pem` file from the following location:
```bash
cat ~/magma-deployer/secrets/rootCA.pem
```
