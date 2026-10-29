```
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, sans-serif;
  background-color: var(--bg-dark);
  color: var(--text-main);
  line-height: 1.6;
  display: flex;
  min-height: 100vh;
}

/* En-tête Mobile */
.mobile-header {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 60px;
  background: var(--bg-sidebar);
  border-bottom: 1px solid var(--border);
  padding: 0 20px;
  align-items: center;
  justify-content: space-between;
  z-index: 100;
}

.mobile-title {
  font-weight: 700;
  font-size: 1.1rem;
  display: flex;
  align-items: center;
  gap: 10px;
}

.menu-toggle {
  background: transparent;
  border: 0;
  color: var(--text-main);
  font-size: 1.5rem;
  cursor: pointer;
}

/* Barre de navigation latérale */
aside {
  width: var(--sidebar-width);
  background-color: var(--bg-sidebar);
  border-right: 1px solid var(--border);
  padding: 30px 20px;
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  gap: 20px;
  z-index: 90;
  transition: transform 0.3s ease;
}

.logo {
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 1.2rem;
  font-weight: 800;
  color: var(--text-main);
  padding-bottom: 20px;
  border-bottom: 1px solid var(--border);
}

.logo-icon {
  width: 36px;
  height: 36px;
  background: var(--accent);
  border-radius: 10px;
  display: grid;
  place-items: center;
  font-size: 1.2rem;
  box-shadow: 0 0 15px var(--accent-glow);
}

nav ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 4px;
}

nav a {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 10px 14px;
  color: var(--text-muted);
  text-decoration: none;
  border-radius: 8px;
  font-size: 0.95rem;
  font-weight: 500;
  transition: all 0.2s ease;
}

nav a:hover {
  color: var(--text-main);
  background-color: rgba(255, 255, 255, 0.05);
}

nav a.active {
  background-color: var(--accent);
  color: #ffffff;
  box-shadow: 0 0 12px var(--accent-glow);
}

/* Contenu principal */
main {
  margin-left: var(--sidebar-width);
  flex: 1;
  padding: 50px 80px 100px;
  max-width: 1200px;
}

header {
  margin-bottom: 50px;
}

header h1 {
  font-size: 2.5rem;
  font-weight: 800;
  margin-bottom: 10px;
  background: linear-gradient(135deg, #ffffff 0%, var(--text-muted) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

header p {
  color: var(--text-muted);
  font-size: 1.1rem;
}

section {
  margin-bottom: 60px;
  scroll-margin-top: 40px;
}

section h2 {
  font-size: 1.6rem;
  font-weight: 700;
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  gap: 12px;
  border-bottom: 1px solid var(--border);
  padding-bottom: 12px;
}

section h3 {
  font-size: 1.2rem;
  font-weight: 600;
  margin: 25px 0 12px 0;
  color: var(--text-main);
}

p {
  color: var(--text-muted);
  margin-bottom: 16px;
}

/* Cartes */
.grid-2 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin: 20px 0;
}

.card {
  background-color: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 24px;
  transition: transform 0.2s ease, border-color 0.2s ease;
}

.card:hover {
  transform: translateY(-2px);
  border-color: rgba(88, 101, 242, 0.4);
}

.card h4 {
  font-size: 1.1rem;
  font-weight: 700;
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.card p {
  font-size: 0.95rem;
  margin-bottom: 0;
}

/* Blocs de code */
.code-wrapper {
  position: relative;
  margin: 15px 0;
}

.code-block {
  background-color: var(--code-bg);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 18px 20px;
  font-family: 'Fira Code', monospace;
  font-size: 0.9rem;
  color: #e1e4e8;
  overflow-x: auto;
}

.code-block pre {
  white-space: pre;
  word-break: normal;
}

.copy-btn {
  position: absolute;
  top: 10px;
  right: 10px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  color: var(--text-muted);
  padding: 6px 12px;
  border-radius: 6px;
  font-size: 0.8rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.2s ease;
}

.copy-btn:hover {
  background: var(--accent);
  color: #fff;
  border-color: var(--accent);
}

.inline-code {
  background-color: rgba(255, 255, 255, 0.08);
  padding: 2px 8px;
  border-radius: 4px;
  font-family: 'Fira Code', monospace;
  font-size: 0.88rem;
  color: #e1e4e8;
}

/* Badges */
.badge {
  display: inline-block;
  padding: 4px 10px;
  border-radius: 6px;
  font-size: 0.8rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.badge-blue { background: rgba(88, 101, 242, 0.15); color: var(--accent); border: 1px solid rgba(88, 101, 242, 0.3); }
.badge-green { background: rgba(35, 165, 90, 0.15); color: var(--green); border: 1px solid rgba(35, 165, 90, 0.3); }
.badge-yellow { background: rgba(240, 178, 50, 0.15); color: var(--yellow); border: 1px solid rgba(240, 178, 50, 0.3); }

/* Tableaux */
.table-container {
  overflow-x: auto;
  margin: 20px 0;
  border: 1px solid var(--border);
  border-radius: 10px;
}

table {
  width: 100%;
  border-collapse: collapse;
  background-color: var(--bg-card);
}

th, td {
  padding: 14px 18px;
  text-align: left;
  border-bottom: 1px solid var(--border);
}

th {
  background-color: rgba(255, 255, 255, 0.02);
  font-size: 0.85rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  color: var(--text-muted);
}

tr:last-child td {
  border-bottom: none;
}

/* Encadrés d'information */
.callout {
  padding: 18px 20px;
  border-radius: 10px;
  border-left: 4px solid var(--accent);
  background-color: rgba(88, 101, 242, 0.08);
  margin: 20px 0;
}

.callout h5 {
  font-size: 1rem;
  font-weight: 700;
  margin-bottom: 6px;
  color: var(--text-main);
}

.callout p {
  margin-bottom: 0;
  font-size: 0.95rem;
}

/* Barre de recherche de variables */
.search-box {
  margin-bottom: 15px;
}

.search-input {
  width: 100%;
  padding: 12px 16px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 8px;
  color: var(--text-main);
  font-size: 0.95rem;
  outline: none;
  transition: border-color 0.2s ease;
}

.search-input:focus {
  border-color: var(--accent);
}

/* Design Responsive */
@media (max-width: 1024px) {
  .mobile-header {
    display: flex;
  }

  aside {
    transform: translateX(-100%);
    top: 60px;
  }

  aside.open {
    transform: translateX(0);
  }

  main {
    margin-left: 0;
    padding: 90px 20px 60px;
  }
}

```

