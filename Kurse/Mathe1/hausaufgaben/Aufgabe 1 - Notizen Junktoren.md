> [!NOTE]
> **Definition - Atomare logische Aussagen**

- Aussagen, die entweder wahr oder falsch sind (z. B. $1 \ne 2$ ; $5 > 6$)
- Dabei egal, ob diese bekannt oder nicht ist (z. B. "Es gibt Aliens") 

 - Diese Bestandteile können wir mithilfe von **Junktoren** zu komplexeren Aussagen verbinden

> [!CUE]
> **Definition - Junktoren**

- Es gibt binäre und unäre Junktoren 
	- Binäre Junktoren verknüpfen zwei Aussagen
	- Unäre Junktoren wirken nur auf eine Aussagen

| Junktor               | Beschreibung             | Name        | Latex           | Typ   |
| --------------------- | ------------------------ | ----------- | --------------- | ----- |
| $\lnot A$             | nicht $A$                | Negation    | \lnot           | Unär  |
| $A\land B$            | $A$ und $B$              | Konjunktion | \land           | Binär |
| $A\lor B$             | $A$ oder $B$             | Disjunktion | \lor            | Binär |
| $A \rightarrow B$     | Falls $A$, dann $B$      | Implikation | \rightarrow     | Binär |
| $A \leftrightarrow B$ | $A$ genau dann, wenn $B$ | Äquivalenz  | \leftrightarrow | Binär |
- Beim Verbinden können Klammern benutzt werden, für die richtige Operatorenreihenfolge und für die Lesbarkeit

<div style="page-break-after: always;"></div>

> [!CUE] 
> ** Beispiel - Einsatz von Junktoren**

- Beispiel für Verbinden: $(x > 0 \land a \geq b) \Rightarrow a \cdot x \leq b \cdot x$
	- Beschreibung: Falls $x$ positiv ist und $a \leq b$, so ist $a \cdot x \leq b \cdot x$

- Mihilfe der Junktoren können wir eine Wahrheitswertetabelle anlegen.

>[!col]
>
| $A$   | $\lnot A$ |
| --- | --------- |
| $w$ | $f$       |
| $f$ | $w$       |
>
>| $A$   | $B$   | $A\land B$ | $A\lor B$ | $A \rightarrow B$ | $A \leftrightarrow B$ |
| --- | --- | ---------- | --------- | ----------------- | --------------------- |
| $w$ | $w$ | $w$        | $w$       | $w$               | $w$                   |
| $w$ | $f$ | $f$        | $w$       | $f$               | $f$                   |
| $f$ | $w$ | $f$        | $w$       | $w$               | $f$                   |
| $f$ | $f$ | $f$        | $f$       | $w$               | $w$                   |

- Weitere Junktoren, die manchmal benutzt werden, sind z. B. 
	- **NAND**: Not-And: $\lnot(A\land B)$
	- **XOR** $\oplus$: Not-And: $(A\land B)\lor\lnot(A\land B)$

> [!CUE] 
> *Tautologie*: Aussage, die unabhängig von dem Wahrheitsgehalt ihrer Teilaussagen wahr ist
> *Kontradiktion*: Aussage, die unabhängig von dem Wahrheitsgehalt ihrer Teilaussagen falsch ist


<div style="page-break-after: always;"></div>

**Ambivalenz bei Junktoren**
- In der Umgangssprache sind Junktoren wie **oder** ambivalent, sie können einschließend oder ausschließend genutzt werden
- Mathematisch sind Junktoren nicht ambivalent sondern exakt 

**Beispiele: Formalisieren von logischen Aussagen**
1. “Wenn es regnet, dann ist die Straße nass.”: 
$R$ sei die atomare logische Aussage “es regnet”; “$N$” sei die atomare logische Aussage “die Straße ist nass”. Wir können nun die Aussage formalisieren zu $R→N$.

2. “Die Straße ist dann, und nur dann, nass, wenn es regnet.” 
$R$ sei die atomare logische Aussage “es regnet”; “$N$” sei die atomare logische Aussage “die Straße ist nass”. Wir können nun die Aussage formalisieren zu $R↔N$

