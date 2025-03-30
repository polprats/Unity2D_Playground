# Unity2D_Playground

# Unity2D Playground 🎮

**Unity2D Playground** és un repositori dedicat a la pràctica i aprenentatge del desenvolupament de videojocs amb Unity en 2D. Conté múltiples subprojectes independents, estructurats per ordre numèric segons la seva complexitat o ordre d'aprenentatge recomanat.

Cada subprojecte està ubicat en una carpeta pròpia, fent més senzilla la navegació i l'aprenentatge progressiu.

---

## 📁 Estructura del Repositori

L'estructura general del repositori és aquesta:

```
Unity2D_Playground/
├── 01-HelloWorld/
├── 02-PlayerMovement/
├── 03-EnemyAI/
├── .gitignore
└── README.md
```

Cada carpeta numerada conté un subprojecte de Unity completament independent.

---

## 🚀 Com treballar amb aquest repositori

Pots utilitzar aquest repositori de diferents maneres segons les teves necessitats:

### 1. Descarregar el repositori complet

Si no tens problemes d'espai i vols tenir-ho tot disponible, fes un clone complet:

```bash
git clone https://github.com/polprats/Unity2D_Playground.git
cd Unity2D_Playground
```

### 2. Descarregar només un subprojecte específic (Sparse Checkout)

Si només vols treballar amb un sol subprojecte, utilitza aquesta opció per descarregar exclusivament el contingut que necessites. Per exemple, descarregarem només el projecte `01-HelloWorld`:

```bash
git clone --filter=blob:none --no-checkout https://github.com/polprats/Unity2D_Playground.git
cd Unity2D_Playground

git sparse-checkout init --cone
git sparse-checkout set 01-HelloWorld .gitignore README.md
git checkout main
```

Això descarregarà únicament el subprojecte específic indicat (`01-HelloWorld`) i els fitxers essencials (`.gitignore`, `README.md`).

**Per afegir més subprojectes més tard:**

```bash
git sparse-checkout add 02-PlayerMovement
```

### 3. Començar un nou subprojecte

Per crear un nou subprojecte:

- Crea una nova carpeta seguint la seqüència numèrica existent (`04-MyNewProject`).
- Desenvolupa-hi el projecte directament amb Unity.
- Els fitxers generats automàticament i no necessaris per compartir seran ignorats gràcies al `.gitignore` global.

---

## ⚙️ Com treballar habitualment amb Git

### Veure l'estat actual dels canvis

```bash
git status
```

### Afegir fitxers per fer commit

- **Afegir tots els fitxers modificats:**
```bash
git add .
```

- **Afegir només fitxers específics:**
```bash
git add nom_del_fitxer
```

### Fer un commit

```bash
git commit -m "Missatge descriptiu dels canvis fets"
```

### Pujar els canvis al repositori remot (GitHub)

```bash
git push origin main
```

---

## 🔧 Com està fet el `.gitignore` global

Aquest repositori conté un sol fitxer `.gitignore` a l'arrel que gestiona tots els subprojectes, basat en el `.gitignore` oficial recomanat per Unity:

