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


