**# For setup elastic stack in you environment:**
Install Ansible
Add your public ip and private ip cd /elk/vars/main.yml
then  run ansible-playbook elk.yml
then go to https://{public ip}:5601/
/usr/share/elasticsearch/bin/elasticsearch-create-enrollment-token -s kibana
/usr/share/kibana/bin/kibana-verification-code
/usr/share/elasticsearch/bin/elasticsearch-reset-password -i -u elastic
after login Go to fleet > Add a fleet server > give a name  > In url https://{private ip}:8220
After Sucessful adding the fleet agent you can start adding other agents to different environments.