- [Unity.gitignore oficial](https://github.com/github/gitignore/blob/main/Unity.gitignore)

### Què ignora aquest fitxer?

- Carpetes de Unity que no calen versionar (ex: `Library/`, `Temp/`, `Obj/`, `Build/`, `Logs/`)
- Fitxers temporals generats per IDEs (Visual Studio, Rider, VS Code)
- Fitxers específics de sistema (ex: `.DS_Store`, `Thumbs.db`)

Gràcies als patrons utilitzats (`**/`), aquest `.gitignore` aplica automàticament a qualsevol subprojecte.

---

## ✅ Bones pràctiques

- Realitza **commits freqüents i clars**.
- Treballa amb **branques sep



Modificar el .gitignore per a que només tingui el .gitignore i el README.md.

Descarregar el repositori amb git sparse-checkout init --cone i git sparse-checkout set .gitignore README.md i git checkout main.

A partir d'aquí, només es descarregaran els fitxers que indiquis explícitament al .gitignore i el README.md.
📌 1. Inicialitzar Sparse Checkout
Executa aquesta comanda:

bash
Copy
Edit
git sparse-checkout init --cone
Què fa aquesta comanda?

Activa la característica "Sparse Checkout" en mode "cone".

"Sparse Checkout" permet que descarreguis només algunes carpetes del repositori en lloc de totes.

El mode --cone indica que vols seleccionar carpetes completes de manera senzilla, en lloc de fitxers específics o patrons complexos.

A partir d'aquest punt, Git està preparat per descarregar només el que li indiquis explícitament, i no pas tot el contingut del repositori.


📌 2. Seleccionar fitxers o carpetes específiques
Ara executa això per descarregar el .gitignore i el README.md:

bash
Copy
Edit
git sparse-checkout set .gitignore README.md
Què fa aquesta comanda?

Li estàs dient explícitament a Git que només vols aquests dos fitxers al teu directori local.

Git encara no els ha descarregat físicament; només sap que els haurà de descarregar quan facis un checkout (ve al següent pas).

Ara, executa la següent comanda per fer efectiva aquesta selecció:

bash
Copy
Edit
git checkout main
Què fa aquesta comanda?

Ara sí, descarrega físicament del servidor els fitxers especificats (.gitignore i README.md) i els col·loca al teu directori local.

El teu directori ja no està buit; hi apareixen els fitxers que has indicat.

📌 5. Com treballar d’ara en endavant?
Per descarregar nous subprojectes més endavant (per exemple, la carpeta 01-HelloWorld):

bash
Copy
Edit
git sparse-checkout add 01-HelloWorld
Afegeix una nova carpeta específica a la teva selecció local.

Descarrega immediatament aquesta carpeta.

Quan vulguis actualitzar el que tinguis localment del servidor:

bash
Copy
Edit
git pull origin main
Actualitza només els fitxers que has seleccionat explícitament, sense descarregar res addicional.

Per comprovar què tens seleccionat actualment:

bash
Copy
Edit
git sparse-checkout list

✅ Resum ràpid de conceptes importants:
Comanda	Què fa exactament
git sparse-checkout init --cone	Activa sparse checkout per descarregar només carpetes específiques del repositori
git sparse-checkout set carpetaX fitxerY	Defineix explícitament quines carpetes o fitxers vols descarregar
git sparse-checkout add carpetaNova	Afegeix més carpetes o fitxers a la selecció actual
git sparse-checkout list	Mostra què tens seleccionat per descarregar actualment
git sparse-checkout disable	Desactiva sparse checkout (descarrega-ho tot)


Clonar el repositori complert per treballar amb tots els arxius:

🚩 1. Clonar el repositori complet
Primer, des de zero, obre la terminal al lloc on vulguis tenir el projecte i executa:

bash
Copy
Edit
git clone https://github.com/polprats/Unity2D_Playground.git
cd Unity2D_Playground
Explicació de les comandes:

git clone <url>:
Descarrega tot el contingut del repositori (totes les carpetes i fitxers).

cd Unity2D_Playground:
Entra dins la carpeta del projecte que s'ha creat automàticament.

Ara tens una còpia completa del repositori amb totes les carpetes visibles i descarregades.


🚩 3. Comprovar l’estat del repositori després de fer modificacions
Imagina't que has estat modificant diversos fitxers dins de diferents carpetes (projectes):

bash
Copy
Edit
git status
Què fa això?

Mostra tots els fitxers que has modificat, afegit, eliminat i encara no has fet commit.

Exemple de sortida:

bash
Copy
Edit
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)

	modified:   .gitignore
	modified:   01-HelloWorld/Assets/Scripts/player.cs
	modified:   02-PlayerMovement/Assets/Scenes/MainScene.unity
🚩 4. Afegir els canvis per fer commit
🟢 Opció A: Afegir TOTS els canvis alhora:
bash
Copy
Edit
git add .
Què fa això?

Afegeix automàticament TOTS els fitxers modificats o nous a la zona de preparació ("staging area") per fer commit.

🔵 Opció B: Afegir només fitxers específics:
Si vols controlar exactament què puges al commit, afegeix només fitxers concrets:

bash
Copy
Edit
git add .gitignore
git add 01-HelloWorld/Assets/Scripts/player.cs
Què fa això?

Només els fitxers especificats s'afegiran al següent commit. La resta de canvis quedaran pendents fins que decideixis afegir-los també.

🚩 5. Fer un commit amb els canvis preparats
Quan ja tinguis afegits tots els fitxers que vols al commit, executa:

bash
Copy
Edit
git commit -m "Missatge descriptiu del commit"
Què fa això?

Desa definitivament els canvis que havies preparat amb git add.

El -m indica el missatge descriptiu del que has fet.

Exemple de commit ben fet:

bash
Copy
Edit
git commit -m "Afegit sistema de moviment bàsic al player i actualitzat .gitignore"
🚩 6. Pujar els canvis al servidor remot (GitHub)
Per últim, puja els canvis al servidor GitHub:

bash
Copy
Edit
git push origin main
Què fa això?

Pujarà tots els commits que has fet localment (i encara no havies pujat) a la branca principal main del repositori GitHub.

🚩 7. Treball habitual (resum dels passos típics)
Cada vegada que treballis i facis canvis, el procés normal serà:

bash
Copy
Edit
git status              # veure què has canviat
git add .               # afegir-ho tot (o fitxers específics amb git add fitxerX)
git commit -m "..."     # fer el commit amb missatge
git push origin main    # pujar els canvis a GitHub
⚙️ Resum ràpid dels conceptes importants:
Comanda	Explicació ràpida
git clone <url>	Copia completament el repositori remot al teu ordinador.
git status	Mostra quins fitxers s’han modificat localment.
git add fitxerX	Prepara fitxers específics per fer commit.
git add .	Prepara TOTS els fitxers modificats/nous per fer commit.
git commit -m "..."	Desa definitivament els fitxers preparats amb un missatge descriptiu.
git push origin main	Puja els commits al servidor GitHub a la branca principal.
🎯 Avantatges i inconvenients respecte Sparse Checkout:
Avantatges:

