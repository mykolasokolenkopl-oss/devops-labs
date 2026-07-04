# Incident 003 - PHP-FPM nie działa

## Problem

Nginx zwraca 502 Bad Gateway.

## Diagnostyka

```bash
curl -I http://localhost
systemctl status php*-fpm
journalctl -u php*-fpm --since today
```

## Możliwe przyczyny

- PHP-FPM zatrzymany.
- Błędna konfiguracja.
- Brak katalogu `/run/php`.
- Zły socket.

## Rozwiązanie

Naprawić przyczynę, a następnie sprawdzić:

```bash
systemctl status php*-fpm
curl -I http://localhost
```

## Wnioski

502 nie oznacza problemu z Nginx. Najpierw sprawdź backend.