3. “Wenn es morgen regnet, dann gehe ich in's Kino, ansonsten spiele ich Volleyball.”: 
$R$ sei die atomare logische Aussage “morgen regnet es”; “$K$” sei die atomare logische Aussage “morgen gehe ich in's Kino”; $V$ sei die atomare logische Aussage “ich spiele morgen Volleyball”. Wir können nun die Aussage formalisieren zu $(R→K)∧(¬R→V)$
## Aussagenumformungen

- Mithilfe eines $=$ können wir zeigen, das zwei Terme den selben Wert haben. 
- Das können wir nutzen, um Terme umzuformen: $2(x+3)=2x+6$
- Würden wir das selbe für logische Aussagen nutzen, würde es zu Verwirrung führen
- Deshalb wird für logische Aussagen das Zeichen $≡$ benutzt.
- Diese beiden Aussagen sind dann **logisch äquivalent**

> [!CUE] 
> *Logische Äquivalenz und Termäquivalenz*
> $x>0∨x=0≡x=0∨x>0$
> Für Terme benutzen wir $=$, für Logik $\equiv$ (Latex: \equiv)

Logische Aussagen können wir also auch umformen. Dafür gibt es ein paar Regeln:

| Name                         | Symbol                                            |
| ---------------------------- | ------------------------------------------------- |
| Doppelte Negation            | $\lnot \lnot A \equiv A$                          |
| $\lor-$Idempotenz            | $A \lor A \equiv A$                               |
| $\land-$Idempotenz           | $A \land A \equiv A$                              |
| Kommutativgesetz für $\lor$  | $A \lor B \equiv B \lor A$                        |
| Kommutativgesetz für $\land$ | $A \land B \equiv B \land A$                      |
| Assoziativgesetz für $\lor$  | $(A \lor B) \lor C \equiv A \lor  (B \lor C)$     |
| Assoziativgesetz für $\land$ | $(A \land B) \land C \equiv A \land  (B \land C)$ |
| De-morgan'sche Regel I       | $\lnot(A \lor B) \equiv \lnot A \land \lnot B$    |
| De-morgan'sche Regel II      | $\lnot(A \land B) \equiv \lnot A \lor \lnot B$    |
| Distributivgesetz I          | $(A∧B)∨C≡(A∨C)∧(B∨C)$                             |
| Distributivgesetz II         | $(A∨B)∧C≡(A∧C)∨(B∧C)$                             |
| Implikation                  | $A→B≡¬A∨B$                                        |
| Kontraposition               | $A→B≡(¬B)→(¬A)$                                   |
| Äquivalenz                   | $A↔B≡(A→B)∧(B→A)$                                 |

> [!NOTE] 
> *Beispiel-Beweise für Regeln*

> [!col]
> 
| $A$   | $B$   | $A \to B$ | $\lnot A\lor  B$ |
| --- | --- | --------- | ---------------- |
| $w$ | $w$ | $w$       | $f$ $w$          |
| $w$ | $f$ | $f$       | $f$ $f$          |
| $f$ | $w$ | $w$       | $w$ $w$          |
| $f$ | $f$ | $w$       | $w$ $w$          |
> **Implikation**
Da in Spalte 3 und 4b die selben Werte stehen, ist die logische Äquivalenz bewiesen
> 
| $A$   | $B$   | $\lnot (A\lor B)$ | $\lnot A\land \lnot B$ |
| --- | --- | ----------------- | ---------------------- |
| $w$ | $w$ | $f$ $w$           | $f$ $f$ $f$            |
| $w$ | $f$ | $f$ $w$           | $f$ $f$ $w$            |
| $f$ | $w$ | $f$ $w$           | $w$ $f$ $f$            |
| $f$ | $f$ | $w$ $f$           | $w$ $w$ $w$            |
>
> **De-morgansche Regel I**
> Da in Spalte 3 und 4b die selben Werte stehen, ist die Richtigkeit der De-morgansche Regel I bewiesen
<div style="page-break-after: always;"></div>

>[!NOTE] 
>**Rechenregeln**
Sei $A$ eine Aussage, gelten folgende Regeln:
 > 
