# okd

Platform: Fedora CoreOS

Download `wget`:
```bash
sudo rpm-ostree install wget
sudo systemctl reboot
```

Download OKD
```bash
OKD_VERSION=4.15.0-0.okd-2024-03-10-010116
wget https://github.com/okd-project/okd/releases/download/${OKD_VERSION}/openshift-client-linux-${OKD_VERSION}.tar.gz
wget https://github.com/okd-project/okd/releases/download/${OKD_VERSION}/openshift-install-linux-${OKD_VERSION}.tar.gz
```

Extract files:
```bash
tar -xvzf openshift-client-linux-${OKD_VERSION}.tar.gz
tar -xvzf openshift-install-linux-${OKD_VERSION}.tar.gz
```

Move the binaries to executable path:
```bash
sudo mv kubectl oc openshift-install /usr/local/bin/
```

Create new cluster:
```bash
openshift-install create cluster
```
