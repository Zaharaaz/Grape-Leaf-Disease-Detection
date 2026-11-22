# Grape Leaf Disease Detection (YOLOv12 + CBAM)

Object-detection model that identifies 2 classes of grape leaf disease,
with a Streamlit web app for interactive inference.

## Results
| Model | mAP@0.5 |
|-------|---------|
| YOLOv12 (baseline) | 81.9% |
| YOLOv12 + CBAM | 67.9% |

The baseline YOLOv12 was selected as the final model.
CBAM showed higher confidence on some samples in the web app,
but lower overall mAP.

## Dataset
- 1,736 images, 2 classes: downey mildew and black rot with 1 healthy class 
- Preprocessing: cleaning, resizing, orientation standardization
- Source: primary data and public dataset from Mendeley data
  ([dataset 1](https://data.mendeley.com/datasets/wkymf8bhcg/5),
  [dataset 2](https://data.mendeley.com/datasets/378c69nwk5/1))

## Tech
Python, PyTorch (Ultralytics YOLOv12), CBAM, Streamlit

## How to run
Open the training notebook in Google Colab or Jupyter
and run the cells in order.

## Demo
![detection example] (demo.png)

## Web App Repo
https://github.com/Zaharaaz/Deteksi-penyakit-daun-anggur

## Notes
CBAM likely underperformed because small dataset
and newly added layers not pretrained. Not yet verified with
multiple seeds.
