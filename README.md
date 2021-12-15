# ACCESSIBILITE_NUMERIQUE

Qu'entends-t'on par accessibilité ?<br>
- Que l'on puisse entrer... où... pourquoi ?<br>
- Accessible à quoi ? Pour qui ?


### L'accessibilité numérique

Depuis les années 1990, le numérique est apparu dans notre quotidien...<br>
petit à petit. Il a mis du temps à entrer dans nos foyers, via le minitel,<br>
les ordinateurs dits de bureau, les logiciels de gestion, les langages<br>
informatiques.<br>
Certes, le temps a passé et les générations qui ont suivies ont appris<br>
à utiliser ces nouvelles technologies et à se les approprier pour les faire<br>
évoluer... aujourd'hui qui n'a pas un mobile et une connexion internet ?

Si la majorité, peut se connecter et accéder aux sources d'informations<br>
numériques, il n'en va pas de même pour les personnes aveugles ou <br>
ayant une déficience acoustique ou visuelle.<br>

Comment permettre de lire un site internet essentiel (comme ceux liés aux<br>
démarches administratives) ou à un formulaire en ligne ?


### Les aides à la navigation ou liens d'évitement

Le menu est placé dès le début d'une page, afin que les liens permettent<br>
dès le chargement de la page d'accéder à la partie recherchée sans parcourir<br>
toute la page pour trouver l'information.

Les liens d'évitement facilitent l'accès au site pour les handicapés et<br>
notamment pour les non voyants : ils leur permettent de se placer <br>
directement à l'endroit souhaité. 

Exemple et informations complémentaires :

https://www.alsacreations.com/article/lire/572-Les-liens-d-evitement.html

A l'origine, le lien d'évitement (skip lines en anglais) a été conçu pour<br>
permettre de passer un regroupement de liens.

Petit exemple codé :

'''<h2 class="navhead"><a name="technologies" id="technologies">W3C A to Z</a></h2>

<ul>
   <li class="invisible">
     <a class="navlink" title="Skip W3C A-Z" href="#news">Skip to News</a>
   </li>
</ul>

Il permet de "zapper" et d'aller directement à l'info.


#### Aides à la navigation : rôles ARIA des zones du document

Avec l'aide technique (lecteur d'écran...) on peut se déplacer dans les pages.<br>
Ces rôles permettent de mieux structurer le document et d'aider dans la navigation.

EX : avec NVDA : NVDA + F7<br>
Avec JAWS : CTRL + INS + ;

Pour coder de façon efficace et propre en html :

<script type="text/javascript">
sap = {ui:{keycodes:{SPACE:32, ENTER:13 }}};<br>
//gère les clics et les événement clavier sur le lien<br>
function navigateLink(evt) {<br>
    if (evt.type=="click" ||<br>
        evt.keyCode == sap.ui.keycodes.SPACE ||<br>
        evt.keyCode == sap.ui.keycodes.ENTER) {<br>
        var ref = evt.target != null ? evt.target : evt.srcElement;<br>
        if (ref) window.open(ref.getAttribute("href"),"_blank");<br>
    }
}
</script>

<body role="application">

    <h3>Lien simple créé avec un <span></h3>
    <span href="http://www.w3c.org" onkeydown="navigateLink(event)" onclick="navigateLink(event)" tabindex="0" id="link1" role="link" class="link">
      Activez ce lien en appuyant sur la barre d’espace ou la touche Entrée
    </span>
</body>

On peut mettre un lien avec span et définir les fonctions dans un script.<br>
https://developer.mozilla.org/fr/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_link_role
   

   
#### Navigation par tabulation

Appuyer sur Tab et répéter jusqu'à sélectionner le lien qui nous intéresse.<br>
On valide avec Entrée.


### Utilitaires pour déficients visuels

#### Différents types de logiciels

##### Lecteurs d'écrans
Transforment les informations portées à l'écran (logiciel de traitement de texte<br>
ou navigateur web par exemple) à destination d'une synthèse vocale ou d'un <br>
périphérique comme une plage braille.

##### Navigateurs vocaux
Destinés à la navigation sur internet dont ils assurent un rendu graphique<br>
(affichage traditionnel) et une lecture vocale ou à destination d'une plage braille.

##### Navigateurs textuels
Affichent des pages web en mode texte.

##### Loupes et assimilés
Elles ont pour objectif d'agrandir ou de modifier une zone de l'écran<br>
pour la rendre lisible par un mal-voyant.

#### Logiciels à connaitre pour l'accessibilité numérique

<b>JAWS</b> (Job Access With Speech)<br>
Logiciel pour déficients visuels, sous Windows, édité par la société<br>
Freedom Scientific.<br>
Logiciel de revue d'écran - lecteur d'écran, qui transforme un texte affiché<br>
sur un écran en un texte oral ou un texte en braille.

<b>NVDA</b><br>
Une revue d'écrans libre et gratuite pour Microsoft Windows XP, Vista et seven.

<b>VOICEOVER</b><br>
Permet aux non-voyants et malvoyants d'utiliser un ordinateur : <br>
Apple a conçu VoiceOver, une solution intégrée à chaque Mac. Solution fiable<br>
simple à apprendre.
