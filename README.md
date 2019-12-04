# Auto-healing networks

This is a Stackstorm pack to demonstrate how a network can recover from router interface
failure.

#### Prerequisites
1. Stackstorm
2. Ansible pack for Stackstorm
3. StackStorm ChatOps integration with Slack

#### Installing

```
cd /opt/stackstorm/packs/
git clone git@github.com:solidex/auto-healing-networks.git
mv auto-healing-networks automation_lab
st2 action create actions/repair_intf.yaml
```

#### Run
```
st2 run automation_lab.repair_interface intf_name="ge-0/0/2" device="vmx-141"
```
