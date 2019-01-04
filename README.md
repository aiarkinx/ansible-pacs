#Создание образа, исходники - https://github.com/Iarkin/conquest-docker
ansible-playbook -i inventories/hosts pacs.yml --tags "imagebuild"

#Первый запуск, персбор базы
ansible-playbook -i inventories/hosts pacs.yml --tags "rebuilddb"

#Старт контейнеров
ansible-playbook -i inventories/hosts pacs.yml --tags "start"
