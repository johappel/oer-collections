# Anforderungssituationen - Lernarrangement-Builder

Studierende müssen aus begrenzten Karten (Ressourcen) ein optimales Lernarrangement zusammenstellen, das eine Anforderungssituation adressiert. Dabei stehen ständige Zielkonflikke an: Tiefe vs. Alltagsnähe, Schülerorientierung vs. theologische Substanz, Zeit vs. Motivation usw.

**Genre**: Deck-Builder & Budget-Manager

<img width="1436" height="753" alt="grafik" src="https://github.com/user-attachments/assets/99480442-0473-443e-8cf9-14b381a4080a" />


## 🎮 Spielablauf

- Zufällige Anforderungssituation wird geladen (Tod des Menschen, Glaube & Wissenschaft, Identitätskonflikt …).
- Ressourcen-Karten mit Aufwenden für die Errbeitung von Kompetenzen, Inhalten, Methoden und Arragements (Settings).

🧩 Spiel-Prinzip im Überblick

| Ressource	| Beispiel-Karte| Was sie liefert | 
| --------- | ------------- | --------------- | 
| Kompetenz	| „Empathie entwickeln“ | → 2 Punkte empathie, 1 Punkt religion| 
| Inhalt	| „Leid & Trost (Bibelstellen)“ | → 2 Punkte leid, 1 Punkt rituale| 
| Methode	| „Gesprächskreis“ | → 1 Punkt gespraech, 1 Punkt reflexion| 
| Setting	| „Doppelstunde“ | → 2 Punkte zeit| 

Das Budget von 100 zwingt zu Priorisierung und Kombination – ganz so, wie es Lehrkräfte täglich tun.


**🎯 So passt du die Daten für deine Studies an:**


Suche im Quelltext nach "Daten" und dann Editiere die folgenden beiden Abschnitte:

**Situationsanforderungen:**
```js
const situations=[
  {
    title:"Der Bruder einet Schülerin verliert nach dem Tod seiner Freundin den Glauben an Gott.",
    needs:{kompetenz:{empathie:2,religion:1},inhalt:{leid:2,rituale:1},methode:{gespraech:1,ritual:1},setting:{zeit:1}}
  },
  {
    title:"Die Klasse diskutiert, ob Glaube und Wissenschaft sich widersprechen.",
    needs:{kompetenz:{argumentation:2,offenheit:1},inhalt:{schoepfung:2,wissenschaft:1},methode:{dialog:2,forSchung:1},setting:{raum:1}}
  },
  {
    title:"Eine Schülerin möchte wissen, warum sie sich als Christin outen soll.",
    needs:{kompetenz:{identitaet:2,courage:1},inhalt:{bekenntnis:1,gesellschaft:2},methode:{rollenspiel:1,reflexion:1},setting:{gruppen:1}}
  }
];
```

**Sektoren (Kompetenzen, Inhaltsbereiche, Methoden, Settings)**:
```js
const sectors={
  kompetenz:[
    {name:"Empathie entwickeln",cost:15,points:{empathie:2,religion:1}},
    {name:"Argumentation stärken",cost:20,points:{argumentation:2,offenheit:1}},
    {name:"Selbstwirksamkeit fördern",cost:18,points:{identitaet:2,courage:1}}
  ],
  inhalt:[
    {name:"Leid & Trost (Bibelstellen)",cost:12,points:{leid:2,rituale:1}},
    {name:"Schöpfung & Naturwissenschaften",cost:15,points:{schoepfung:2,wissenschaft:1}},
    {name:"Bekenntnis in der Öffentlichkeit",cost:14,points:{bekenntnis:1,gesellschaft:2}}
  ],
  methode:[
    {name:"Theologisieren",cost:10,points:{gespraech:1,reflexion:1}},
    {name:"Wissenschaftsdialog",cost:15,points:{dialog:2,forSchung:1}},
    {name:"Rollenspiel „Coming-out“",cost:12,points:{rollenspiel:1,identitaet:1}}
  ],
  setting:[
    {name:"Doppelstunde",cost:10,points:{zeit:2}},
    {name:"Partnerarbeit",cost:8,points:{lernaktivität:1,gruppen:1}},
    {name:"Projekttag",cost:20,points:{zeit:2,raum:1}}
  ]
};
```
