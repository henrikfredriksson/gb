# Föreläsning 6

## Konfidensintervall

{% hint style="danger" %}
Kursutveckling pågår
{% endhint %}



När man beräknar medelvärden av en stor datamängd utifrån _stickprov_ så beror medelvärdet såklart på vilken data som ingår i stickprovet. Ett sätt tackla detta problem är att ange ett intervall som innehåller det sökta medelvärdet, med en viss sannolikhet.

### Exempel

1. Livslängden för en viss bil ligger mellan 12 och 15 år med sannolikheten 0.95
2. Antalet studenter som söker till BTH per är mellan 1500 och 2000 med sannolikhet 0.8

Intervallen i exemplen ovan kallas _konfidensintervall_ och är ett mått på den osäkerhet slumpen bidrar med när vi försöker skatta den bakomliggande populationens medelvärde.

{% hint style="info" %}
Konfidensintervallet är en skattning av hur pass säkert eller osäkert medelvärdet är i en undersökning.
{% endhint %}

Två viktiga egenskaper för konfidensintervall

* Högre konfidensgrad \(säkerhet\) leder till bredare intervall
* Större stickprov leder till smalare intervall

För ett stickprov med $$n$$ observationer så gäller det att stickprovets medelvärde

$$
\overline { X } = \frac { 1 } { n } \sum x _ { i }
$$

Låt $$X$$ vara en normalfördelad slumpvariabel med väntevärde $$\mu$$ och standardavvikelse $$\sigma$$. 

Vi gör ett stickprov med $$n$$ observationer. Då gäller att

* stickprovets medelvärde $$\overline{X}$$ 
* är normalfördelat med väntevärdet $$\mu$$ 
* och standardavvikelsen $$\cfrac{\sigma}{\sqrt{n}}$$ .

Stickprovets medelvärde $$\overline{X}$$ befinner sig med $$95\%$$ sannolikhet i intervallet

$$
\left[\mu - 1.96\cdot \dfrac{\sigma}{\sqrt{n}}, \mu +1.96\cdot \dfrac{\sigma}{\sqrt{n}} \right]
$$

Man kan visa att

$$
\operatorname { Pr } \left[ \overline { X } - 1,96 \cdot \frac { \sigma } { \sqrt { n } } < \mu < \overline { X } + 1,96 \cdot \frac { \sigma } { \sqrt { n } } \right] = 95 \%
$$

Med hjälp av ovanstående så kan man hitta ett intervall där medelvärdet befinner med $$95\%$$ sannolikhet.

Om man ökar intervallets storlek så ökar såklart sannolikheten att väntevärdet befinner sig i intervallet. Det gäller att

$$
\Pr\left[ \overline { X } - 2.58 \cdot \frac { \sigma } { \sqrt { n } } , \overline { X } + 2.58 \cdot \frac { \sigma } { \sqrt { n } } \right] = 99\%
$$

Om man minskar intervallets storlek så minskar även sannolikheten

$$
\Pr\left[ \overline { X } - 1.64 \cdot \frac { \sigma } { \sqrt { n } } , \overline { X } + 1.64 \cdot \frac { \sigma } { \sqrt { n } } \right] = 90\%
$$

### Exempel

Ett stickprov på 100 studenter var medelålder 24.4 och standardavvikelsen 3.1 år. En intervallskattning av  på medelåldern på alla studenter är alltså medelåldern är mellan 

* 23.8 och 25 år med 95% sannolikhet
* 23.6 och 25.2 år med 99% sannolikhet

### När $$n \to \infty$$.

Vi ser att när $$n$$ växer så blir intervallet mindre och mindre. Ju större stickprov vi tar, desto närmare kommer vi det faktiska medelvärdet.

Stora talens lag säger att om $$\overline{X_n}$$ är medelvärdet av $$n$$ likafördelade oberoende stokastiska variabler $$X_1, . . . , X_n$$ med ändlig varians, så gäller följande

{% hint style="info" %}
## Stora talens lag

$$\mathrm { Pr } \left( \left| \overline { \mathrm { X } } _ { \mathrm { n } } - \mu  \right| > \varepsilon \right) \rightarrow 0 \quad \text {då } n \rightarrow \infty$$ 

för varje $$\varepsilon > 0$$ 
{% endhint %}

## Konfidensintervall för populationens andel

På liknande sätt så kan man bestämma andelen individer med en viss egenskap i en population. Antag att vi gör en undersökning med $$n$$ observationer och $$p$$ andelen av hela populationen så besitter den sökta egenskapen.

Om $$n\cdot p (1-p) > 5$$ så är ett konfidensintervall för hela populationens andel $$\pi$$ 

$$
p \pm z \cdot \sqrt { \frac { p ( 1 - p ) } { n } }
$$

där $$z$$ är 1.64, 1.96, 2.58 för 90, 95, 99% säkerhet.



