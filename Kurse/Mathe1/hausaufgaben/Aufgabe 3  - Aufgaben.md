# Hausaufgabe Woche 2 - Peter Pagenstedt

*Tutorium: Kleiner Prinz, Wintersemester 2024/25*
## 1. Harry, fahr schon mal den Wagen vor!

Kommissar Stefan und Inspektor Harry haben die drei Verdächtigen Langfinger-Ede, Nepper-Johnny und Diedrich-Dieter vorläufig festgenommen. Inspektor Harry fasst die Fakten zusammen:  
(1) Niemand außer Langfinger-Ede, Nepper-Johnny oder Diedrich-Dieter war an den Verbrechen beteiligt  
(2) Wenn Langfinger-Ede schuldig ist und Nepper-Johnny unschuldig, so muss Diedrich-Dieter schuldig sein.  
(3) Diedrich-Dieter arbeitet niemals allein.  
(4) Langfinger-Ede arbeitet niemals mit Diedrich-Dieter zusammen.

Gibt es einen oder mehrere Verdächtige, die sicher schuldig sind und von Kommissar Stefan auf der Stelle eingesperrt werden können? Muss Kommissar Stefan einen der Verdächtigen freilassen, weil er sicher unschuldig ist? FORMALISIERE ZUNÄCHST ALLE AUSSAGEN!

**Lösung**

L (Langfinger-Ede)
N (Nepper-Johnny)
D (Dietrich-Dieter)

**Wahrheiten**:
(1) $L \lor N \lor D$
(2) $L \land \lnot N \to D$
(3) $D \to N \lor L$
(4) $L \to \lnot D$ 

Die Wahrheiten sind quasi mit UND miteinander verknüpft. Wenn eine also falsch ist, müssen wir die anderen nicht mehr ausrechnen.

| L   | N   | D   | $L \lor N \lor D$ | $L \land \lnot N \to D$ | $D \to N \lor L$ | $L \rightarrow \lnot D$ | möglich? |
| --- | --- | --- | ----------------- | ----------------------- | ---------------- | ----------------------- | -------- |
| 1   | 1   | 1   | 1                 |                         | 1                | 0                       | 0        |
| 1   | 1   | 0   | 1                 |                         | 1                |                         |          |
| 1   | 0   | 1   | 1                 |                         | 1                | 0                       | 0        |
| 1   | 0   | 0   | 1                 | 0                       | 1                |                         | 0        |
| 0   | 1   | 1   | 1                 |                         | 1                |                         |          |
| 0   | 1   | 0   | 1                 |                         | 1                |                         |          |
| 0   | 0   | 1   | 1                 |                         | 0                |                         | 0        |
| 0   | 0   | 0   | 0                 |                         | 1                |                         | 0        |
-> N ist auf jeden fall ein Täter
-> Bei den anderen ist es nicht klar

<div style="page-break-after: always;"></div>

## 2. KNF 2

Forme die folgende Aussage äquivalent in KNF um.
$$
2 \mbox{ teilt }x \wedge 3 \mbox{ teilt }x \rightarrow 6 \mbox{ teilt }x.
$$

**Lösung**

Die KNF besteht immer aus einem oder mehr Maxtermen, die mit $\land$ miteinander verknüpft sind. Die Maxterme bestehen aus allen Variablen, und sind mit $\lor$ miteinander verknüpft. Einzelne Variablen können negiert werden.

1. Wir wissen das $A \to B \equiv \lnot A \lor B$.
2. Wir können also umstellen zu $\lnot (2 \text{ teilt } x \land 3 \text{ teilt } x) \lor (6 \text{ teilt } x)$.
3. In der KNF wollen wir keine Negation von Klammern, sondern nur von Variablen.
4. Da können wir die zweite De'Morgansche Regel nehmen: $\lnot(A \land B) \equiv \lnot A \lor \lnot B$
5. Nach der Umformumg kommen wir zu dem Ergebnis
$$(\lnot(2 \text{ teilt }x) \lor \lnot (3 \text{ teilt }x) \lor (6 \text{ teilt } x))$$
6. Um es schöner auszudrücken, könnten wir den einzelnen Aussagen auch Variablen zuweisen: $A = 2 \text{ teilt }x$ ;  $B = 3 \text{ teilt }x$ ;  $C = 6 \text{ teilt }x$
$$
(\lnot A \lor \lnot B  \lor C)
$$
Unsere Lösung besteht nur aus einem einzelnen Maxterm.