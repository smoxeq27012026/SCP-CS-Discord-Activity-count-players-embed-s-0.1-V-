# 📊 Discord Server Activity Activity (SCP:CS) :: ALPHA 0.1V
<img alt="Static Badge" src="https://img.shields.io/badge/By%20Smoxeq%20-%20scp%3Acs?style=for-the-badge&logo=scpfoundation&logoColor=black&label=SCP%3ACLASSIFIED%20SITE%20API&color=blue">
Этот плагин позволяет выводить динамическую статистику вашего сервера в Discord-канал. Вместо постоянного спама новыми сообщениями, плагин **редактирует** одно существующее сообщение, обновляя онлайн в реальном времени.
**Read this in other languages: [English](README.en.md)**
**Нашли ошибку или желаете предложить что-то к плагинам и последщим его версиям? Вам в https://discord.gg/QJrfDnapv2!**
> [!IMPORTANT]
> **Для скачивания перейдите в [Релизы / Releases](https://github.com/smoxeq27012026/SCP-CS-Discord-Activity-count-players-embed-s-0.1-V-/releases). Учтите что первое сообщение не будет обновляться до перезапуска.**
## ⚙️ Доступные конфигурации (Config)

| Параметр | Тип | Описание |
| :--- | :--- | :--- |
| `Servername_activity` | string | Название вашего сервера, которое будет в заголовке Embed. |
| `URLHook_activity` | string | URL вашего Discord Webhook. |
| `maxplayers`(игровой конфиг оффц.) | int | Максимальное количество игроков (для отображения лимита). |
| `DiscordMessageId` | string | ID сообщения, которое будет редактироваться (см. инструкцию). |

---

## 🚀 Инструкция по установке и настройке

Чтобы плагин работал в режиме "обновления", а не "спама", выполните следующие действия:

1. **Тихий режим:** Рекомендуется проводить настройку, когда на сервере **нет онлайна**.
2. **Первичный запуск:** * Заполните только `URLHook_activity` и `Servername_activity`. 
   * Поле `DiscordMessageId` оставьте **пустым**.
   * Запустите сервер.
3. **Получение ID:** * После старта раунда в Discord придет новое сообщение (Embed).
   * Нажмите на него правой кнопкой мыши и выберите **"Копировать ID сообщения"** (у вас должен быть включен Режим разработчика в Discord).
4. **Фиксация:** * Вставьте полученный ID в конфиг `DiscordMessageId`.
   * Перезапустите сервер(дождитесь окончания раунда). Теперь плагин будет изменять именно это сообщение, при каждом перезапуске сервера или раунда.

> [!WARNING]
> Если оставить поле `DiscordMessageId` пустым, плагин будет отправлять **новое сообщение при каждом старте раунда**, не удаляя старые.

---

## 🛑 Чего делать НЕ стоит
* **Не удаляйте сообщение** в Discord после того, как вписали его ID в конфиг. Если сообщение удалено, плагин не сможет его редактировать и будет выдавать ошибку.
* **Не заполняйте ID вручную** "наобум" - это приведет к ошибкам отправки. ID должен быть создан самим вебхуком при первом сообщении когда не был заполнен конфиг: `DiscordMessageId`! (Важно).
* **Избегайте частых перезагрузок** сервера в моменты пикового онлайна, чтобы не поймать временный лимит (Rate Limit) от API Discord.

---

## 🖼️ Примеры отображения

<p align="center">
  <img src="https://media.discordapp.net/attachments/1479118717475360962/1479118742217691219/image.png?ex=69aae02c&is=69a98eac&hm=ed9eaa2adeeede44eadd127782ccc74dcf2d42a77f191028660b18321863d976&=&format=webp&quality=lossless&width=689&height=320" width="80%" alt="Preview Stats">
  <img src="https://media.discordapp.net/attachments/1479118717475360962/1479119441437524148/image.png?ex=69aae0d3&is=69a98f53&hm=7f1105ef4aff7cad1ff829f862eb01a4b62ffe8b1fd6baf9c1c6e20f931d48fb&=&format=webp&quality=lossless&width=1381&height=468" width="80%" alt="Preview Stats">
</p>

---
**By Smoxeq (DeltaEX)**
