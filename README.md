# Python Academy - Project 3

## Popis projektu
Tento skript slouží k získání výsledků parlamentích voleb 2017 z jednotlivých obcí vámi zadaného okresu.  <br/>
Na této [adrese](https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=2&xnumnuts=2101) by skript extrahoval výsledky jednotlivých obcí pro okres Benešov.

## Instalace Pythonu:
__Mac OS X__: Verze Pythonu je již nainstalována.  <br/>
__Windows__: Budete muset nainstalovat jednu z verzí Pythonu 3.9 dostupných na adrese [python.org](https://www.python.org/getit/).

### Instalace knihoven:<br/>

Jednotlivé knihovny použité ve skriptu jsou v souboru `requirements.txt`. Pro instalaci doporučuji vytvoření nového virtuálního prostředí. S nainstalovaným manažerem můžete knihovny nainstalovat následovně:<br/><br/>
&emsp;  __$ pip 3__ --version &emsp; &emsp; &emsp; &emsp; &emsp;&emsp;&emsp;  # oveření verze manažeru  <br/>
&emsp;  __$ pip 3__ install -r requirements.txt  &emsp;  # instalace knihoven

## Spuštění skriptu <br/>

Pro správné spuštění skriptu `election_scraper.py`je zapotřebí v rámci příkazového řádku zadat dva argumenty.  <br/><br/>
&emsp;  python election_scraper.py <<span></span>odkaz okresu> <jméno souboru>  <br/>

Název souboru je důležité zadat s příponou __.csv__.  <br/>
Po spůštění skriptu dojde ke stažení dat a jejich uložení do zadaného názvu souboru.
  
## Ukázka projektu
  
Výsledky hlasování pro okres Benešov: <br/><br/>
&emsp;    1. Argument &emsp; `https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=2&xnumnuts=2101`  <br/>
&emsp;    2. Argument &emsp; `vysledky_benesov.csv`  <br/>
  
__Spuštění skriptu__  <br/>
<pre>
python election_scraper.py 'https://<span></span>www<span></span>.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=2&xnumnuts=2101' 'vysledky_benesov.csv'
</pre>

__Průběh skriptu__  <br/><br/>
&emsp;  CONNECTING to: 'https://<span></span>www<span></span>.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=2&xnumnuts=2101' <br/>
&emsp;  DOWNLOADING DATA from: 'https://<span></span>www<span></span>.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=2&xnumnuts=2101' <br/>
&emsp;  SAVING DATA to: '<absolutní cesta>/vysledky_benesov.csv'  <br/>
&emsp;  Closing program  <br/> 

__Částečný výstup__  <br/><br/>

|Code|City|Registered|Envelopes|Valid|Občanská demokratická strana|...|
|:---|:---|:---|:---|:---:|:---|:---:|
|529303|Benešov|13 104|8 485|8 437|1 052|...|
|532568|Bernartice|191|148|148|4|...|
...
