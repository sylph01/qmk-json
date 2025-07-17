# qmk-json

## procedures

### setup qmk

- https://docs.qmk.fm/newbs_getting_started
- https://docs.astral.sh/uv/
  - uses `uv` because the normal procedure gives a `externally-managed-environment` error

```
cd
sudo apt install -y git python3-pip
curl -LsSf https://astral.sh/uv/install.sh | sh
qmk setup
```

### copy user-specific config

copy `users/sylph01` under `qmk_firmware`. this includes info on tapping term

### compile

```
qmk compile -c iris/iris-rev6-sylph01.json
```

### flash

```
qmk flash keebio_iris_rev6_sylph01.hex
```

## troubleshooting

### errors relating to HENK/MHEN

https://docs.qmk.fm/keycodes_basic

`KC_HENK` -> `KC_INT4`
`KC_MHEN` -> `KC_INT5`