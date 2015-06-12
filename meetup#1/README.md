# Meetup #1

## Warsztaty
Warsztaty polegają na zainstalowaniu maszyny z Zabbixem, zapoznaniu się z interfejsem webowym oraz wykorzystaniu funkcji autorejestracji agentów w jednym, centralnym serwerze.
Są one przeprowadzane w formie BYOL *(Bring Your Own Laptop)* - potrzebujesz  laptopa, którego zabierzesz na warsztaty. 

### Wymagania

Laptop powinien posiadać co najmniej **1GB** wolnej pamięci i trochę dysku na odpalenie maszyny wirtualnej. Oczywiście najlepiej jak będzie miał system linuksowy, ale dowolny system, na którym odpalisz VirtualBoxa będzie ok.
Potrzebujesz też następujących rzeczy, aby w pełni skorzystać z warsztatów:
  * Zainstalowane oprogramowanie [vagrant](https://www.vagrantup.com/downloads.html)
  * Zainstalowany [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

### Przygotowanie
Ze względu na czas operacji następujące kroki najlepiej wykonaj przed przyjściem:
  * Ściągnij kod konfiguracji maszyny z repozytorium:

  ```
  git clone https://github.com/slashr00t/vagrant-zabbix
  ```
  * Wejdź do katalogu i uruchom maszynę

  ```
  vagrant up
  ```
  * Po kilkunastu minutach (w zależności od szybkości łącza i twojego sprzętu) maszyna zainstaluje się - sprawdzisz to logując się do interfejsu [http://localhost:8080/](http://localhost:8080)
  * Możesz wyłączyć maszynę - resztę czynności dokonasz już na warsztatach

### Na warsztatach
Poniższe działania powinny być wykonane już na warsztatach. Zakładane jest, że masz przygotowane środowisko zgodnie z wcześniejszym opisem.

  * Odpal swoją maszynę - wejdź do katalogu z repozytorium (patrz *Przygotowanie* wyżej) i uruchom komendą

  ```
  vagrant up
  ```
  * Zaloguj się do maszyny korzystając z konsoli graficznej VirtualBox twojej maszyny wirtualnej - użytkownik **root** z hasłem **vagrant**
  * Zmień nazwę domenową hosta na taką, które zidentyfikuje ciebie (dowolna nazwa) w domenie **meetup.zabbix** - to pozwoli na rejestrację w centralnym systemie

  ```
  sudo hostnamectl set-hostname mojnazwa.zabbix.meetup
  ```
  * Otwórz plik konfiguracyjny **/etc/zabbix/zabbix_agentd.conf** swoim ulubionym edytorem i zmień wartość parametru **ServerActive** dodając kolejny adres IP podany przez prowadzącego

  ```
    ServerActive=127.0.0.1, A.B.C.D
  ```
  * Zrestartuj usługę agenta zabbixa

  ```
  sudo systemctl restart zabbix-agent
  ```
  * I to by było na tyle :-)



