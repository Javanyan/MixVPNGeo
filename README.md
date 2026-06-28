<div align="center">

# 🚀 MixVPN Geo Routing

**Готовые конфигурации маршрутизации для [Happ](https://happ.su), [INCY](https://incy.cc) и [Mihomo](https://github.com/MetaCubeX/mihomo) (Clash Meta и др.)**

> Умный роутинг для 🇷🇺 России и 🇧🇾 Беларуси: RU-сервисы и банки идут напрямую (видят твой реальный IP), заблокированное — через VPN, реклама и слежка — режутся.

![Happ](https://img.shields.io/badge/Happ-blue.svg)
![Mihomo](https://img.shields.io/badge/Mihomo-grey.svg)
![Incy](https://img.shields.io/badge/Incy-darkgreen.svg)

**Поддержка и подписка → [@vpn_mix_bot](https://t.me/vpn_mix_bot) · 99₽/мес**

</div>

---

## 📱 Установка для Happ

| Профиль | Что делает | Ссылки |
|---|---|---|
| **DEFAULT** | RU/BY direct, YouTube/Telegram/GitHub через прокси, реклама блокируется | [DEEPLINK](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/HAPP/DEFAULT.DEEPLINK) · [JSON](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/HAPP/DEFAULT.JSON) |
| **WHITELIST** | direct только для RU/BY whitelist, всё остальное через прокси | [DEEPLINK](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/HAPP/WHITELIST.DEEPLINK) · [JSON](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/HAPP/WHITELIST.JSON) |
| **JSONSUB** | минимальный профиль: только DNS + кастомные geo, без встроенных правил | [DEEPLINK](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/HAPP/JSONSUB.DEEPLINK) · [JSON](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/HAPP/JSONSUB.JSON) |

## 📱 Установка для INCY

| Профиль | Ссылки |
|---|---|
| **DEFAULT** | [DEEPLINK](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/INCY/DEFAULT.DEEPLINK) · [JSON](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/INCY/DEFAULT.JSON) |
| **WHITELIST** | [DEEPLINK](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/INCY/WHITELIST.DEEPLINK) · [JSON](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/INCY/WHITELIST.JSON) |
| **JSONSUB** | [DEEPLINK](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/INCY/JSONSUB.DEEPLINK) · [JSON](https://raw.githubusercontent.com/Javanyan/MixVPNGeo/main/INCY/JSONSUB.JSON) |

## 💻 Mihomo (Clash Meta)

В папке `MIHOMO/`: `default.yaml` (ручное добавление) и `template_remnawave.yaml` (для интеграции с панелью Remnawave).

---

## 🗺 Что роутится в DEFAULT

### 🟢 DIRECT (напрямую, виден реальный RU IP)
- Русские/белорусские домены и CIDR
- «Казённые» сервисы и CDN: VK, OK, Mail.Ru, Яндекс
- Все банки РФ (с сайта ЦБ + саморезолвинг)
- Обновления и пуши: Apple, Microsoft
- Игры: Steam, Epic Games, Riot, Escape from Tarkov
- **Faceit** — фикс для РФ-игроков, больше доступных локаций серверов
- Twitch, Pinterest

### 🔵 PROXY (через VPN)
- Google Play / Android, YouTube, Telegram, GitHub
- Twitch-ads (полное качество Source с блоком рекламы)
- Весь остальной интернет

### 🔴 BLOCK
- Домены слежки Windows
- BitTorrent DHT (экономия трафика, спокойствие хостера)
- Реклама VK

---

## 🇷🇺 DNS

| Назначение | Сервер | Зачем |
|---|---|---|
| 🏠 Domestic (direct) | Яндекс DNS `77.88.8.8` | работает везде в РФ при ТСПУ/шатдаунах, низкий пинг |
| 🌍 Remote (proxy) | Google DNS `8.8.8.8` | резолвинг проксируемого трафика |

---

## 🔄 Автообновление

GitHub Actions (`.github/workflows/update-configs.yml`):
- проверяет новые версии geo-списков каждые 6 часов
- обновляет URL и таймстемпы в JSON
- регенерирует base64-диплинки (`onadd` — авто-применение при добавлении подписки)
- коммитит автоматически

---

## 🔌 Интеграция с Remnawave

Чтобы роутинг автоматически прилетал в подписки пользователей панели —
см. [ADDON_AUTOROUTING/Remnawave/](ADDON_AUTOROUTING/Remnawave/).

Альтернатива (то что используется сейчас): диплинк `HAPP/DEFAULT.DEEPLINK`
прописывается в `happRouting` настроек подписки Remnawave — тогда Happ
применяет роутинг автоматически при добавлении подписки.

---

<div align="center">

**MixVPN** · поддержка и продление → [@vpn_mix_bot](https://t.me/vpn_mix_bot)

</div>
