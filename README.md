# Ryh El Yasmine — Site vitrine & identité de marque

Organisation & décoration d'événements — en salle ou à domicile.
Projet lié à la page Facebook [Ryh el Yasmine](https://www.facebook.com/ryhelyasmine1/).

> « Nous créons, vous vivez l'exception. »

---

## Contenu

```
index.html              Site vitrine (fichier unique, sans dépendance)
images/                 Photos du site, optimisées web (~3 Mo)
marque/
  livrables/            ⭐ Fichiers finaux prêts à l'emploi
  sources/              Sources éditables (HTML/CSS) du logo et de la couverture
    photos-hd/          Photos originales HD utilisées pour la couverture
apercus/                Maquettes de rendu sur la page Facebook
```

## Livrables

| Fichier | Dimensions | Usage |
|---|---|---|
| `marque/livrables/logo-profil.png` | 2000×2000 | Photo de profil Facebook |
| `marque/livrables/logo-transparent.png` | 2000×2000 | Logo détouré (site, documents) |
| `marque/livrables/couverture-facebook.png` | 1640×664 | Photo de couverture Facebook |
| `marque/livrables/couverture-HD.png` | 3280×1328 | Master d'archive / impression |

Les variantes `*-ivoire` et `*-avec-embleme` sont des alternatives conservées.

## Coordonnées

- Téléphone / WhatsApp : **+213 549 09 86 48**
- Facebook : https://www.facebook.com/ryhelyasmine1/

## Prestations

Décoration de mariages et d'événements · Service traiteur haut de gamme ·
Organisation complète · Conférences et événements professionnels

## Le site

Ouvrir `index.html` dans un navigateur — aucun serveur ni installation nécessaire.

Fonctionnalités :
- Galerie filtrable par type d'événement, avec visionneuse plein écran
- Prise de rendez-vous avec calendrier, qui génère un message pré-rempli
  vers le WhatsApp de la page (`wa.me/213549098648`)
- Responsive (mobile, tablette, ordinateur)

### Régénérer le logo ou la couverture

Les visuels sont produits en HTML/CSS puis exportés en PNG :

```bash
cd marque/sources
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --hide-scrollbars \
  --force-device-scale-factor=3 --window-size=1640,664 \
  --screenshot=couverture.png coverB.html
```

Puis réduire à 1640×664 (`sips -Z 1640 couverture.png`) — le suréchantillonnage
donne un rendu nettement plus net qu'un export direct.

### Note sur la couverture Facebook

Facebook recadre la couverture différemment selon l'appareil : ~20 px rognés en
haut et en bas sur ordinateur (affichage 820×312), et ~230 px sur chaque côté sur
mobile (affichage 640×360). La bordure dorée est donc reculée à 56 px des bords :
elle reste entière sur ordinateur, et seuls ses filets horizontaux subsistent sur
mobile — c'est inévitable pour toute bordure de pourtour.