Simplicitat: tens tot el repositori complet.

Més còmode si no et molesta tenir-ho tot descarregat.

Inconvenients:

Ocupa més espai (descarregues tot, encara que no ho necessitis).

Més lent si tens molts subprojectes grans.



Exemple de com pujar els canvis a GitHub d'un subprojecte. 

🎯 Exemple pràctic amb Sparse Checkout
Suposem que vols treballar només amb la carpeta del subprojecte:

01-HelloWorld

🚩 1. Fer un clone mínim sense fitxers
Executa això en una carpeta buida on vulguis treballar:

bash
Copy
Edit
git clone --filter=blob:none --no-checkout https://github.com/polprats/Unity2D_Playground.git
cd Unity2D_Playground
Què passa aquí?

--filter=blob:none: No baixa cap fitxer, només metadades.

--no-checkout: Evita que Git baixi fitxers automàticament.

Ara tens un repositori pràcticament buit, però Git ja sap que existeix tot el contingut remot.

🚩 2. Activar el Sparse Checkout
Executa això:

bash
Copy
Edit
git sparse-checkout init --cone
Explicació ràpida:

Activa el mode Sparse Checkout perquè puguis especificar quines carpetes vols baixar exactament.

El mode --cone és el més simple i eficaç, permetent seleccionar fàcilment carpetes completes.

🚩 3. Seleccionar la carpeta específica del subprojecte
Ara descarrega només la carpeta del subprojecte 01-HelloWorld, i també el .gitignore global (recomanable):

bash
Copy
Edit
git sparse-checkout set 01-HelloWorld .gitignore README.md
git checkout main
Explicació ràpida:

set 01-HelloWorld .gitignore README.md: indica que vols descarregar només aquests elements.

git checkout main: efectua la descàrrega real d'aquests fitxers al teu directori local.

Ara tens només aquests elements descarregats:

Copy
Edit
Unity2D_Playground/
├── .gitignore
├── README.md
└── 01-HelloWorld/
🚩 4. Modificar un fitxer dins del subprojecte
Suposem que has fet canvis dins del projecte, per exemple:

Has editat el fitxer:

bash
Copy
Edit
01-HelloWorld/Assets/Scripts/player.cs
🚩 5. Comprovar canvis i fer commit
Primer revisa què has canviat amb:

bash
Copy
Edit
git status
Exemple de sortida:

yaml
Copy
Edit
Changes not staged for commit:
	modified:   01-HelloWorld/Assets/Scripts/player.cs
Ara, afegeix aquest fitxer per fer commit:

bash
Copy
Edit
git add 01-HelloWorld/Assets/Scripts/player.cs
Alternativa ràpida (si vols fer commit de tot el modificat alhora):

bash
Copy
Edit
git add .
Ara fes el commit amb missatge descriptiu:

bash
Copy
Edit
git commit -m "Millorat el moviment del player al projecte HelloWorld"
🚩 6. Pujar els canvis al repositori remot (GitHub)
Finalment, puja aquests canvis al servidor remot:

bash
Copy
Edit
git push origin main
Ara tens els teus canvis publicats a GitHub.

🚩 7. Continuar treballant normalment (flux típic)
Cada vegada que modifiquis coses:

bash
Copy
Edit
git status            # revisa els canvis
git add .             # afegeix els fitxers modificats per commit
git commit -m "..."   # commit amb missatge descriptiu
git push origin main  # puja els canvis al servidor remot
🎯 Resum visual del procés complet (Sparse Checkout)
bash
Copy
Edit
# 1. Clone mínim
git clone --filter=blob:none --no-checkout https://github.com/polprats/Unity2D_Playground.git
cd Unity2D_Playground

# 2. Activar Sparse Checkout
git sparse-checkout init --cone

# 3. Descarregar només carpeta específica i fitxers essencials
git sparse-checkout set 01-HelloWorld .gitignore README.md
git checkout main

# 4. Modificar fitxers (fes-ho amb el teu editor o Unity)
# --> 01-HelloWorld/Assets/Scripts/player.cs modificat.

# 5. Commit dels canvis
git add .
git commit -m "Missatge explicant els canvis"

# 6. Push al remot
git push origin main
🛠 Extra: Com afegir més subprojectes més endavant
Si després necessites un altre subprojecte, només cal fer:

bash
Copy
Edit
git sparse-checkout add 02-PlayerMovement
I es descarregarà només aquesta carpeta addicional.

⚠️ Avantatges de Sparse Checkout (resum)
Descarregues només allò que necessites.

És més ràpid en repositoris grans.

Evita ocupar espai innecessàriament.