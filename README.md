# available_cluster_ansible
## Функционал
Данный плейбук разворачивает высоко доступный балансировщик нагрузки с плавающим ip адресом
## Используемый стек
Ansible
Docker
Nginx
Haproxy
Keepalived
### Для запуска (Linux)
```
apt install python3-venv git
```
```
python3 -m venv venv
```
```
cd venv
```
```
source ./bin/activate
```
```
echo "net.ipv4.ip_nonlocal_bind=1" >> /etc/sysctl.conf
```
```
sysctl -p
```
```
pip install ansible
```
```
ansible-galaxy collection install community.docker
```
```
git clone https://github.com/viktorisup/available_cluster_ansible.git
```
```
cd available_cluster_ansible
```
```
ansible-playbook -i ./inventory/hosts.yaml blaybook.yaml
```
### для установки локально раскоментируйте строчки в playbook.yaml и в hosts.yaml и закоментируйте group1 в hosts.yaml
### Кластер станет доступен по адресу 10.0.0.200

