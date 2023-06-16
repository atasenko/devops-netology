### Задача 1.  
![Proof](img/ubuntu_image.png)  

### Задача 2.  
Создавать машину с помощью web-интерфейса не интересно, пропустил этот этап.  
[apply_out](Terraform/apply_out.txt)
![YC proof](img/terraform_vm.png)

### Задача 3.  
Создаем директорию:  
sudo mkdir /data  
Запуск контейнера CentOS (используем полный путь /data, иначе docker создаст volume в дебрях своих служебных директорий):  
sudo docker run --name centos -d -t -v /data:/data centos  
Создаем текстовый файл внутри CentOS:  
sudo docker exec -it centos bash  
vi /data/createdfromCentOS  
exit  
Добавляем еще один файл с хоста:  
sudo vi /data/createdfromHost  
Запуск контейнера debian и подключение к нему по тому же принципу:  
sudo docker run --name debian -d -t -v /data:/data debian  
sudo docker exec -it debian bash  
Или просто:  
sudo docker exec -it debian ls -l /data  
sudo docker exec -it debian cat /data/createdfromCentOS  
sudo docker exec -it debian cat /data/createdfromHost  


