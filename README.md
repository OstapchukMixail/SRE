## Подключение
ssh -i ~/.ssh/id_sre_learn -p 29022 muostapchuk@176.109.82.213

## Запуск команды
ansible-playbook -i inventory deploy_pgcluster.yml

## Запуск helm

helm upgrade --install api-chart api-chart --kubeconfig ./student_8.yaml -f ./api-chart/custom_values.yaml 

## Заходим и проверяем postgres
ssh -i ~/.ssh/id_sre_learn -p 29023 muostapchuk@176.109.82.213

sudo su postgres

pg_lsclusters

## Миграции
заходим на под и в папке миграции init.sql
(ее надо накатить)

## Swagger
Добавляем в /etc/hosts 176.109.82.213   muostapchuk
Теперь открываем в браузере https://muostapchuk/swagger/index.html
