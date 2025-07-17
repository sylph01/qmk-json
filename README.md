# qmk-json

## procedures

### setup qmk

on home directory, clone forked version (that has changes to TAPPING_TERMs of certain keyboards):

```
git clone git@github.com:sylph01/qmk_firmware.git
cd qmk_firmware
git checkout sylph01
```

then install qmk

- https://docs.qmk.fm/newbs_getting_started
- https://docs.astral.sh/uv/
  - uses `uv` because the normal procedure gives a `externally-managed-environment` error

```
cd
sudo apt install -y git python3-pip
curl -LsSf https://astral.sh/uv/install.sh | sh
qmk setup
```

### compile

```
qmk compile iris/iris-rev6-sylph01.json
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