## Setup Zephyr Env

```
pip install west

west init -m https://github.com/ck-telecom/lcd-demo.git lcd_demo_workspace

cd lcd_demo_workspace

west update
west zephyr-export
west packages pip --install
west sdk install -t arm-zephyr-eabi
 ```
see more via https://docs.zephyrproject.org/latest/develop/getting_started/index.html

## Build with west
```
cd lcd_demo_workspace/app # make sure in this directory

west build -b sf32lb58_devkit_lcd .
```

## Flash
```
west flash or

west flash --port=<your serial port> (COM5 eg.)
```
