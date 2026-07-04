# Incident 004 - Brak miejsca na dysku

## Problem

Serwer działa niestabilnie z powodu braku wolnego miejsca.

## Diagnostyka

```bash
df -h
du -ah | sort -rh | head -n 10
find / -type f -size +500M
```

## Rozwiązanie

- Zidentyfikować największe pliki.
- Wykonać backup przed usunięciem.
- Usunąć niepotrzebne dane.

## Wnioski

- Zawsze wykonaj backup.
- Nie usuwaj plików systemowych bez analizy.