| Name                                  | Definition           | Code Äquivalent     |
| ------------------------------------- | -------------------- | ------------------- |
| $\lor$ Neutralität von $f$            | $A \lor f \equiv A$  | a \|\| false == a   |
| $\land$ Neutralität von $w$           | $A \land f \equiv A$ | a && false == a     |
| $\lor$ Dominanz von $w$               | $A \land w = w$      | a \|\| true == true |
| $\land$ Dominanz von $f$              | $A∧f≡f$              | a && false == false |
| Satz vom ausgeschlossenen Widerspruch | $A∧¬A≡f$             | a && !a == false    |
| Satz vom ausgeschlossenen Dritten     | $A∨¬A≡w$             | a \|\| !a == true   |

Komplexere logischen Aussagen können wir Umformen, um bereits bewiesene Aussagen zu erhalten, so dass keine neue Wertetabelle angelegt werden muss.

$$
\begin{align}
((A \land B) \land C) \land D &\equiv ((A \land B) \lor D) \lor (C \land D) && | \text{ Distributionsgesetz 1} \\
&\equiv ((A \lor D) \land (B \lor D)) \land (C \lor D) && | \text{ Distributionsgesetz 1}
\end{align}
$$

>[!NOTE] 
>[Konjunktive Normalenform (KNF)](https://de.wikipedia.org/wiki/Konjunktive_Normalform)
> Jede Formel der Aussagenlogik lässt sich in die konjunktive Normalenform umwandeln.
> Diese ist nicht unbedingt die kleinste Darstellung, sondern bloß eine Standardisierte Schreibweise.
> 
>  Beispiel für KNF:
> - $C \land \lnot A$ 
> - $A$
>   
> Beispiele für nicht-KNF
> 
> - $\lnot(A \land B)$

Mithilfe der Umformungsregeln und den Rechenregeln können wir logische Aussagen in die KNF überführen.
Ein Beispiel:
$$
\begin{align}
	\varphi & \equiv \neg [ (A \rightarrow B) \rightarrow ((B \rightarrow C) \rightarrow (A \rightarrow C))]\\
	 & \equiv \neg [ (\neg A \vee B) \rightarrow ((\neg B \vee C) \rightarrow (\neg A \vee C)) ] && \mbox{| Def. $\rightarrow$}\\
	 & \equiv \neg [\neg(\neg A \vee B) \vee (\neg(\neg B \vee C) \vee (\neg A \vee C)) ] && \mbox{| Def. $\rightarrow$}\\
	 & \equiv (\neg A \vee B) \wedge \neg (\neg(\neg B \vee C) \vee (\neg A \vee C)) && \mbox{| De-Morgan, Dop.Neg.}\\
	 & \equiv (\neg A \vee B) \wedge (\neg B \vee C) \wedge \neg (\neg A \vee C) && \mbox{| De-Morgan, Dop.Neg.}\\
	 & \equiv (\neg A \vee B) \wedge (\neg B \vee C) \wedge  A \wedge \neg C. && \mbox{| De-Morgan, Dop.Neg.}

\end{align}
$$
Die letzte Zeile ist logisch äquivalent zur ersten, allerdings in KNF.

>[!NOTE] 
>**Hauptsatz zur Junktorvollständigkeit**
> Mithilfe von drei verschiedenen Junktoren (paaren) können wir alle anderen Junktoren darstellen.
> 1. $\lnot, \land$
> 2.  $\lnot, \lor$
> 3. NAND
>    
> D. h. Wir können mit einem einzigen Junktor (NAND) alle anderen Junktoren durch schlaues kombinieren darstellen. Dies ist sehr praktisch für die Architektur von Computerchips.

---

> [!TIP] 
> **Zusammenfassung**
> - Junktoren verbinden atomare logische Aussagen miteinander.
> - Wir können logische Aussagen mit ihnen also gut formalisieren.
> - Es gibt unäre und binäre Junktoren, ähnlich wie Operatoren in Programmiersprachen.
> - Mithilfe weniger Junktoren (oder sogar nur NAND) können wir viele weitere Junktoren bilden.
> - Aussagen können umgeformt werden, um in die KNF (Konjunktive Normalform) gebracht zu werden, oder um Aussagen einfacher beweisen zu können.
> - Dafür gibt es zahlreiche Rechengesetze und Umformungsregeln