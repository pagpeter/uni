
- https://moodle.hpi.de/mod/assign/view.php?id=28716
- https://hpi.de/friedrich/docs/scripts/24_Mathe1/MengenQuantoren.html
### Mengen

- Menge als "Zusammenfassung von wohlunterscheidbaren Objekten"
- M = $\{1, 2, 4\}$ ; M = $\{1, 2, 3, \dots\}$ (Unendlich)
- Zwei Mengen sind dann identisch, wenn sie die selben Elemente enthalten

>[!CUE] Operationen

- Schnitt: $A \cap B$  (Elemente die in A und in B sind)
- Vereinigung: $A \cup B$ (Elemente die in A oder B sind)
- Differenz: $A \setminus B$ (Elemente in A, die nicht in B sind)
- Symmetrische Differenz: $A \; \Delta \; B$ (Elemente in A oder B, aber nicht in beiden)

- Kardinalität: $|A| = n$ (Menge der Elemente in A, nicht definiert bei unendlichen Längen)

- Allquantor: $\forall x \in M: A(x)$            Für alle Elemente x von M gilt A(x)
- Existenzquantor: $\exists x \in M: A(x)$  Für ein oder mehr Element x von M gilt A(x)

>[!CUE] Beispiel

- Die Aussage “Für alle reellen Zahlen $a,b$ und alle positiven reellen Zahlen x gilt, falls $a≤b$, so ist $a⋅x≤b⋅x$.”
- $\forall a \in \mathbb{R} \; \forall b \in \mathbb{R} \; \forall x \in \mathbb{R}_+: a \leq b \Rightarrow a \cdot x \leq b \cdot x.$
- Ist eine Menge leer, so ist der Allquantor immer wahr und der Existenzquantor immer falsch.

>[!CUE] Scope

- Scope wie in der Programmierung - Bereich, wo Variablen nutzbar sind
- Gültige Aussage: $\varphi \wedge \forall x \in M: A(x)$
- Ungültige Aussage: $A(x) \wedge \forall x \in M: \varphi$ ($x$ ist in dem scope von $A(x)$ noch nicht definiert)
- Gültige Aussage: “Sei $x∈R$. Nun gilt $x^2≥0$. Außerdem ist $x^4≥0$.” (*Sei* definiert quasi globale Variablen)
- Ungültige Aussage: Für alle x∈R gilt $x2≥0$. Außerdem ist $x4≥0$.”

>[!CUE] Formalisieren

- Dies müssen wir nun formalisieren
- 