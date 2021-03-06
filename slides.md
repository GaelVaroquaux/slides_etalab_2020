class: center, middle

# Covid19-dash

Emmanuelle Gouillart & Gaël Varoquaux

Plotly &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; INRIA 

https://covid19-dash.github.io/

Russ Poldrack, Guillaume Lemaitre, Ashwin PN, Mojdeh Rastgoo Lemaitre, Ranjan
Khyadad, Marianne Corvellec, Elizabeth DuPre

???

Some notes go here including this list:


---

# But: Sensibiliser le grand public

**Début mars**: Indifférence généralisée.

Non compréhension de la croissance exponentielle.

Ergotage sur les termes pandémie et phase 3.


.red.shift-left.width60.pull-left[
Dashboards existants à l'époque:

* Évolution de la Chine uniquement
* Trop technique
]
.green.width40.shift-right.pull-right[
Conséquences:

* Présentation simple
* Explications texte
]

<img src="lemonde-titre.png" style="float: left; width: 42%; margin-right: -8%;margin-top: -2%;">
<img src="lemonde-titre2.png" style="float: right; width: 42%; margin-right: -8%;margin-top: -2%;">

---

# Techno web pour chercheurs pressés

.shift-right.pull-right[

<iframe width="120%" height='900px' src="https://plotly.com/python/choropleth-maps/" frameborder="0" allowfullscreen></iframe>


]


* Python: stack scientifique
* Plotly: figure interactives, web natif (HTML + Javascript) avec API Python
* Dash: applications web analytiques en pur Python

.xxxlarge[🐍]


---

# Demo

* Limiter les interactions
* Choix: 
    * Rapporté à la population (infos complètes dans le hover)
    * Lin vs. log
    * Cas confirmés et décès


---

# Développement pour chercheurs maladroits

* GitHub Actions
* Fonctionnement communautaire: revue des pull requests grâce aux artifacts
  Circle CI

---

# Data wrangling

<img src="github_wrangling.png" style="float: right; width: 52%; margin-right: -8%;margin-top: -12%;">

* Source de données

   * Johns Hopkin University
   * Cas détectés et dates

* Croiser les données

   * Appariement d'entités

.xxxlarge[🐼]

---

# Modèle prédictif

.shift-right.pull-right[

<img src="extrapolation_linear.png" style="width: 100%; margin-top: -30%;">

<img src="extrapolation_long_time.png" style="width: 100%;">

]

* Modèle linéaire en échelle log
* Fenêtre sur 14 jours
* Poids décroissant avec le temps
* Validation en rejouant l'historique

https://github.com/covid19-dash/covid-dashboard/blob/master/modeling.py

---
class: center, middle


# Thank you

.xxxlarge[😸]
