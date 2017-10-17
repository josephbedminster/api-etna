# API ETNA
Liste non-exhaustive des routes utilisées par l'ETNA (@ETNA ALTERNANCE, France), pour ses micro-services.

### Authentification
Se connecter, obtenir un cookie :
```
POST https://auth.etna-alternance.net/login
fields: login <string>, password <string>
```
Obtenir des informations sur son compte une fois connecté :
```
GET https://auth.etna-alternance.net/identity
```
### Informations utilisateurs
Obtenir les informations d'un utilisateur via son ID :
```
GET https://auth.etna-alternance.net/api/users/{id}
```
Obtenir les promotions de l'utilisateur courant :
```
GET https://prepintra-api.etna-alternance.net/promo
```
Obtenir les "Activités en cours" :
```
GET https://modules-api.etna-alternance.net/students/{login}/currentactivities
```
Obtenir les "Notifications" :
```
GET https://prepintra-api.etna-alternance.net/students/{login}/informations
```
Obtenir la photo de l'user :
```
GET https://auth.etna-alternance.net/api/users/{login}/photo
```
Obtenir les évènements du planning :
```
GET https://prepintra-api.etna-alternance.net/students/{login}/events?end={end}&start={start}
format: 2017-04-17+00:00:00 ou 2017-04-17
```
Obtenir les notes :
```
GET https://prepintra-api.etna-alternance.net/terms/{promo_id}/students/{login}/marks
```
### Trombinoscope
Obtenir le trombinoscope toutes promotions confondues :
```
GET https://prepintra-api.etna-alternance.net/trombi
```
Obtenir le trombinoscope d'une promotion :
```
GET https://prepintra-api.etna-alternance.net/trombi/{id_promo}
```
### Informations promotion
Obtenir les informations d'une promotion :
```
GET https://prepintra-api.etna-alternance.net/promo/{target_name}
```
### Murs
Obtenir les murs accessibles par l'utilisateur :
```
GET https://prepintra-api.etna-alternance.net/walls
```
Accéder à un mur :
```
GET https://prepintra-api.etna-alternance.net/walls/{wall_name}/conversations?from={start}&size={end}
```
Accéder au mur d'une promotion :
```
GET https://prepintra-api.etna-alternance.net/terms/{wall_name}/conversations?from={start}&size={end}
format: (int). Ex: 0 à 50.
```
### Tickets
Afficher les tickets de l'utilisateurs (ouverts et clos) :
```
GET  https://tickets.etna-alternance.net/api/tasks.json
```
Afficher un ticket via son id :
```
GET https://tickets.etna-alternance.net/api/tasks/{id}.json
```
### Trophées / Badges
Obtenir les trophées d'un utilisateur :
```
GET https://achievements.etna-alternance.net/api/users/{login}/achievements
````
Obtenir l'image d'un badge :
```
GET https://achievements.etna-alternance.net/api/achievements/{id}.png
```
### Logs Alternance
Obtenir les logs de travail :
```
GET https://gsa-api.etna-alternance.net/students/{login}/logs
````
### Activité / Projet
Obtenir les informations d'un projet (groupes formés) :
```
GET 
https://prepintra-api.etna-alternance.net/sessions/{id_session}/project/{id_project}/groups
```
Obtenir les informations d'un projet (mon groupe) :
```
GET https://prepintra-api.etna-alternance.net/sessions/{id_session}/project/{id_project}/mygroup
```
## Contact
joseph@etna.io