```
<!-- Vue d'ensemble -->
<section id="overview">
  <h2>📌 Vue d'ensemble</h2>
  <p>Cette solution clé en main combine un **bot Discord autonome** rédigé en Node.js (discord.js v14) et un **Dashboard Web d'administration**. Il offre un contrôle total sur les messages du bot, le règlement du serveur, les sanctions automatiques et la modération sans avoir besoin de toucher une seule ligne de code.</p>
  
  <div class="grid-2">
    <div class="card">
      <h4>⚡ Modération du Règlement</h4>
      <p>Supervise automatiquement les membres sans le rôle "Règlement lu", délivre des rappels automatiques et bannit les retardataires après expiration des délais.</p>
    </div>
    <div class="card">
      <h4>🎛️ Dashboard Web d'Édition</h4>
      <p>Interface responsive protégée par mot de passe permettant d'éditer les textes, les statuts, les messages de bienvenue et les boutons interactifs.</p>
    </div>
    <div class="card">
      <h4>🗄️ SQLite Légère</h4>
      <p>L'ensemble de la configuration et le suivi des membres avertis résident dans un fichier <span class="inline-code">database.db</span> unique et facile à exporter.</p>
    </div>
    <div class="card">
      <h4>🚀 Compatibilité KarmaCloud</h4>
      <p>Prêt à tourner 24/7 sur un serveur KarmaCloud avec accès SFTP et support des variables d'environnement <span class="inline-code">.env</span>.</p>
    </div>
  </div>
</section>

<!-- Architecture -->
<section id="architecture">
  <h2>🏗️ Architecture des Fichiers</h2>
  <p>Arborescence complète du projet Node.js + Express à transférer sur le serveur KarmaCloud :</p>

  <div class="code-wrapper">
    <button class="copy-btn" onclick="copyCode(this)">Copier</button>
    <div class="code-block">
      <pre>mon-bot-discord/

```

