
- Umkehrung des Ableitens

**Bestimmtes Integral**: Integrationsgrenzen $\int$
**Unbestimmtes Integral:** Keine Integrationsgrenzen $\int^a_{a}$

## Bildung der Stammfunktion

#### Unbestimmtes Integral (Keine Integrationsgrenzen)

- Eine Funktion hat unendlich viele Stammfunktionen

$$
\begin{align}
f(x) &= 2x \\
F(x) &= x^2 + 2 \\
F(x) &= x^2 - 3 
\end{align}
$$

$$
\begin{align}
\int 2x \text{ } dx = x^2 + c \\
\text{Oder allgemein} \\
\int f(x)dx = F(x) +c
\end{align}
$$
#### Unbestimmtes Integral (Mit Integrationsgrenzen)


$$
\int \limits_b^a fx(dx)
$$

- $[a,b]$: Integrationsbereich
- Es kommt eine konkrete Zahl hinaus
- Dies ist die Fläche, die die Funktion mit der X-Achse einschließt 


$$
\begin{align}
\int \limits^5_0 -\frac{1}{2}x+4dx & \\
F(x) &= -\frac{1}{4}x^2+4x \\
\int \limits^5_0  -\frac{1}{2}x+4dx &= \left[-\frac{1}{4}x^2+4x \right]^5_{0} \\
&=\left( -\frac{1}{4} \cdot 5^2 +4 \cdot 5 \right) \\
&-\left( -\frac{1}{4} \cdot 0^2 +4 \cdot 0 \right)  \\
&=13.75
\end{align}
$$

1. Stammfunktion bilden
2. In eckige klammern hinter Integral schreiben
3. Obere und unteren Integrand berechnen
4. voneinander abziehen

## Integrationsregeln

#### Potenzregel

$$
\int x^2dx = \frac{1}{3}x^3+c
$$

#### Faktorregel

$$
\int 2x^2dx = 2 \cdot \int x^2 dx = 2 \cdot \left(\frac{1}{3}x^3+c \right)
$$

#### Summenregel

$$
\int (1+x^3)dx =  \int 1d x + \int x^3dx
$$

#### Differenzregel


$$
\int (2-x^3)dx =  \int 2 dx - \int x^3dx
$$

### Specials

$$
\begin{align}
\int e^x dx &= e^x+c \\
\int \ln (x)dx &= x \cdot \ln(x) -x +c
\end{align}
$$

## Substitution



## Partielle Integration

![[Bildschirmfoto 2024-09-24 um 23.40.53.png]]![[Bildschirmfoto 2024-09-24 um 23.43.33.png]]