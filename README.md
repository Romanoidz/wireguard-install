# WireGuard installer

**Этот скрипт представляет собой сценарий bash, целью которого является настройка [WireGuard](https://www.wireguard.com /) VPN на сервере Linux, как можно проще!**

WireGuard - это point-to-point VPN, который можно использовать по-разному. Здесь мы имеем в виду VPN, как в: клиент будет пересылать весь свой трафик через зашифрованный туннель на сервер.
Сервер применит NAT к трафику клиента, чтобы он выглядел так, как будто клиент просматривает веб-страницы с IP-адреса сервера.

Скрипт поддерживает как IPv4, так и IPv6. Пожалуйста, проверьте [issues](https://github.com/angristan/wireguard-install/issues) для текущей разработки, ошибок и запланированных функций!

WireGuard не подходит для вашей среды? Попробуйте [openvpn-install](https://github.com/angristan/openvpn-install).

## Требования

Поддерживаемые дистрибутивы:

- Ubuntu >= 16.04
- Debian >= 10
- Fedora
- CentOS
- Arch Linux
- Oracle Linux

## Использование
Загрузите и запустите скрипт. Ответьте на вопросы, заданные сценарием, и он позаботится обо всем остальном.

```bash
curl -O https://raw.githubusercontent.com/Romanoidz/wireguard-install/master/wireguard-install.sh
```
```bash
chmod +x wireguard-install.sh
```
```bash
./wireguard-install.sh
```
или 
```bash
wget https://raw.githubusercontent.com/Romanoidz/wireguard-install/master/wireguard-install.sh
```
```bash
bash wireguard-install.sh
```

Скрипт установит WireGuard (модуль ядра и инструменты) на сервер, настроит его, создаст службу systemd, файл конфигурации клиента и QR-код для быстрой настройки с мобильных устройств.

Запустите скрипт еще раз, чтобы добавить или удалить клиентов!
