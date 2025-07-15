# Flask + RabbitMQ + KEDA Autoscaling Demo 🐇⚙️🔥

Görev: Minikube Üzerinde Flask + RabbitMQ + KEDA ile Otomatik Ölçekleme





Minikube cluster'ına RabbitMQ kur.
RabbitMQ servis bilgilerini (host, port, kullanıcı, şifre) not et.
Flask ile RabbitMQ'ya mesaj atıp aynı kuyruğu tüketen bir uygulama geliştir.
Uygulamayı Docker imajına çevir.
Minikube içindeki Docker ortamında imajı build et.
Flask uygulamasını Kubernetes'e deploy et (RabbitMQ bağlantı bilgileriyle).
Minikube cluster'ına KEDA kur.
RabbitMQ kuyruk uzunluğuna göre scale eden bir KEDA ScaledObject tanımı oluştur.
Uygulama içinden çok sayıda mesaj üretip kuyruğu doldur.
KEDA'nın uygulamayı otomatik olarak scale ettiğini gözlemle.




