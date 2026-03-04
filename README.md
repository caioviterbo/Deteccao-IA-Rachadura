# 🧠 Sistema Inteligente de Detecção de Rachaduras Estruturais 

Sistema embarcado de **detecção e segmentação de rachaduras em tempo real**, desenvolvido para execução em **Raspberry Pi 5**, utilizando **Visão Computacional e Deep Learning**, com envio automático de **alertas via API REST e e-mail** quando uma anomalia crítica é identificada.

---

## 🎯 Objetivo do Projeto

Automatizar o processo de **monitoramento estrutural**, identificando **rachaduras em superfícies** (paredes, concreto, estruturas) de forma contínua e autônoma.

O sistema opera diretamente no dispositivo (**Edge AI**), reduzindo latência e dependência de servidores externos, sendo ideal para cenários de **monitoramento 24/7**.

---

## ⚙️ Funcionalidades

- 📷 Captura de vídeo em tempo real via **câmera CSI**
- 🧠 Detecção e **segmentação de rachaduras** com YOLO
- 🎯 Threshold mínimo de confiança configurável (≥ 80%)
- 📨 Envio automático de alerta para API externa
- 📧 Envio de e-mail com imagem anexada
- ⏱️ Controle de intervalo entre alertas (anti-flood)
- 🗂️ Configuração externa via arquivo YAML
- 🖼️ Visualização em tempo real com máscaras e bounding boxes
- 🔌 Operação contínua em dispositivo embarcado

---

## 🧱 Tecnologias Utilizadas

- **Python**
- **OpenCV**
- **YOLO (Ultralytics)**
- **NumPy**
- **Requests**
- **SMTP (Email)**
- **YAML**
- **Roboflow (Dataset e Treinamento)**

---

## 🖥️ Hardware Utilizado

- Raspberry Pi 5 — **8GB RAM**
- Câmera CSI oficial do Raspberry Pi
- Cartão microSD (32GB ou superior)
- Fonte oficial Raspberry Pi (5V / 5A)
- Sistema Operacional: **Raspberry Pi OS 64-bit**

---

## 📁 Estrutura do Projeto

configs/
device_config.yaml # Configurações do dispositivo e API

src/
main.py # Execução principal do sistema
predict.py # Inferência e visualização
api/ # Integrações auxiliares

data/
images/ # Dataset / imagens de entrada

results/
examples/ # Exemplos de detecções geradas

runs/
segment/ # Pesos do modelo YOLO (best.pt)

docs/
dataset.md # Informações sobre o dataset
model.md # Detalhes do modelo treinado

requirements.txt
README.md

