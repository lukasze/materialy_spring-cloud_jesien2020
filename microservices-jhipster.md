# 0. Przed kolejnymi krokami - zainstalowany git, npm, JHipster

    https://git-scm.com/downloads
    https://nodejs.org/en/download/ (zawiera npm)
    https://www.jhipster.tech/installation/
    

# 1. JHipster Registry 

## Klonowanie i uruchomienie:
    git clone https://github.com/jhipster/jhipster-registry.git && cd jhipster-registry && ./mvnw

# 2. JHipster Console
	
	https://github.com/jhipster/jhipster-console/blob/master/bootstrap/docker-compose.yml

## Wykomentuj komponent alerter (problemy w windows, potrzeba dociagania plikow etc.) 

## Wystartuj docker-compose (w katalogu głównym z projektami)

	docker-compose up

# 3. Wygenerowanie aplikacji 

## Pobranie pliku jdl, ze zdefiniowanymi komponentami aplikacji

	https://github.com/ContextMapper/context-mapper-examples/blob/master/src/main/cml/microservice-generation/JDL-example/generated-insurance-microservices.jdl

## Jhipster w konsoli - wygenerowanie projektow na podstawie pliku jdl

	jhipster jdl generated-insurance-microservices.jdl


# 4. Import do IDE, zmiana w plikach application-dev.yml i uruchomienie 

## Importujemy katalog z wygenerowanymi aplikacjami do IDE.

## Ustawiamy, w plikach application-dev.yml - dla poszczególnych kopmonentów - flagi na true (pliki są w formacie yaml)

	jhipster.logging.logstash.enabled
	
	jhipster.metrics.logs.enabled

## Startujemy aplikacje (z poziomu IDE)


## Dodatkowo dla gateway (w katalogu projektu) uruchomienie frontend'u

	npm start (haslo admin / admin)

# Przydatne linki:

[jhipster - architektura](https://www.jhipster.tech/microservices-architecture/)

[jhipster- generowanie microserwisów](https://contextmapper.org/docs/jhipster-microservice-generation/)


