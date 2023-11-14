# Setting up Elastic Stack in Your Environment

1. Install Ansible.
2. Add your public IP and private IP in `/elk/vars/main.yml`.
3. Run the following command:
    ```bash
    ansible-playbook elk.yml
    ```

4. Access Kibana at [https://{public ip}:5601/](https://{public ip}:5601/).

5. Generate enrollment token for Kibana:
    ```bash
    /usr/share/elasticsearch/bin/elasticsearch-create-enrollment-token -s kibana
    ```

6. Obtain the Kibana verification code:
    ```bash
    /usr/share/kibana/bin/kibana-verification-code
    ```

7. Reset the Elasticsearch password:
    ```bash
    /usr/share/elasticsearch/bin/elasticsearch-reset-password -i -u elastic
    ```

8. Log in to Kibana, go to Fleet, and add a fleet server with the following URL: [https://{private ip}:8220](https://{private ip}:8220).

9. After successfully adding the fleet agent, you can start adding other agents to different environments.

