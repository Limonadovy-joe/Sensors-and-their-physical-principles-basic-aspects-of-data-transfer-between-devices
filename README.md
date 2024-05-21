# Sensors-and-their-physical-principles-basic-aspects-of-data-transfer-between-devices

- [Signal](#signal)
- [Principles of physical quantity converters](#principles-of-physical-quantity-converters)
  - [Temperature](#Temperature)
  - [Current](#current)
  - [Resistance](#resistance)
  - [Eletric Power](#eletric-power)
  - [Eletric Capacitance](#eletric-capacitance)
  - [Inductance](#inductance)
  - [Frequency](#frequency)
 

## Signal
- V technice se slovo signál používá v poněkud posunutém významu pro **fyzikální veličinu závislou na čase.**
- signály optické, elektrické, elektromagnetické, akustické, mechanické, pneumatické, nebo hydraulické.

- **Signál ve spojitém čase** je definovaný pro všechny okamžiky na intervalu: - jde tedy o **nespočetnou množinu časových okamžiků.**
  - **Signál může být definovaný na celém reálném čase: t ∈ (−∞,∞).**
    -  Příklad: Signál x(t) = sin⁡(t) je definován pro **všechny reálné hodnoty času t**. Tento signál je **sinusová vlna, která osciluje nekonečně v čase.**
    -  Příklad signálu, který odpovídá sinusové vlně oscilující nekonečně v čase: Střídavé elektrické napětí v síti
  - Pouze na určitém časovém úseku: t∈[0,T], kde T je nějaký konečný časový okamžik.
  - Může být definovaný na jiném konkrétním intervalu, například t∈[a,b] **kde a a b jsou konkrétní reálné časové okamžiky.**
  
 <br>
 
- **Signál v diskrétním čase**, je definován jen pro určité časové okamžiky , z čehož plyne, že se jedná o **spočetnou množinu.**
  -  Diskrétní časový signál lze tedy popsat jako **posloupnost hodnot.** Intervaly v diskrétním čase:
    - **Celý početní interval**: n ∈ Z, Signál je definován pro všechny celé čísla, **tedy pro všechny časové okamžiky n.**
      - Priklad: **Digitální komunikace** - Binární signál přenášený digitálním komunikačním kanálem.
      - Sekvence bitů x[n] může reprezentovat digitální data (např. 1s a 0s): x[n]={1,0,1,1,0,…}
    - **Omezený interval**: n ∈ {0,1,2,…, N − 1 }
      - Signál je definován pro konečný počet vzorků, což odpovídá konkrétnímu počtu časových okamžiků.
      - Priklad: Video signál (frame sekvence) - Sekvence snímků (frames) v digitálním videu
      - Video signál může být reprezentován jako **posloupnost obrazových snímků x[n]**, kde každý snímek je zachycen v určitý časový okamžik nn s pevnou snímkovací frekvencí (např. 30 fps).
     
- **Determinovaný signál** - je takový signál u nějž lze určit hodnotu v jakýkoliv okamžik s absolutní jistotou.
  - **Periodické** - signál je definovaný pro frekvence a **harmonický nebo neharmonicky průběh**
    - **Harmonický** signál je takový signál, který lze vyjádřit funkcí f(t) - **může být modelován funkcemi sinus nebo kosinus**
    - **Neharmonický signál**
      -  Neharmonický signál lze vyjádřit pomocí **Fourierovy řady** , která **rozkládá signál na nekonečnou sumu sinusových a kosinusových funkcí.**
      -  Pro neperiodické signály může být použit **Fourierova transformace** k vyjádření signálu jako **integrálu harmonických složek s různými frekvencemi.**
  - **neperiodické signal** - nemá periodu, často nazývá **aperiodický signál.**
    - **Impulsní signál (Diracův delta impuls)**
      -  **Diracův delta impuls** je matematickým konceptem s **nekonečnou amplitudou a nulovou šířkou v čase**
      -  **Impulsní charakteristika** je odezva lineárního časově invariantního systému (LTI) na tzv. **Diracův jednotkový impuls**
        -  je důležitým nástrojem teoretické analýzy **LTI systémů (tedy například filtrů, zesilovačů, PID regulátorů apod.)**, protože **konvolucí** vstupu s impulzní odezvou lze získat výstup LTI systému.
      - Využití v elektrotechnice - Teorie obvodů:  elektrický obvod obsahující zdroj napětí V a odpor R. Při analýze chování obvodu může nastat situace, kdy chceme určit proud, který prochází v určitém čase **t**. V okamžiku t=0 se **zdroj napětí V náhle zapne.**
      - Diracův delta impuls k popisu **okamžité změny napětí na zdroji V**
      - Napětí V(t) na zdroji v čase t lze vyjádřit pomocí Diracova delta impulsu δ(t)δ(t) 
      - umožňuje matematické modelování a analýzu **náhlých změn v elektrických obvodech**
      - **Šum (náhodný signál), Exponenciálně rostouci, klesající signál**

- **Stochastický signál** - velikost signálu v libovolném okamžiku, **dovedeme určit pouze s nějakou pravděpodobností.**
- Stacionární signály  jejichž **statistické vlastnosti zůstávají stejné při posunu v čase**. To znamená, že tyto signály nejsou závislé na poloze počátku časové osy.
  -  **stacionární** - nejsou závislé na poloze počátku časové osy. - **ergodické, neergodické**
  -  **nestacionární** - jsou závislé na poloze počátku časové osy

- Existují signály, které nejsou deterministické ani stochastické. Přiřazení do určité kategorie není absolutní.
- **V případech, kdy je deterministický popis signálu příliš složitý se může vyplatit zpracovávat jej jako stochastický signál.**

- **Signál se spojitou amplitudou**
  - Spojitý signál má definici takovou, že jeho **amplituda je spojitá funkce času**, což znamená, že nemůže mít nespojitosti.
  - Spojitý signál je signál, **který nemá žádné skoky ani přerušení v amplitudě v žádném bodě svého trvání.** To znamená, že pro každý bod v čase t platí, **že limita signálu zleva a zprava se rovná hodnotě signálu v tomto bodě.**

- **Signál s nespojitou(diskrétní) amplitudou**

<br>

- Elektrické signály jsou nosič informace, přičemž vlastní signál může být stejnosměrný, nebo střídavý.
- Střídavý signál může být dále **nízkofrekvenční (nf) nebo vysokofrekvenční (vf), analogový (spojitý) nebo digitální (nespojitý).**
- Příklad: Telefonní signál – přeměnou akustické energie lidského hlasu na energii elektrickou se vytváří **elektrický nízkofrekvenční signál** a  je v kmitočtovém hovorovém pásmu 300–3400 Hz

- 


## Principles of physical quantity converters
- Převodníky  slouží k převodu jedné fyzikální veličiny na jinou formu, **často na elektrický signál**, aby bylo možné veličinu měřit, monitorovat nebo regulovat.
- Principy převodníků lze rozdělit podle různých kritérií, včetně typu převáděné veličiny (teplota, tlak, síla, pohyb, světlo atd.)


## Temperature
- Při měření teploty t se využívá vždy **nepřímá metoda**, při níž se přímo měří obecně jiná veličina A, která je na teplotě t závislá podle určitého vztahu
- A = f(t)    (1)
-  Vztah (1) může být více či méně složitý a z **něho lze hodnotu teploty číselně vypočítat [1].**
-  


