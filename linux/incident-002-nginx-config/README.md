# Incident 002 - Błędna konfiguracja Nginx

## Problem

Po zmianie konfiguracji Nginx przestał się uruchamiać.

## Objawy

- `systemctl status nginx` -> failed
- `nginx -t` -> błąd składni
- `journalctl -u nginx --since today` wskazuje linię z błędem

## Diagnostyka

```bash
systemctl status nginx
nginx -t
journalctl -u nginx --since today
```

## Przyczyna

Literówka w konfiguracji (linia 41).

## Rozwiązanie

```bash
nginx -t
systemctl reload nginx
```

## Wnioski

- Backup przed zmianą konfiguracji.
- Zawsze wykonuj `nginx -t` przed `reload`.
- Logi pokazują dokładne miejsce błędu.
