# add board config to vivado
## download config file
```shell
wget https://github.com/Digilent/vivado-boards/archive/master.zip
```

## unzip this file
```shell
unzip master.zip 
```

## install config file
```shell
cp -rf  vivado-boards-master/new/board_files/ <your vivado installed path>/Vivado/2018.2/data/boards/
```
