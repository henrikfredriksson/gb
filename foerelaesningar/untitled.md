---
description: binomialfördelning
---

# Föreläsning 4

## Inledande exempel

Enligt BTHs årsrapportering från 2017 så var antalet helårsstudener $$2652$$. Av dessa så var $$36\%$$ kvinnor och $$64\%$$ män.

Om vi slumpvis väljer $$5$$ studenter, vad är då sannolikheten att få exakt 3 kvinnliga studenter?

Ett möjligt utfall är

$$
\text{Man, Kvinna, Kvinna, Man, Kvinna}
$$

Sannolikheten för detta utfall är

$$
0.64\cdot 0.36 \cdot 0.64 \cdot 0.36 \cdot 0.36 = 0.64^2\cdot 0.36^3
$$

Ett annat möjligt utfall är 

$$
\text{Kvinna, Kvinna, Man,  Man, Kvinna}
$$

med samma sannolikhet eftersom

$$
0.36 \cdot 0.36 \cdot 0.64 \cdot 0.64 \cdot 0.36 = 0.64^2\cdot 0.36^3
$$

Det $${5} \choose {3}$$ ordningsföljder med $$3$$ kvinnor och $$2$$ män. Sannolikheten är alltså 

$$
{{5} \choose {3}} \cdot 0.64^2\cdot 0.36^3 \approx 0.19
$$

## Binomialfördelning

Binomialfördelning används när man gör ett slumpmässigt urval med $$n$$ individer ur en stor population och räknar antalet individer $$X$$ med en viss egenskap.

Om sannolikheten att en individ \(eller att ett försök lyckas\) har en viss egenskap med sannolikhet $$p$$, där $$0<p<1$$, så är sannolikheten för individen inte har egenskapen $$1-p$$ \(försöket misslyckas\).  Vad är sannolikheten att att exakt $$k$$ individer har en vissa egenskap eller att $$k$$ försök är lyckade?

$$
\Pr(X=x) = {{n}\choose {x}} \cdot p^{x} (1-p)^{n-x}
$$

{% hint style="danger" %}
I boken används $$\pi $$ istället för $$p$$ ovan.
{% endhint %}

{% hint style="info" %}
Binomalfördelning används när sannolikheten inte förändras mellan försöken
{% endhint %}

### Exempel

Det är ungefär $$0.2$$ sannolikhet att det är vinst på en trisslott. Om man köper och skrapar $$100$$stycken vinstlotter. Vad är sannolikheten att det **exakt** på $$3$$ stycken lotter?

$$
\Pr(X=3) = {{100} \choose {3}} \cdot 0.2^3 \cdot 0.8^{97} = 5.147 \cdot 10^{-7} = 5.147 \cdot 10^{-7}.
$$

Vad är sannolikheten att det är vinst på **högst** $$3$$ stycken lotter?

$$
\Pr(X \leq 3) = \Pr(X=0) + \Pr(X=1) + \Pr(X=2) + \Pr(X=3) = 5.830 \cdot 10^{-7}
$$

Vad är sannolikheten att det är vinst på **minst** $$10$$ stycken lotter?

$$
\Pr(X > 10) = 1 - \Pr(X \leq 10) = 0.994
$$

{% hint style="info" %}
Om en variabel $$X$$ är binomialfördelad med parametrarna $$n$$ och $$p$$ så gäller det att väntevärdet

$$E(X) = n\cdot p$$ 

och variansen är

$$Var(X) = n\cdot p\cdot (1-p)$$ 
{% endhint %}



