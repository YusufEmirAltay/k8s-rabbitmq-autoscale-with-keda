# Flask + RabbitMQ + KEDA Autoscaling Demo 🐇⚙️🔥

Bu proje, Kubernetes ortamında çalışan bir Flask uygulamasının, **RabbitMQ kuyruk uzunluğuna bağlı olarak KEDA ile otomatik olarak ölçeklenmesini** (autoscaling) sağlar.

## 🚀 Proje Bileşenleri

- **Flask:** HTTP endpoint üzerinden mesaj üretir ve RabbitMQ kuyruğuna gönderir.
- **RabbitMQ:** Mesaj kuyruğunu tutar.
- **KEDA:** Kuyruk uzunluğunu izleyerek Flask consumer pod'larını otomatik ölçekler.

---

## 📂 Proje Yapısı
├── app.py # Flask app + RabbitMQ consumer (thread ile)
├── Dockerfile # Uygulama imajı
├── requirements.txt # Flask, pika
├── deployment.yaml # Flask deployment + service
├── scaledobject.yaml # KEDA ScaledObject tanımı
├── secret.yaml # RabbitMQ kullanıcı bilgileri

---

## 🛠️ Kurulum ve Çalıştırma

### 1. Gerekli bileşenleri yükle

> Projeyi deploy etmeden önce RabbitMQ çalışıyor olmalı. Minikube ortamı için Bitnami RabbitMQ Helm Chart kullanılabilir.

```bash
# RabbitMQ kurulumu (Helm ile)
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install my-rabbitmq bitnami/rabbitmq
