# Incident 001 – 502 Bad Gateway

## Cel

Nauczyć się diagnozować błąd 502 Bad Gateway.

## Scenariusz

Objaw:

- Strona zwraca 502 Bad Gateway.

## Plan diagnostyki

1. Sprawdzić odpowiedź HTTP.

```bash
curl -I http://localhost
```

2. Sprawdzić status nginx.

```bash
systemctl status nginx
```

3. Sprawdzić konfigurację.

```bash
nginx -t
```

4. Sprawdzić logi nginx.

```bash
journalctl -u nginx --since today
```

5. Sprawdzić backend (PHP-FPM).

```bash
systemctl status php*-fpm
```

## Wniosek

(To uzupełnimy po wykonaniu ćwiczenia.)
