# Corne v3 — QMK на Pro Micro RP2040

QMK-прошивка для Corne (`crkbd/rev1`) на проводном контроллере
SparkFun Pro Micro RP2040 (и совместимых: Adafruit KB2040, Blok, Bit-C PRO и др.),
собранная через фичу [Converters](https://docs.qmk.fm/feature_converters):
`CONVERT_TO=sparkfun_pm2040` на базе штатной раскладки Pro Micro (`promicro`).

Это [QMK Userspace](https://docs.qmk.fm/newbs_external_userspace) — отдельный
шаблон-репозиторий, устроенный иначе, чем ZMK-конфиг на ветке `main`
(там свой build.yaml/west.yml под ZMK). При пуше GitHub Actions скачивает
`qmk/qmk_firmware`, собирает прошивку и публикует `.uf2` в Releases.

Локальная сборка:

```sh
qmk config user.qmk_home=<путь до qmk_firmware>
qmk userspace-compile
```
