# Format des données (un fichier par siman)

```js
HALAKHA.addSiman({
  id: "202",                 // numéro, sert de clé
  siman: "ר״ב",               // affichage
  title: "ברכת פירות האילן",
  source: "סיכום ר״ב מלא",     // document d'origine
  seifim: [{
    seif: "א׳", title: "…",
    topics: [{
      title: "…",              // nom court du sujet
      question: "…",           // niveau 1 : question générique
      gemara: {                // niveaux 2-3 (facultatif)
        ref: "ברכות לה.",       //   référence
        text: ["…"]            //   texte / résumé de la sugya
      },
      rishonim:  [{ who: "רש״י", text: "…" }],   // niveau 4 (facultatif)
      acharonim: [{ who: "מג״א", text: "…" }],   // niveau 5 (facultatif)
      psak: {                  // niveau 6
        sa: ["…"], rama: ["…"],     // שו״ע / רמ״א
        mb: ["…"], bh: ["…"], shtz: ["…"]  // משנ״ב / ביאה״ל / שעה״צ
      },
      notes: ["…"],            // facultatif : remarques personnelles (ולענ״ד)
      table: { cols: [], rows: [[]] }  // facultatif : tableau récapitulatif
    }]
  }]
});
```

Un niveau absent est simplement sauté pendant la révision.
