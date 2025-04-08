# Test mit Can on  G4 

## Build Samples
Create .venv
```python3 -m venv .venv```

activate venv
```source .venv/bin/activate```

Build my App:
```west build -b nucleo_g474re app/can/isotp/ ```


Build Blinky:
```west build -b nucleo_g474re zephyr/samples/basic/blinky ```

