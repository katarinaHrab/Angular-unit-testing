# Angular Unit Testing

## Materialy na studium:

https://angular.io/guide/testing

https://dev.to/mustapha/angular-unit-testing-101-with-examples-6mc


## Ulohy:

1. Stiahnite si projekt tour of heroes: https://angular.io/guide/example-apps-list#tour-of-heroes-get-data-from-a-server

2. Urobte *npm install* a nasledne spustite testy prikazom *ng test*

3. Skontrolujte ake % kodu mame pokryte unit testami: *ng test --no-watch --code-coverage*


### AppComponent testy

1. Vytvorte test pre AppComponentu, ktory bude testovat, ze sa na stranke zobrazi napis "Tour of Heroes" ulozeny v title komponenty

2. Vytvorte test pre AppComponentu, ktory bude testovat, ze sa na stranke zobrazia 2 tlacitka/linky, ktore smeruju na Dashboard a Heroes

*hint: expect(fixture.nativeElement.querySelectorAll('a')[0].getAttribute('routerlink')).toEqual('/dashboard');*


### MessagesComponent testy

1. Vytvorte testovaci subor pre MessagesComponentu a messageServiceMock pre MessageService s mockovanymi spravami

2. Napiste test, ktory overi, ze ked z messageService nedostaneme ziadnu spravu, ziaden obsah sa nezobrazi

3. Napiste test, ktory naopak overi, ze ked sa v messages nejake spravy nachadzaju, zobrazi sa nazov 'Messages', tlacitko 'Clear messages' a konkretne spravy

4. Napiste test, ktory overi, ze ked klikneme na tlacitko 'Clear' zavola sa metodu clear z messageService 


### HeroesComponent testy

1. Vytvorte testovaci subor pre HeroesComponentu a heroServiceMock pre HeroService, ktora bude brat data z mock-heroes.ts

2. Napiste testy pre vsetky 3 metody z HeroesComponent - getHeroes, add, delete. V ramci testov overujte, ze sa vola spravna metoda z HeroService a ze data v heroes liste su aktualne (napr. ze po zavolani add metody sa prida hero do heroes zoznamu)

3. Podobne vytvorte testovacie triedy pre HeroDetailComponent a HeroSearchComponent. Piste testy, ktore maju zmysel a testuju funkcionalitu. Nemusite testovat 'kazdy napis'.
