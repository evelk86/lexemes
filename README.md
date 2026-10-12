- `lexemes_with_sounds.json` – všech 30 slov v požadované struktuře
- `missing_sounds.csv` – 7 slov, ke kterým je potřeba nahrávku dogenerovat

23 slov má nahrávku, 7 slov nahrávku nemá.

Anglická slova se porovnávají s textem nahrávky. Při
porovnání:
- nezáleží na velkých a malých písmenech 
- ignorují se mezery na začátku a konci
- sjednocuje se zápis diakritiky (u „café“ bylo „é“ v souborech uložené dvěma
různými způsoby).

  Ve výsledném souboru zůstávají texty v původní podobě.


- Obě slova „bat“ (netopýr i pálka) sdílejí jednu nahrávku, protože se
vyslovují stejně.
- „orange“ (pomeranč i oranžový) je v seznamu chybějících dvakrát, protože jde
  o dvě různá slova s vlastním id.
- Varianty (např. „run“ u „to run“) se pro hledání nahrávky nepoužívají
- Slova bez nahrávky mají ve JSON `"sound": null`.
- Prázdné skupiny distraktorů (`null`) se vynechávají, prázdné varianty jsou `[]`.


U nahrávky „hello“ název souboru uvádí „Emma's voice“, ale voice_name je 
en-GB-RyanNeural

U slova „café“ je mezi distraktory typu TYPO „cafe“. V angličtině je to ale oficiálně
uznáno jako správný zápis, takže by aplikace uživateli označila jako chybu odpověď, která
chybou není.

  
Úlohu jsem vypracovala s pomocí Clauda. Výsledný skript jsem si prošla a oba výstupní soubory zkontrolovala, zda odpovídají zadání.
