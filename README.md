# Задание 1
На лекции рассматривались режимы репликации master-slave, master-master, опишите их различия.
master-slave есть основной сервер, остальные копии (slave) которые считывают обновления с мастера и вносят себе изменения. Это полезно если нужно распараллелить нагрузку при этом приложения работают на чтения с slave (много), а запись только в master (мало)
maste-master все тоже самое только каждый узел становится еще мастером для последующего. Такой конфиг удачен для зональных серверов которые обслуживают определенную локацию и в каждом такой зоне работает master. При DRP (Disaster Recovery Plan) будет переключен на master других зон.
Задание 2
Выполните конфигурацию master-slave репликации, примером можно пользоваться из лекции.

Приложите скриншоты конфигурации, выполнения работы: состояния и режимы работы серверов.
<img width="834" height="534" alt="image" src="https://github.com/user-attachments/assets/ccf1269f-edd0-46db-9c4a-4e1021ee7ccb" />
<img width="646" height="583" alt="image" src="https://github.com/user-attachments/assets/308cc0ed-bc8a-40e4-a757-8abf3a5192cb" />

используем эти команды: <img width="576" height="315" alt="image" src="https://github.com/user-attachments/assets/6f42e31b-885a-4662-9f27-5e2d27c50059" />
соотвественно после 2 скриншота результат таков:
<img width="199" height="154" alt="image" src="https://github.com/user-attachments/assets/0c4a2a1b-c8d5-4728-ad8e-32b6a9c6bd31" />
