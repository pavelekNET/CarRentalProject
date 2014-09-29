CarRentalProject
==========

Co aplikace nezahrnuje
================================
JS testy
kompletní pokrytí testy - testy pokrývají pouze základní rámec funkčností.
zdokumentovaný JS kód - některé části obsahují komentáře, ale je to pouze občasné.

Co je nutno nastavit pro správné fungování aplikace
================================================================
v js klientovi je potřeba aby souhlasil server API (defaultně localhost:1333) a to se nastavuje v "app/config/config.global.ts":

jedná se o řádek:
public static serverAdress = "http://localhost:1333/api/";

POZOR, musí běžet Grunt, jinak se změna nepromítne do zbuilděného js souboru.
pokud se tomuto chcete vyhnout, tak stačí adresu serveru změnit přímo v js souboru, tedy v "app/_build/out/out.js"

Struktura js klienta
================================
Common - obsahuje genericke repozitáře
CarRentalDB - obsahuje in-memory DB
CarRentalClient - JS klient vytvořený pomocí TypeScript. Hlavní aplikace je ve složce app
  app/
      _build - nastavení pro Grunt (po spuštení Node.js příkazu "Grunt" nad touto složkou je konfigurace spuštěna
      config - třídy a metody pro nastavení aplikace
      layout - základní nastavení vzhledu a umístění routovacího pohledu v aplikaci
      modals - třídy a html soubory pro modální okna
      models - třídy užívané v JavaScript klientovi
      services - služby použitelné v JavaScript klientovi
      templates - pohledy aplikace
      app.ts - základní konfigurační soubor aplikace
  content - css a fonty (případně obrázky)
  scripts - js knihovny třetích stran
      
CarRentalAPI - API pro JS klienta - ASP.NET MVC 5.0 WebAPI v2
CarRentalAPI.Tests - základní testy pro CarRentalAPI controllery (repozitáře, tedy projekt Common jsem netestoval)

