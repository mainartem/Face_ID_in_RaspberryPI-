# Face_ID_in_RaspberryPI
Система распознавания лиц для raspberry pi 

## Системные требования
* Raspberry pi 3B+ (или старшие модели) или компьютер под управлением windows
* Python version 3.10 **Обязательно!!!**
* Установленный git 
> *Обратите внимание, что на Windows сервер правильно установится только на версии python 3.10*
## Установка на компьютер под управлением Windows (server.py) и установка клиента на том же компьютер (client.py)
### установка
1. Скопировать репозиторий
`git clone https://github.com/mainartem/Face_ID_in_RaspberryPI-.git`
2. Создать виртуальное окружение
```
cd Face_ID_in_RaspberryPI-
python -m venv face-id-venv
```
3. Установить библиотеки
```
face-id-venv\Scripts\activate.bat
pip install dlib-19.24.2-cp310-cp310-win_amd64.whl
pip install -r requirements.txt
```
### запуск

#### создание базы данных

1. Запустить скрипт для добавления лица в базу данных
```
python write.py
```
2. Дождаться запуска интерфейса
3. Когда ваше лицо будет рамке, нажмите клавишу пробел
4. Запишите в консоле ваше имя

#### сервер

```
python server.py
```

#### клиент

```
python client.py
```

### Установка на сервер под управлением Raspberry Pi OS (server.py) и установка клиента на компьютре под управлением Windows
## server
1. Скопировать репозиторий
`git clone https://github.com/mainartem/Face_ID_in_RaspberryPI-.git`
2. Создать виртуальное окружение
```
cd Face_ID_in_RaspberryPI-
python -m venv face-id-venv
```
3. Установить библиотеки
```
source face-id-venv/bin/activate
pip install -r requirements.txt
```
4. Изменить IP адрес устройство в сети в файле server.py в строке 28
`socket_address = ("IP_Adress", port)`
## client 
1. Скопировать репозиторий
`git clone https://github.com/mainartem/Face_ID_in_RaspberryPI-.git`
2. Создать виртуальное окружение
```
cd Face_ID_in_RaspberryPI-
python -m venv face-id-venv
```
3. Установить библиотеки
```
pip install python-opencv
```

