# Juxtaphony Project

[English](https://github.com/jin237/juxtaphony_project/blob/main/README-en.md)
[日本語](https://github.com/jin237/juxtaphony_project/blob/main/README.md)

# Projet Juxtaphony

<img src="https://github.com/jin237/jaxtaphony_project_english/blob/main/images/document_visual_theme.003.jpeg">

<img src="https://github.com/jin237/jaxtaphony_project_english/blob/main/images/document_visual_theme_serious.002.jpeg">

### Aperçu et importance du projet par l'équipe du projet Juxtaphony
Ce projet vise à minimiser le risque d'infection virale dans des conditions "denses". Parler dans un environnement dense augmente le risque d'infection par gouttelettes, mais "ne pas parler" est impossible dans la vie quotidienne. C'est pourquoi il a été rapporté que le fait de parler d'une voix chuchotée peut réduire la quantité de virus et de bactéries dans la bouche. Si nous pouvons réaliser des conversations "chuchotées", il sera possible de rétablir les activités sociales qui étaient possibles avant l'épidémie en portant des masques et en évitant les groupes.
Dans ce contexte, l'équipe du projet aimerait se concentrer sur les "microphones à gorge" (également appelés microphones à gorge ou microphones à conduction osseuse) et les utiliser, car ils peuvent capter de petits sons au niveau de la gorge pour réaliser des conversations "à voix basse". De plus, en développant une application "SILENT - parler" utilisant Bluetooth (une fonction de communication sans fil attachée aux smartphones, ordinateurs, etc.), nous pensons que nous pouvons rapidement créer un environnement facile à utiliser pour réaliser des conversations à l'aide d'un micro laryngophone. 

### Qu'est-ce qu'un "micro laryngophone" ?
Un "micro laryngophone" est un microphone qui capte la voix par conduction osseuse autour du larynx, et qui peut capter la voix même dans des environnements bruyants ou venteux (Figure 1 à droite). Les autres types de microphones ne fonctionnent pas bien dans les environnements ci-dessus en raison du bruit de fond élevé. Plus la qualité du microphone est élevée, plus il peut capter les "chuchotements" et donc permettre la communication avec un très faible volume vocal.

<img src="https://github.com/jin237/jaxtaphony_project_english/blob/main/images/ThroatMIC_Black.png" height=200px>

formulaire Wikipedia：： ["Microphone pour la gorge"](https://en.wikipedia.org/wiki/Throat_microphone)
>Un laryngophone est un type de microphone à contact qui absorbe les vibrations directement de la gorge du porteur au moyen de capteurs simples ou doubles portés contre le cou. Ces capteurs, appelés transducteurs, peuvent capter la parole même dans des environnements extrêmement bruyants ou venteux, comme sur une moto ou dans une boîte de nuit. D'autres types de microphones ne fonctionnent pas bien dans ces conditions en raison des niveaux élevés de bruit de fond. Les laryngophones avancés sont capables de capter les chuchotements, et sont donc performants dans les environnements où il est nécessaire de communiquer avec d'autres personnes à distance en silence, comme lors d'opérations militaires ou de maintien de l'ordre secrètes. Les microphones à gorge sont également très utiles lorsqu'un casque ou une protection respiratoire est nécessaire. De nombreux appareils respiratoires isolants, CABA, respirateurs SAR, respirateurs élastomères, PAPR N95 ou masques de protection respiratoire ne sont pas équipés d'un microphone à l'intérieur du masque. Le micro laryngophone peut être utilisé en toute sécurité, car il est placé à l'extérieur du joint facial du masque et, en tant que tel, ne compromet pas la protection respiratoire fournie par le masque, ni n'enfreint les agréments et la certification des masques.
>Avec l'arrivée de COVID-19 en 2020, l'utilisation du micro laryngophone s'est étendue à d'autres domaines tels que les urgences des hôpitaux [1], Commerce de détail et restaurants. En effet, l'utilisation universelle de masques faciaux et de séparateurs physiques en plastique transparent pour renforcer la distance sociale a rendu les communications face à face beaucoup plus difficiles, les gens devant élever la voix de manière significative pour communiquer.
<br><br>
### Qu'est-ce que "SILENCIEUX - parlant" ?
Nous allons développer une application qui permettra à "SILENT - talking" de parler avec un micro laryngophone en utilisant le Bluetooth. Cette application propose quatre modes (tableau 1 à droite) et peut être utilisée dans toutes les situations de la vie quotidienne, telles que les conférences et les cours à l'école, les cafés, les dîners et les réunions dans les bureaux. Elle peut être utilisée pour réduire au maximum le risque lorsqu'un groupe de personnes se réunit. Il peut également être transporté partout et peut être utilisé quotidiennement en le portant autour du cou.

Chart１ 4 Modes et contenus sur SILENT - parler
| Mode | Nombre de personnes | Contenu |
|------|------|------|
| Ad-hoc | One-to-One | Permettre les appels vocaux via Bluetooth |
| Partie| Multitude | Permettre les appels vocaux par le biais de dispositifs hôtes | 
| Table-talk | Multitude | Réalisation d'une conversation vocale aléatoire dans un espace fixe |
| Salle de classe | One-to-Multitude | Réalisation de conférences et de cours par conversation vocale via des dispositifs hôtes |

<img src="https://github.com/jin237/jaxtaphony_project_english/blob/main/images/app_4mode_explain.007.jpeg" height=250px><img src="https://github.com/jin237/jaxtaphony_project_english/blob/main/images/app_4mode_explain.008.jpeg" height=250px><img src="https://github.com/jin237/jaxtaphony_project_english/blob/main/images/app_4mode_explain.009.jpeg" height=250px><img src="https://github.com/jin237/jaxtaphony_project_english/blob/main/images/app_4mode_explain.010.jpeg" height=250px>
<br><br>

# Que fait le projet Juxtaphony ?
"Jaxtaphonie" est un mot inventé en combinant "Jaxta" et "ostéophonie".
Ce projet fait principalement 2 travaux.
- Créer un ensemble de données original pour le micro laryngophone
- Création d'une application originale utilisant le Bluetooth et filtrée pour améliorer le son du micro laryngophone
