SafeBase - Système de Backup/Restauration de Bases de Données
Fastify
React
PostgreSQL
MySQL
Docker

SafeBase est une solution complète pour sauvegarder et restaurer automatiquement des bases de données (PostgreSQL, MySQL) via une interface web intuitive et des tâches planifiées (CRON).

📌 Fonctionnalités
✅ Backup automatisé (dumps SQL planifiés)
✅ Restauration en 1 clic depuis l’interface
✅ Gestion centralisée des sauvegardes
✅ Support multi-BDD (PostgreSQL, MySQL)
✅ Monitoring des jobs CRON
✅ Interface React simple et moderne

🚀 Installation
Prérequis
Docker & Docker-Compose

Node.js 18+

Lancement avec Docker
bash
git clone https://github.com/morgane-marechal/SafebaseBack.git
cd safebase
docker-compose up -d
➡️ L'application sera disponible sur :

Frontend : http://localhost:3000

Backend (API) : http://localhost:3001

Adminer (DB GUI) : http://localhost:9080

🛠️ Architecture
safebase/
├── safebasefront/      # Interface React
├── safebaseback/       # API Fastify
├── docker-compose.yml  # Configuration des services
└── README.md
Services Docker
Service	Description	Port
safebasefront	Interface React	3000
safebasefastify	API Fastify (backup/restore)	3001
postgres_database	PostgreSQL	5432
mysql_database	MySQL	3306
adminer	Gestionnaire de BDD	9080
🔧 Configuration
Variables d'environnement (.env)
env


📚 Documentation Technique
API Endpoints
Route	Méthode	Description
/api/database	GET	Liste toutes les BDD
/api/backup	POST	Crée un nouveau backup
/api/systeme/dump/:databaseId	GET	Déclenche un dump manuel
/api/systeme/restauration/:backupId	GET	Restaure une BDD
💡 Améliorations Possibles
Notifications (Email/Slack en cas de backup échoué)


📜 Licence
MIT © Marechal Morgane

Un problème ?
Ouvrez une issue ou contactez-moi ! ✨

Développé avec ❤️ et Fastify