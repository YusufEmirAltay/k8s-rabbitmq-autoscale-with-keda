## 🧪 Görev: Minikube Üzerinde Flask + RabbitMQ + KEDA ile Otomatik Ölçekleme

Bu projede aşağıdaki adımlar takip edilerek Flask, RabbitMQ ve KEDA kullanarak Kubernetes üzerinde otomatik ölçeklenen bir sistem kurulmuştur:

1. Minikube cluster'ına RabbitMQ kur.
2. RabbitMQ servis bilgilerini (host, port, kullanıcı, şifre) not et.
3. Flask ile RabbitMQ'ya mesaj atıp aynı kuyruğu tüketen bir uygulama geliştir.
4. Uygulamayı Docker imajına çevir.
5. Minikube içindeki Docker ortamında imajı build et.
6. Flask uygulamasını Kubernetes'e deploy et (RabbitMQ bağlantı bilgileriyle).
7. Minikube cluster'ına KEDA kur.
8. RabbitMQ kuyruk uzunluğuna göre scale eden bir KEDA ScaledObject tanımı oluştur.
9. Uygulama içinden çok sayıda mesaj üretip kuyruğu doldur.
10. KEDA'nın uygulamayı otomatik olarak scale ettiğini gözlemle.