├── 📁 public/            # Application Web Frontend (Dashboard)
│   ├── 📄 index.html     # Page HTML unique du Panel
│   └── 📄 app.js         # Logique dynamique & requêtes API
├── 📄 .env               # Fichier secret (Token Discord, Port, Password)
├── 📄 bot.js             # Code source du Bot Discord
├── 📄 db.js              # Gestionnaire de base de données SQLite
├── 📄 server.js          # API REST Express.js pour le Panel Web
├── 📄 schema.sql         # Fichier d'initialisation des tables SQLite
├── 📄 migrate.js        # Script de transfert depuis un ancien config.json
└── 📄 package.json       # Dépendances du projet Node.js



```
<!-- GitHub Pages -->
<section id="github-pages">
  <h2>🌐 Héberger cette documentation sur GitHub Pages</h2>
  <p>Pour mettre cette page web à disposition de votre cliente gratuitement et indépendamment du serveur du bot, vous pouvez la publier sur GitHub Pages en quelques clics :</p>

  <div class="callout">
    <h5>💡 Instructions pour GitHub Pages :</h5>
    <p>1. Créez un dépôt public sur votre compte GitHub (ex: <span class="inline-code">bot-discord-doc</span>).<br>
    2. Déposez ce fichier sous le nom exact <span class="inline-code">index.html</span> dans le dépôt.<br>
    3. Allez dans <strong>Settings</strong> > <strong>Pages</strong>.<br>
    4. Sous <strong>Source</strong>, sélectionnez la branche <span class="inline-code">main</span> / <span class="inline-code">root</span> puis cliquez sur <strong>Save</strong>.<br>
    5. Votre site sera disponible en 1 à 2 minutes à l'adresse : <span class="inline-code">https://votre-pseudo.github.io/bot-discord-doc/</span>.</p>
  </div>
</section>

<!-- Déploiement KarmaCloud -->
<section id="deployment">
  <h2>🚀 Déploiement sur KarmaCloud (SFTP)</h2>
  
  <h3>1. Configuration du fichier .env</h3>
  <p>Créez un fichier nommé <span class="inline-code">.env</span> à la racine de votre dossier sur le serveur :</p>
  <div class="code-wrapper">
    <button class="copy-btn" onclick="copyCode(this)">Copier</button>
    <div class="code-block">
      <pre>TOKEN=votre_token_secret_discord_ici

```

PANEL_PASSWORD=mot_de_passe_choisi_pour_la_cliente
PORT=3000


