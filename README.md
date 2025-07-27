# 🧰 Ansible Playbooks for Semaphore

To repozytorium zawiera zestaw gotowych playbooków Ansible wykorzystywanych w systemie automatyzacji **Ansible Semaphore**. Każdy playbook realizuje określone zadanie administracyjne na serwerach z systemami Linux (Debian/Ubuntu oraz RHEL/CentOS).

## 🚀 Jak używać w Semaphore

1. **Dodaj repozytorium Git** w interfejsie Semaphore jako nowy projekt.
2. **Zdefiniuj inventory** – np. `all`, `prod`, `test`, `debian_only`, itp.
3. **Stwórz szablony zadań (task templates)** dla każdego playbooka:
   - Wybierz odpowiedni plik `.yml`
   - Ustaw użytkownika (`become: true` jeśli wymagane)
   - Dodaj ewentualne parametry (np. tagi)
4. **Uruchamiaj ręcznie lub przez harmonogram (cron)** w Semaphore.

## ✅ Wymagania

- Ansible 2.10+
- Semaphore 2.x (zintegrowane z tym repozytorium Git)
- Serwery z poprawnie skonfigurowanym SSH
- Ewentualnie `sudo` bez hasła dla użytkownika Ansible (`NOPASSWD:`)

## 📌 Uwagi

- Playbooki są podzielone według funkcji — łatwo je rozbudować o własne role.
- Używają wbudowanych modułów (`apt`, `yum`, `reboot`, `stat`, `debug` itd.).
- Zaleca się używanie oddzielnego środowiska testowego przed użyciem na produkcji.

## 📃 Licencja

MIT – używaj, modyfikuj, rozszerzaj.
