# **Avanceret CSS faget - Del 1**


### **Node, NPM, Webpack, Præprocessorer (LESS, SASS, SCSS, osv)**

*(NPM står for Node Package Manager)*

* Download og installér Node.js:<br>
[WUHF01 / Node](/Blandet/Node.md)

* Clone følgende repository i en ny mappe på harddisken:<br>
https://github.com/NielsHarbo/Webpack-med-Babel-Sass-og-BEMSkel

* Åbn `dist/index.html` i browseren, som viser en vejledning.

* Opret en ny test mappe på harddisken kaldet f.eks. "test-webpack".

* Følg ovennævnte vejledning, der viser hvordan du arbejder med Webpack, Babel, præprocessorer (LESS, SASS, SCSS, osv).

**Hvis det går galt**, kan du altid bare oprette en **ny test mappe** og følge vejledningen fra toppen igen.
<br><br><br>



---



### **GitHub: Node og gitignore**

Når du arbejder med Node projekter, så får du en mappe som hedder **"node_modules"**. Mappen indeholder moduler, som projektet har brug for, som f.eks. præprocessorer (så man bl.a. kan bruge LESS, SASS, SCSS, osv), MySQL database interface, og lignende.

Mappen indeholder typisk flere tusinde elementer (mapper og filer), som vi IKKE ønsker at pushe til GitHub. Derfor er det vigtigt, at du altid husker at lave en **gitignore til Node**, når du opretter repositories på GitHub.

Du skal nu teste om du kan få den til at ignorere "node_modules" mappen, når du pusher til GitHub.

* På GitHub, opret et nyt repository: "test-gitignore"

* Clone dette repository til din harddisk.

* Åbn mappen i VSCode.

* Åbn terminalen (se ovenstående instruktioner vedrørende terminalen)

* Skriv: `npm init -y`<br>
Dette skulle gerne oprette en `package.json` fil i mappen og ikke andet.

* Skriv: `npm install money --save`<br>
Dette er et modul, som bl.a. kan gøre det nemt at konvertere fra én valuta til en anden. Vi skal ikke rigtig bruge det til noget. Vi har bare brug for et tilfældigt modul.

* Højre-klik på `package.json` i VSCode og vælg **"Reveal in Explorer"** (i **Windows**) eller "Reveal in Finder" (på **Mac**).

* Du skulle gerne se mappen **"node_modules"**.<br>
Få dit operativsystem til at tjekke hvor mange undermapper og filer den indeholder. I Windows kan man **højre-klikke** på mappen og vælge **"Egenskaber"** (Properties).<br>
Efter at have installeret `money` modulet, siger min 5 filer og 1 mappe, hvilket slet ikke er slemt.

* Skriv: `npm install webpack webpack-cli --save`<br>
Tjek antallet af undermapper og filer igen. Min siger nu ca. **3400 filer** og **700 mapper**.

* Åbn GitHub Desktop, commit og push til GitHub.

* Åbn dit repository på GitHub's hjemmeside, sørg for at siden er genindlæst efter din Commit og bekræft, at **"node_modules"** mappen IKKE ligger på GitHub. <br>Hvis du kan se mappen på GitHub, så mangler du højst sandsynligt din **gitignore**.<br>
Det er muligt, at kopiere en gitignore fil fra et tidligere projekt.
<br><br><br>



---



### **Skriv noter!**

Husk at skrive en masse noter. Opsætning af websites er jo ikke noget man gør så ofte på uddannelsen, hvilket gør det svært at huske proceduren.
<br><br><br>



---



### **LESS, SASS, SCSS**

LESS, SASS og SCSS har mange af de samme features. Der er dog naturligvis forskel på syntaksen.

**LESS** *(Leaner Style Sheets)* har intet med de to andre at gøre. Filtypen er typisk `.less`

**SASS** *(Syntactically Awesome Style Sheets)* er den **første udgave** af SASS. Filtypen er typisk `.sass`

**SCSS** (Sassy CSS) er **anden udgave** af SASS. Filtypen er typisk `.scss`

Det betyder ikke så meget, hvilken én man starter med at lære, men vi er nødt til at vælge én af dem, når vi underviser.

**Vi har valgt SCSS (Sassy CSS).**
<br><br><br>



---



### **SCSS** *(Sassy CSS)*

**Inden du går i gang**

* Du skal lige være opmærksom på, at **når nogen siger "SASS"**, er der enten tale om **SASS syntaksen** eller **SCSS syntaksen** (forskellen er forholdsvis lille).

* Du skal også lige huske, at LESS og SASS endnu ikke er understøttede i browserne. **Browserne kan kun afvikle almindelig CSS**. Du skal derfor sørge for at bruge en **præprocessor**, som konverterer SASS til CSS.

**Video-tutorials**

* Jeg har forsøgt at finde nogle gode, korte **videoer**, som giver et hurtigt indblik i hvordan SASS fungerer, men i det fleste videoer jeg kunne finde, bruger de en masse tid i starten på at installere præprocessorer og de ævler løs om hvorfor man skulle bruge LESS, SASS, osv. **Hvis du finder nogle gode videoer**, så del dem venligst med os og holdkammeraterne.

> Update:<br>
> * Nanna har fundet denne video:<br>
**"SASS Tutorial #1 - What is SASS?"** af The Net Ninja<br>
https://www.youtube.com/watch?v=St5B7hnMLjg

**Tekst-tutorials / dokumentation**

Nedenstående sider demonstrerer hurtigt og simpelt de muligheder man har i SASS. <br>Jeg vil råde dig til at **starte med at lære om Nesting og Variables**.

* **SASS Basics**  (officielle side)<br>
https://sass-lang.com/guide

* **Farve-manipulering**<br>
https://thoughtbot.com/blog/controlling-color-with-sass-color-functions

* **Functions**<br>
*(Rul ned til afsnittet "Functions")*<br>
https://tutorialzine.com/2016/01/learn-sass-in-15-minutes
<br><br><br>



---



### **Lav et lille website**

Lav et lille website, der bruger **Webpack** til at **kompilere JS og SCSS**, så du er sikker på, hvordan det hele hænger sammen.

**Tag gerne noget du allerede har lavet før** og kopiér koden til de steder i Webpack projektet, hvor du mener den skal hen.

> *Når jeg siger "Webpack projekt", mener jeg blot et projekt, som bruger Webpack, JS/CSS præprocessorer, osv.*

Hvis du har fået lavet dig en **webpack-skabelon**, så pas på det ikke er dén, du får indsat koden i. Hold skabelonen så simpel som muligt.

* Husk at den kun kan **kompilere koden**, hvis du har sat den til at **holde øje med ændringer (watch)** ved at skrive `npm run develop`

* Læg mærke til hvilken **JS fil**, der indlæses i `index.html`<br>
Det er `bundle.js` og ikke `index.js`, hvilket må betyde, at den kode du skriver i `index.js` bliver automatisk indsat i `bundle.js`, hver gang du gemmer.
