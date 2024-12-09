# Deep Art Gallery

Dieses Projekt ermöglicht es, Bilder mit neuronalen Netzwerken in verschiedene künstlerische Stile zu transformieren und
die Ergebnisse in einer Galerie darzustellen. Um dein eigenes Ergebnis hinzuzufügen, folge den untenstehenden Schritten.

[Link zur Gallery](https://yodarx.github.io/deep_art_gallery/)

## Schritte zum Hinzufügen eines Ergebnisses zur Galerie

1. Repository auschecken

    ```
    git clone https://github.com/yodarx/deep_art_gallery.git
    cd deep_art_gallery
    ```

1. Neuen Branch erstellen
    ```
    git checkout -b juergs_deep_art
    ```
1. Input-Bild sichern

   Speichere das Input-Bild (das Originalbild) im Verzeichnis `/data/input`.

1. Gewünschtes Style-Bild für den Transfer sichern

   Speichere das gewünschte Style-Bild (z. B. ein Picasso-Gemälde) im Verzeichnis `/data/style`.

1. Ergebnis-Bild generieren oder sichern

    * Wenn du bereits ein generiertes Bild hast, speichere es im Verzeichnis `/data/output`.

    * Alternativ kannst du das Bild auch mit dem Jupyter-Notebook `deep_art_gallery.ipynb` generieren. Es wird
      empfohlen, das
      Notebook in Google Colab mit T4-Ressourcen auszuführen, um die besten Ergebnisse zu erzielen.

1. Bild in Gallery hinzufügen

   Füge den folgenden Codeblock in die Datei index.html ein, um dein Ergebnis in die Galerie aufzunehmen. Platziere den
   Code über dem Kommentar:
   ```
   <!--  Add your images -->
   ```

   Füge dann diesen Codeblock hinzu:

   ```
   <figure onclick="openLightbox('Comparison 1: Picasso Style Transformation by Jeremy Rhodes', './data/input/eingabebild.png', './data/output/ausgabebild.png')">
       <div class="images">
           <img src="./data/input/eingabebild.png" alt="Source Image 1">
           <img src="./data/output/ausgabebild.png" alt="Generated Image 1">
       </div>
       <figcaption>Comparison 1: Picasso Style Transformation by Jeremy Rhodes</figcaption>
   </figure>   
   ```

1. Änderungen committen und pushen
1. Erstelle einen Pull Request um deine Änderungen in den main-Branch zu integrieren und dein Ergebniss in der Gallery
   zu sehen.