# Stalcraft Server Blocker

> Сделано при помощи [**unofficial-stalcraft-api**](https://github.com/Art3mLapa/unofficial-stalcraft-api)

---

## 🧩 Описание
**Stalcraft Server Blocker** — это приложение на Python, предназначенное для **блокировки игровых серверов Stalcraft** путём перехвата сетевых пакетов.  
Пользователь может **проверять пинг**, **выбирать серверы** из списка и **блокировать подключение** к ним, чтобы игра не могла установить соединение.  

Поддерживаются все основные регионы: **RU**, **EN**, **SEA**, **NA**.  
Доступно на двух языках **English** и **Русском**

---

## ⚙️ Возможности
- 🔘 **Выбор серверов** из JSON-файла (`Servers.json`)  
- 📶 **Проверка пинга** через модуль `socket` (без сторонних библиотек)  
- 🚫 **Блокировка пакетов** на портах `29450–29460` через `pydivert`  
- 💾 **Сохранение выбранных серверов и настроек** между запусками (`Settings.json`)

---

## 🧰 Требования
- **Python** ≥ 3.8  
- **Зависимости** (указаны в `requirements.txt`):
  - `PyQt6` — графический интерфейс  
  - `pydivert` — перехват и фильтрация пакетов  
- **Права администратора** — обязательны для работы `pydivert`  
- **WinDivert драйвер** — устанавливается автоматически при установке библиотеки  

---

## 🪄 Установка
1. **Скачайте репозиторий**:
   ```bash
     Нажмите кнопку `Code` и выберите `Download ZIP`. Распакуйте архив в любую папку.
   ```

2. **Установите зависимости**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Проверьте наличие файла `Servers.json`** — он должен быть в формате:
   ```json
   {
     "pools": [
       {
         "name": "Название пула",
         "region": "Регион",
         "tunnels": [
           {
             "name": "Название сервера",
             "address": "IP:Порт"
           }
         ]
       }
     ]
   }
   ```

4. **Запустите приложение**:
   ```bash
   python SBT.py
   ```
   **Или скачайте готовый исполняемый файл из [Release](https://github.com/FakeAngles/Stalcraft-Server-Blocker/releases)   и запустите его напрямую**

---

## 🚀 Использование
1. Запустите приложение от имени администратора.  
2. Выберите нужные серверы в списке.  
3. Проверьте пинг — программа протестирует доступность серверов через `socket`.  
4. Нажмите **▶ Заблокировать**, чтобы начать фильтрацию пакетов.  
5. Для остановки нажмите **■ Разблокировать**.  
6. Ваш выбор сохранится в `Settings.json`.

---

## ⚠️ Примечания
- Для работы требуется **доступ администратора**.   
- Диапазон портов блокировки: **29450–29460 (TCP/UDP)**.  
- Использование `socket` обеспечивает более стабильную проверку доступности серверов без внешних зависимостей.

---

## 👨‍💻 Авторы
Разработано **YungDaggerStab** и **WeedSellerBand**.  
Использованы библиотеки **PyQt6**, **pydivert**, и стандартный модуль **socket**.  

Благодарности:  
- [![GitHub](https://img.shields.io/badge/GitHub-@Art3mLapa-181717?style=flat&logo=github)](https://github.com/Art3mLapa) — предоставил **RU сервера**.
- **Kesame (kwlxx)** — предоставил **EN сервера**.  
- **Анонимный участник** — предоставил **SEA и NA сервера**.  

## 📞 Контакты

### **YungDaggerStab**
- ▶️ YouTube: [@PoshelNaxuy](https://www.youtube.com/@PoshelNaxuy)  
- 💬 Telegram: [@BestGook](https://t.me/BestGook)  
- 💻 Discord: `aida64`

### **WeedSellerBand**
- 💬 Telegram: [@ker9j](https://t.me/ker9j)
- 💻 Discord: `.ker9`

### **Art3mLapa**
- 🧠 GitHub: [https://github.com/Art3mLapa](https://github.com/Art3mLapa)  
- ▶️ YouTube: [@buildersc_production](https://www.youtube.com/@buildersc_production)  
- 💬 Telegram: [@bscp_podval](https://t.me/bscp_podval)  
- 💻 Discord: [discord.gg/8fKuhxQRRR](https://discord.gg/8fKuhxQRRR)

![разрешено EXBO](https://i.imgur.com/9i1wRzn.png)


