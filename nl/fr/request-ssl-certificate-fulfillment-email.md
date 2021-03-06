---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-28"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Demander l'e-mail d'exécution d'un certificat SSL

## Aperçu

Lorsque vous passez commande d'un nouveau certificat SSL via {{site.data.keyword.BluSoftlayer_full}},
l'autorité de certification envoie un e-mail d'exécution à l'administrateur de domaine dont les coordonnées sont fournies dans cette commande.
Cet e-mail contient tous les détails associés au certificat SSL.
Vous pouvez à tout moment demander un nouvel envoi de l'e-mail d'exécution d'un certificat particulier à partir
de l'écran Commandes SSL du portail {{site.data.keyword.slportal_full}}.
Suivez les étapes ci-dessous pour demander à l'autorité de certification qu'elle vous renvoie l'e-mail d'exécution d'un certificat SSL.


## Demander un e-mail d'exécution

1. Accédez au portail [{{site.data.keyword.slportal_full}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
2. Dans le menu **Sécurité**, sélectionnez **SSL > Commandes**.
3. Cliquez sur le lien **Envoyer** dans la colonne **E-mail**, sur la ligne du certificat SSL voulu.
<br/>**Remarque :** une fenêtre apparaît pour vous permettre de confirmer votre demande.
Cette fenêtre contient l'adresse e-mail de l'administrateur de domaine qui a été communiquée lors de la commande du certificat SSL.

4. Cliquez sur le bouton **Renvoyer l'e-mail** pour confirmer votre choix et
demander que l'autorité de certification vous envoie un nouvel exemplaire de l'e-mail d'exécution.
Sinon, cliquez sur **Annuler** pour annuler l'opération.


## Etapes suivantes

Une fois que vous avez demandé à recevoir un nouvel exemplaire de l'e-mail d'exécution, votre demande est
transférée à l'autorité de certification compétente afin qu'elle y réponde.
Les détails d'un certificat SSL étant confidentiels, {{site.data.keyword.BluSoftlayer_notm}} ne les stocke pas
sur nos systèmes.
Une fois les détails du certificat SSL reçus par e-mail, au besoin, ils peuvent être [importés](import-ssl-certificate.html)
manuellement sur le portail {{site.data.keyword.slportal}}.

