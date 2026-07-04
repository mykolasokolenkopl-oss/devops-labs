# Incident 005 - Wysokie użycie pamięci RAM

## Problem

Serwer działa wolno.

## Diagnostyka

```bash
free -h
top
htop
ps aux --sort=-%mem | head
```

## Rozwiązanie

- Znaleźć proces zużywający pamięć.
- Sprawdzić, czy można go zrestartować.
- Sprawdzić logi.

## Wnioski

- Wysokie użycie RAM nie zawsze oznacza problem.
- Najpierw znajdź przyczynę, później podejmij działania.
