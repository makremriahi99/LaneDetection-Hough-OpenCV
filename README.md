# Rilevamento Corsie Stradali — Trasformata di Hough + OpenCV

Sistema di **rilevamento delle corsie stradali** in tempo reale usando la Trasformata di Hough Probabilistica (`HoughLinesP`) di OpenCV, applicato a una foto di autostrada.

## Cosa fa

- Preprocessing dell'immagine (scala di grigi, sfocatura gaussiana)
- Rilevamento dei bordi con il filtro di Canny
- Applicazione di una maschera ROI (Region of Interest)
- Rilevamento delle linee con `HoughLinesP`
- Disegno delle corsie rilevate sull'immagine originale

## Come si usa

```bash
pip install opencv-python numpy
python lane_detection.py
```

## Tecnologie

- `OpenCV` — elaborazione delle immagini e Trasformata di Hough
- `numpy` — operazioni su array
- `matplotlib` — visualizzazione risultati

## Tag

`python` `opencv` `computer-vision` `lane-detection` `hough-transform` `image-processing`
