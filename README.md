# room_occupancy_stimation
Room Occupancy Estimation

- Daniel Alejandro Yepes Mesa alejandro.yepes@udea.edu.co 
- Juan Felipe Santa Ospina juan.santa@udea.edu.co
- Cristian David Tamayo Espinosa cristian.tamayoe@udea.edu.co 



# Feature Selection and Model Training Pipeline

Este script implementa la fase de **reducción de dimensión**, **búsqueda de hiperparámetros** y **entrenamiento final** para el proyecto **Room Occupancy Estimation**, siguiendo un enfoque de **regresión ordinal con datos temporales**.

## Estructura

- Descripción de la metodología de validación y mallas de hiperparámetros.  
- **feature_selection_and_model_training.py**:  
  1. Carga y split temporal (fold único con todas las clases).  
  2. Análisis univariante (ANOVA, MI, Kendall Tau).  
  3. Selección de features (SFS con XGBoost).  
  4. GridSearchCV en 5 modelos (LogReg, k-NN, RF, XGB, MLP, SVM).  
  5. Evaluación de métricas ordinales (Kendall Tau, MAE, Adjacent Accuracy).  
  6. Entrenamiento final de XGBoost y exportación.

## Requisitos

- Python ≥ 3.8  
- pandas, numpy, matplotlib, seaborn  
- scikit-learn ≥ 1.0  
- xgboost  
- joblib  

# Ejecucion del proyecto en Docker

## Paso 1: Construir imagen
docker build -t room-occupancy-notebook .

## Paso 2: Ejecutar el contenedor
docker run -it -p 8888:8888 -v ${PWD}/app:/app room-occupancy-notebook



## Video de sustentacion: 

- https://drive.google.com/drive/folders/1bgq-rsaVKWx7oT0ak3rLfj3eqyQQRMOI?usp=sharing
