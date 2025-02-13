# Vad är en signal?

## Förord

### Syftet med utbildningen

Att ge en individen, oberoende fördjupningsområde, en förståelse för grundläggande fysik med utgångspunkt från specifik verksamhet och nomenklatur. Utbildningen skall genomföras under individens första tid för att ge möjligheten att se samband mellan fysik och de begrepp och den teknik som vardagen består av. Känslan av verksamheten består av ”svart magi” ska minska. Utbildningen skall också ses som en grund till vidare teknisk utbildning inom respektive fördjupningsområde, som i många fall kommer många veckor senare.

### Målet med utbildningen

Efter genomförd utbildning ska individen kunna se grundläggande samband mellan fysik och teknik inom följande områden:

- Sinusvågen
- Tid och frekvens
- dB och brus
- Kapacitet
- Signalens väg

### Avgränsningar

Utbildningen syftar inte till att förklara hur tekniken fungerar då det tillhör utbildning som genomförs inom ramen för respektive fördjupningsområde.

Den syftar heller inte till att härleda fysikaliska och matematiska samband utan istället skall sambanden påvisas.

### Tidsåtgång

TBD
LABB

## Index

- [Kapitel 1: Sinusvågen](#chapter-1-sinusvagen)
- [Kapitel 2: Tids och frekvensdomän](#chapter-2-tid-v-fq)
- [Kapitel 3: Frekvensspektrumet](#chapter-3-frekvensspektrumet)
- [Kapitel 4: Brus](#chapter-4-brus)
- [Kapitel 5: Kapacitet](#chapter-5-kapacitet)
- [Kapitel 6: Signalens väg](#chapter-6-signalens_vag)

---

<details>
<summary><h2 id="chapter-1-sinusvagen">Kapitel 1: Sinusvågen</h2></summary>

### Definition

Oberoende överföringsteknik eller kommunikationsform är det sinusvågen som är möjliggöraren. När sinusvågen färdas i ett godtyckligt medium breder den ut sig likt vågringar på vatten. Vågen existerar i tre dimensioner. 

<br>

> *"En sinusvåg är den naturliga svängningsrörelsen för ett fritt svängande system."* Här finns mer att läsa om [sinusvågen.](https://sv.wikipedia.org/wiki/Sinusv%C3%A5g)

<br>
Sinusvågen defineras med hjälp av ett antal egenskaper.
<br>

![Sinusvåg](./sine_wave.png "Sinusvåg")

<div align="center">

$y(t) = A \cdot \sin(2 \pi f t + \phi)$

</div>

- $A$ = Kurvans amplitud
- $f$ = Kurvans frekvens
- $\phi$ = Kurvans fasförskjutning


### Varför är det viktigt?

När en sinusvåg färdas i ett godtyckligt medium vid vissa frekvenser, gör den det i form av elektromagnetisk energi och benäms ofta som en *radiosignal*. En sändare genererar signalen som i sin tur tas emot av mottagaren. För att signalen ska kunna bära information behöver sändaren och mottagaren komma överens om ett gemensamt "språk". Sändaren behöver alltså ändra signalens egenskaper så att mottagaren i sin tur kan översätta ändrigarna till information.

Dessa engenskapsförändringar, eller anpassningar, benäms *modulation*. När sändaren modulerar en omodulerad signal (CW) och överför den, kommer mottagaren att *demodulera* samma signal för att komma åt informationssignalen. 

![Sinusvåg](./am_fm_time_domain.png "AM/FM")

<!---
17_lektioner.pdf sidan 65
-->

</details>

---

<details>
<summary><h2 id="chapter-2-tid-v-fq">Kapitel 2: Tids och frekvensdomän</h2></summary>

### Definition
Vi har i förra kapitel tittat på matematiska och fysikaliska fenomen med avseende på tid, där tiden utgjort x-axeln i grafen. Ett annat och minst lika vanligt sätt att beskriva signalen är att göra det utifrån dess frekvens.

I enkla ord:

- **Tidsdomän**: Visar hur en signal förändras över tid. Du ser signalens värde vid varje ögonblick.
- **Frekvensdomän**: Visar hur mycket av signalen som finns vid olika frekvenser.

### Varför är det viktigt?
Det finns många anlednigar till varför man vill kunna analysera en signal med avseende olika domänder men den mest uppenbara är underlättandet att studera repetitiva fenomen, till exempel radiovågor. I grafen nedan illustreras en signal i tidsdomänen med tid (s) på x-axeln och ytterligare en signal i frekvensdomänen med frekvensen (Hz) på motsvarande axel.

<br>

![Domäner](./time_freq_domain.png "Tid/Frekvens")

<br>

> Frekvensen är det inverterade värdet av periodtiden: <br> $f = 1 / T$

> Sambandet mellan ljusets utbredningshastighet c i vakuum, frekvensen f och våglängden λ: <br> $λ = c / f$ <br>

> *Transformteori* är ett sammanfattande namn på de delar av matematiken som beskriver transformer. Här kan du läsa mer om [Fouriertransform](https://sv.wikipedia.org/wiki/Fouriertransform)

</details>

---

<details>
<summary><h2 id="chapter-3-frekvensspektrumet">Kapitel 3: Frekvensspektrumet</h2></summary>

### Definition
Ett frekvensspektrum är ett avgränsat område med frekvenser. Inom radiotekniken anses det användbara frekvensområdet omfatta frekvenser mellan 10 kHz till 300 GHz. Det är dock långt ifrån det enda definerade frekvensspektrumet. Som exempel nyttjas spektrumet för ljus när information överförs i [fiberoptisk kabel.](https://en.wikipedia.org/wiki/Wavelength-division_multiplexing)

<br>

![Frekvensspektrum](./spektrum.jpg "Telekrig 1997")

I figuren nedan ses en skärmdump tagen över ett skarpt frekvensspektrum. En radiomottagare som kopplats till en dator har konfigurerats att motta signaler runt om kring 140 MHz - 150 MHz. X-axeln visar frekvensen och y-axeln visar amplituden. Mitt i figuren ses ett antal signaler som i detta fall bär en nyttosignal. Fleralet av de nyttosignaler som mottagaren tar emot har mjukvaran markerat med gula cirklar för att påvisa signalens amplitud. 

Utöver att mottagaren tar emot signalen med en viss signalstyrka, alokerar signalens bredd ett visst frekvensutrymme. Signalens bredd benäms bandbredd. Bandbredden är ett mått på det frekvensområde som en signal upptar, och en högre informationsöverföringshastighet kräver ett större frekvensområde för att kunna överföra mer data per tidsenhet.

I foten på nyttosignalerna ses ett blått område som övergår i svart. Området består av brus där "taket" av rektangeln benämns brusgolv. Brus är en signal där vi inte känner signalens tidsfunktion, utan bara dess amplitudspektrum. Brus alstras av flera olika, av varandra oberoende generatorer. Alstringen sker bland annat i atmosfären, i rymden och internt i våran mottagare med egenskapen att amplituden följer normalfördelningsprincipen.

### Varför är det viktigt?

Den fysikaliska faktorn avgränsar oss till att använda vissa frekvenser även fast frekvenserna, inom ramen för signalteorin kan anta ett oändligt antal värden. Vi måste också förhålla oss till den omgivning som vi sänder och mottager i. En för svag mottagen signal löper risk att "försvinna" i bruset.

Överföring av information med hjälp av elektromagnetisk energi kommer alltså med begränsningar. Mer om dessa begränsningar i efterföljande kapitel.

<br>

![SDR](./sdr.JPG "SDR#")


> Här kan du förkovra dig i brus; [AGWN.](https://en.wikipedia.org/wiki/Additive_white_Gaussian_noise)

> Vill du börja leta signaler? Hobbyn är billig och kräver ingen särskilld förkunskap. Läs mer om [SDR.](https://www.rtl-sdr.com/rtl-sdr-quick-start-guide/)

</details>

---

<details>
<summary><h2 id="chapter-4-brus">Kapitel 4: Signal till brus</h2></summary>

### Definition

När en signal lämnare en sändare genomför det med en viss mängd effekt (W). Intill dess att signalen uppfattas av mottagaren kommer den utsättas för *dämpning*. Alla delar i en signalkedja som inte förstärker signalen kommer att påverka den negativt, till exempel förlust i kabel och fri i rymd. Däpningen är även relaterad till frekvensen, där däpningen ökar med ökad frekvens.

När en mottagare tar emot en signal, gör den det med en viss kvalitet. Kvaliteten på signalen kan mätas på många olika vis. Ett sätt är att bestämma dess signal-brus-förhållande (SNR), vilket är skillnaden i nivå mellan signal och brus. SNR mäts i decibel (dB).


![Signal-Brus-Förhållande](./snr.png "snr")

Det logaritimiska måttet dB är en användbart verktyg när stora och små värden hanteras samtidigt. Genom att använda dB kan till exempel en hög och låg signalstyrka jämföras även fast de linjära värdena ligger långt från varandra. dB är ett relavitvt mått och har per definition ingen enhet. Måttet refereras istället till en effektnivå.

<br>

<div align="center">

$dBm = 10 \cdot \log_{10}(mW) + 30$

</div>

<div style="display: flex; justify-content: space-between;">

<div style="flex: 1; margin-right: 10px;">
  
| Linjär (mW)   | Logaritmisk (dBm)  | 
|---------------|--------------------|
| 1             | 0                  |
| 2             | 3                  |
| 10            | 10                 |
| 100           | 20                 |
| 1000          | 30                 |

</div>

<div style="flex: 1; margin-left: 10px;">

| dBm   | Sändare     |
|-------|-------------|
| 80    | Rundradio   |
| 60    | Mikrovågsugn|
| 27    | Mobilsite   |
| 15    | WiFi        |
| 10    | Bluetooth   |


</div>

</div>

### Varför är det viktigt?
När ett system för kommunikationsöverföring designas måste tillgänglig effekt budgeteras, vilket kallas för länkbudget. Genom att räkna på signalstyrkan för varje steg i överföringskedjan och analysera förluster är det i slutändan mottagarens tolerans för SNR som är gränssättande. Om insignalen till mottagaren har utsatts för hög däpning under överföringen riskerar signalen försvinna i bruset och informationen går förlorad.

> Här kan du läsa mer om [länkbudget.](https://pysdr.org/content/link_budgets.html)

<br>

Ett sätt att visualisera hur en digital signal uppträder i en mottagare är att använda ett konstellationsdiagram. Desto mer brus som signalen (QPSK) utsätts för, desto svårare har mottagaren att uppfatta rätt symbol. Alltså kommer bitfelshalten (BER) att öka med med minskad SNR.  

![QPSK+AGWN](./qpsk.png "QPSK+AGWN")

> Ett sätt att ta höjd för höga bitfelshalter är att nyttja [kanalkodning.](https://sv.wikipedia.org/wiki/Kodningsteori)

> Mer om digital fasmodulering i radiolänk; [TCM.](https://en.wikipedia.org/wiki/Trellis_coded_modulation)

</details>

---

<details>
<summary><h2 id="chapter-5-kapacitet">Kapitel 5: Kapacitet</h2></summary>

### Definition

</details>

---

<details>
<summary><h2 id="chapter-6-signalens_vag">Kapitel 6: Signalens väg</h2></summary>

### Definition

</details>

---

**Skapare:** Johannes Andersson

**Datum skapad:** 2025-01-15  

