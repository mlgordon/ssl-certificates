---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-28"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL-Zertifikate verwalten

{{site.data.keyword.BluSoftlayer_full}} bietet jetzt die Möglichkeit zum Speichern von Zertifikaten im eigenen Portal. Dieses kann nicht nur als Repository für die Verwaltung der Zertifikate dienen, sondern ist auch bei der Nutzung von Services und beim Anfordern von Zertifikaten erforderlich.

1. Greifen Sie mit Ihren eindeutigen Berechtigungsnachweisen auf das [{{site.data.keyword.slportal_full}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} zu.
2. Wählen Sie aus dem Menü **Sicherheit** die Option **SSL > Zertifikate > Zertifikate verwenden** aus.

Es werden eine Liste der aktuellen Zertifikate sowie entsprechende Statusinformationen angezeigt.

Sie können ein Zertifikat durchsuchen, Teile oder eine PEM-formatierte Version des Zertifikats herunterladen oder das Ablaufdatum für die Zertifikate überprüfen. Außerdem können Sie sehen, wie viele Services die einzelnen Zertifikate momentan verwenden. Dies zeigt Ihnen, welche Maßnahme ergriffen werden muss, wenn ein Zertifikat fast abgelaufen ist.

## Zertifikat hinzufügen

Wenn Sie ein Zertifikat hinzufügen möchten, wählen Sie im Untermenü des Navigationsbereich oder im Zertifikatslistentitel die Option zum Hinzufügen eines Zertifikats aus. Sie müssen nur das Zertifikat und den entsprechenden privaten Schlüssel angeben. Wenn Ihr Aussteller ein Zwischenzertifikat bereitstellt und Sie dieses nicht angeben, kann dies jedoch zu einer unterbrochenen Zertifikatskette und fehlerhaften Validierung für Endbenutzer oder zugehörige Services führen.

Hinweis: Private Schlüssel, für die eine Kennphrase erforderlich ist, können nicht gespeichert werden.

Sobald sie hinzugefügt wurden, werden die folgenden Felder direkt aus den Zertifikaten abgeleitet:

* Allgemeiner Name
* Name der Organisation
* Gültigkeitszeitraum


Geschafft!

## Zertifikat bearbeiten

Durch das Aktivieren des Dreiecks links neben einem Zertifikat werden die Bestandteile des Zertifikats in ihrer Gesamtheit sichtbar gemacht. Außerdem können dann die Bestandteile bearbeitet werden. Es kann außerdem eine Anmerkung hinzugefügt werden und bei Bedarf kann das Zertifikat entfernt werden. Zudem wird eine Liste der Services angezeigt, die das Zertifikat momentan verwenden.



Wichtiger Hinweis: Der private Schlüssel, das Zertifikat oder das Zwischenzertifikat als Bestandteile von Zertifikaten können nur für Zertifikate aktualisiert werden, die keinem Service zugeordnet sind. Das Zertifikat kann auch nicht entfernt werden.

Sie können die Anmerkung jederzeit ändern.

## Zertifikat entfernen

Um ein Zertifikat zu entfernen, befolgen Sie die Schritte zum Bearbeiten des Zertifikats, aktivieren Sie das Kontrollkästchen zum Bestätigen der Zertifikatsentfernung und speichern Sie die Änderung.

### API

Sie können Zertifikate auch über die SLAPI 'sldn.softlayer.com' hinzufügen, entfernen, bearbeiten und durchsuchen. Einige Beispiele dazu finden Sie im folgenden SLDN-Artikel: sldn.softlayer.com/article/SSL-Management-my-SLAPI-Its-more-likely-you-think.
