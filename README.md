#Installing and running RabbitMQ  
1. Install RabbitMQ

2. Enable management plugin to be ble to use admin UI  
   ```rabbitmq-plugins enable rabbitmq_management```  

3. Start RabbitMQ server with default node name (which is 'rabbit')  
   ```rabbitmq-server``` 

4. Alternatively, start RabbitMQ in the background  
   ```rabbitmq-server -detached```  

5. Add user with password  
   ```rabbitmqctl add_user gravity-cbs Infy123++```  

6. Add a virtual host named gravityvhost  
   ```rabbitmqctl add_vhost gravityvhost```  

7. Grant the user named gravity-cbs access to the virtual host called gravityvhost, with configure permissions on all resources whose names starts with "gravity-", and write and read permissions on all resources  
   ```rabbitmqctl set_permissions -p gravityvhost gravity-cbs "^gravity-.*" ".*" ".*"```  