```
  <h3>2. Installation des paquets Node.js</h3>
  <p>Ouvrez la console KarmaCloud ou votre terminal SSH et exécutez :</p>
  <div class="code-wrapper">
    <button class="copy-btn" onclick="copyCode(this)">Copier</button>
    <div class="code-block">
      <pre>npm install</pre>
    </div>
  </div>

  <h3>3. Démarrage de l'application</h3>
  <p>Lancez le bot Discord et le serveur Web du Panel simultanément :</p>
  <div class="code-wrapper">
    <button class="copy-btn" onclick="copyCode(this)">Copier</button>
    <div class="code-block">
      <pre>npm start</pre>
    </div>
  </div>
</section>

<!-- Manuel Panel Web -->
<section id="dashboard">
  <h2>💻 Manuel d'utilisation du Panel Web</h2>
  <p>La cliente peut se connecter au Dashboard en entrant l'adresse IP et le port configurés (ex: <span class="inline-code">http://ip-du-serveur:3000</span>) ainsi que le mot de passe défini dans le fichier <span class="inline-code">.env</span>.</p>

  <div class="table-container">
    <table>
      <thead>
        <tr>
          <th>Onglet</th>
          <th>Fonctionnalités & Réglages</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>📊 Vue d'ensemble</strong></td>
          <td>Visualisation en direct du statut du bot (En ligne/Hors ligne, Ping ms, serveurs), statistiques d'utilisation et liste des membres actuellement sous statut <em>Averti</em>.</td>
        </tr>
        <tr>
          <td><strong>💬 Textes & Statut</strong></td>
          <td>Modification du statut de jeu du bot, des messages privés d'avertissement/kick/ban et des réponses associées aux commandes slash.</td>
        </tr>
        <tr>
          <td><strong>⚙️ Automatismes</strong></td>
          <td>Configuration de l'ID du rôle "Non Lu" et ajustement précis de l'intervalle de vérification automatique ainsi que des délais de rappel et de bannissement.</td>
        </tr>
      </tbody>
    </table>
  </div>
</section>

<!-- Variables Dynamiques -->
<section id="variables">
  <h2>🔤 Variables Dynamiques</h2>
  <p>Ces balises peuvent être directement tapées dans les champs du Panel. Elles seront automatiquement remplacées par la vraie donnée au moment de l'envoi du message sur Discord.</p>

  <div class="search-box">
    <input type="text" id="variableSearch" class="search-input" placeholder="Rechercher une variable ou une commande...">
  </div>

  <div class="table-container">
    <table id="variablesTable">
      <thead>
        <tr>
          <th>Variable</th>
          <th>Description</th>
          <th>Champ compatible</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><span class="inline-code">{user}</span></td>
          <td>Remplacé par le pseudo / tag du membre.</td>
          <td>Réponses <span class="inline-code">/kick</span></td>
        </tr>
        <tr>
          <td><span class="inline-code">{channel}</span></td>
          <td>Remplacé par la mention du salon visé.</td>
          <td>Réponses <span class="inline-code">/say</span></td>
        </tr>
        <tr>
          <td><span class="inline-code">{step}</span></td>
          <td>Numéro de l'étape de confirmation en cours.</td>
          <td>Bouton <span class="inline-code">/espace</span></td>
        </tr>
        <tr>
          <td><span class="inline-code">{total}</span></td>
          <td>Nombre total de clics nécessaires.</td>
          <td>Bouton <span class="inline-code">/espace</span></td>
        </tr>
        <tr>
          <td><span class="inline-code">{kicked}</span></td>
          <td>Nombre de membres expulsés avec succès.</td>
          <td>Résultat <span class="inline-code">/espace</span></td>
        </tr>
        <tr>
          <td><span class="inline-code">{failed}</span></td>
          <td>Nombre d'échecs d'expulsion (ex: rôle supérieur).</td>
          <td>Résultat <span class="inline-code">/espace</span></td>
        </tr>
        <tr>
          <td><span class="inline-code">\n</span></td>
          <td>Effectue un saut de ligne dans le message.</td>
          <td>Tous les champs texte</td>
        </tr>
      </tbody>
    </table>
  </div>
</section>

<!-- Commandes Slash -->
<section id="commands">
  <h2>⚡ Commandes Slash Disponibles</h2>

  <div class="grid-2">
    <div class="card">
      <h4>/kick <span class="badge badge-blue">Modération</span></h4>
      <p>Exclut le membre spécifié et lui envoie au préalable un message privé de notification personnalisable dans le panel.</p>
    </div>

    <div class="card">
      <h4>/espace <span class="badge badge-yellow">Owner Only</span></h4>
      <p>Déclenche la procédure d'éjection globale avec confirmation à clics multiples réservée au propriétaire du serveur.</p>
    </div>

    <div class="card">
      <h4>/say <span class="badge badge-blue">Admin</span></h4>
      <p>Envoie un message sous le nom et le pseudo du bot dans le salon de discussion sélectionné.</p>
    </div>

    <div class="card">
      <h4>/botinfo <span class="badge badge-green">Créateur</span></h4>
      <p>Affiche un rapport technique sur les performances, le ping et le temps de fonctionnement du bot.</p>
    </div>
  </div>
</section>

<!-- Base de données -->
<section id="database">
  <h2>🗄️ Gestion de la Base de Données</h2>
  <p>Toutes les informations sont conservées localement dans <span class="inline-code">database.db</span> grâce à SQLite.</p>

  <div class="callout">
    <h5>🛡️ Récupération & Sauvegarde :</h5>
    <p>Pour effectuer une sauvegarde manuelle ou déplacer la configuration sur un autre serveur, connectez-vous en SFTP sur KarmaCloud et téléchargez simplement le fichier <span class="inline-code">database.db</span>.</p>
  </div>
</section>

```