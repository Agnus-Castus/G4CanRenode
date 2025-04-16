# Test mit Can on  G4 

## Zephier Setup
Create .venv

```
python3 -m venv .venv
```

activate venv

```
source .venv/bin/activate
```

```
pip install west
```

```
west sdk install
```

Build my App:
```west build -b nucleo_g474re app/can/isotp/ ```


Build Blinky:
```west build -b nucleo_g474re zephyr/samples/basic/blinky ```

## Renode Setup


Install renode portable see theire github


To start renode run from prject root start

blinky.resc runs the blinky.example from zephyr: whit localy build elf
``` ~/renode_portable/renode renode/blinky.resc```



This commands runs the hello world example with elf hosted by renode 

```~/renode_portable/renode renode/hello_world.resc```

Attenation dont forget to start the emulation 
type ```start``` in the renode terminal

## Debuging

You need the gdb multiarch package

```sudo apt install gdb-multiarch```

## Example build comandas

Build iso-tp sample with nucleo stm32G474re in dedicated build folder:

``` west build --pristine --board nucleo_g474re zephyr/samples/subsys/canbus/isotp -d build-can-isotp```

Build iso-tp sample with nucleo stm32h743 in dedicated build folder:

```west build --pristine --board nucleo_h743zi zephyr/samples/subsys/canbus/isotp -d build-can-isotp-h7```