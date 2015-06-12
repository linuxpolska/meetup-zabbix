# Meetup #1

## Warsztaty
Warsztaty polegają na zainstalowaniu maszyny z Zabbixem, zapoznaniu się z interfejsem webowym oraz wykorzystaniu funkcji autorejestracji agentów w jednym, centralnym serwerze.
Są one przeprowadzane w formie BYOL *(Bring Your Own Laptop)* - potrzebujesz  laptopa, którego zabierzesz na warsztaty. 

### Wymagania

Laptop powinien posiadać co najmniej **1GB** wolnej pamięci i trochę dysku na odpalenie maszyny wirtualnej. Oczywiście najlepiej jak będzie miał system linuksowy, ale dowolny system, na którym odpalisz VirtualBoxa będzie ok.
Potrzebujesz też następujących rzeczy, aby w pełni skorzystać z warsztatów:
  * zainstalowane oprogramowanie [vagrant](https://www.vagrantup.com/downloads.html)
  * zainstalowany [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

### Przygotowanie
Ze względu na czas operacji następujące kroki najlepiej wykonaj przed przyjściem:
  * ściągnij kod konfiguracji maszyny z repozytorium:
  ```
  git clone https://github.com/slashr00t/vagrant-zabbix
  ```
  * wejdź do katalogu i uruchom maszynę
  ```
  vagrant up
  ```
  * po kilkunastu minutach (w zależności od szybkości łącza i twojego sprzętu) maszyna zainstaluje się - sprawdzisz to logując się do interfejsu [http://localhost:8080/](http://localhost:8080)
  * możesz wyłączyć maszynę - resztę czynności dokonasz już na warsztatach

