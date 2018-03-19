# coreos-swapfile-vagrant-demo
Test CoreOS VM environment for coreos-swapfile

It is assumed that you already have the following installed on your machine:
- vagrant
- virtualbox

To clone:
```bash
git clone --recurse-submodules git@github.com:stackhpc/coreos-swapfile-vagrant.git
```

After cloning,
```python
python -m venv venv
. venv/bin/activate
pip install -r requirements.txt
```

Then,
```bash
vagrant up --provision
```

To ensure that the swap space has been provisioned,
```bash
vagrant ssh
top
```

To cleanup,
```bash
vagrant destroy -f
```
