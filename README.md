# deploy-envoy-proxy

## Step

1. create file deploy-envoy.yml
```
- hosts: envoy
  become: yes
  roles:
    - deploy-envoy-proxy
```
2. create file inventory
```
[envoy]
192.168.0.5

[all:vars]
ansible_user=user
ansible_become_pass=password
```

2. mkdir roles
3. cd roles
4. git clone https://github.com/doko89/deploy-envoy-proxy.git
5. cd ..
6. ansible-playbook -i inventory deploy-envoy.yml
