## Docker Komutları

### Genel Komutlar
- Docker daemon başlatılması  `docker -d`
- Docker yardım dosyası
`docker --help`
- Docker hakkında detaylı sistem bilgisi
`docker info`

### Images

- Dockerfile 'dan image oluşturma
`docker build -t <image_adı> .`
- Cache 'siz Dockerfile'dan Image oluşturma
`docker build -t <image_adı> . -no-cache`
- Lokaldeki image'ların listelenmei
`docker images`
- Bir image'ın silinmesi
`docker rmi <image_adı>`
- Kullanılmayan (container edilmemiş) Image'ların silinmesi
`docker image prune`

### Containers

- Bir image'dan container oluşturulması ve çalıştırılması
`docker run --name <container_adı>`
- Bir container'ın host'dan ulaşılacak port tanımlanmasının yapılması ve çalıştırılması
`docker run -p <host_port>:<container_port> <image_adı>`
- Container'ın arka planda çalıştırılması
`docker run -d <image_adı>`
- Bir container'ın başlatma ve durdurma
`docker start|stop <container_adı> (ya da container-id)`
- Durdurulmuş bir container'ın kaldırılması
`docker rm <container_adı>`
- Çalışan bir container'ın shell komut satırının aktif edilmesi
`docker exec -it <container_adı>`
- Çalışan bir container'ın log'larının izlenmesi
`docker logs -f <container_adı>`
- Çalışan bir container'ın bilgilerinin alınması
`docker inspect <container_adı> (ya da container-id)`
- Çalışan container'ların listelenmesi
`docker ps`
- Tüm container'ların listelenmesi
`docker ps --all`
- Çalışan container'ların kullanım (disk/memory/vb.) değerleri
`docker container stats`
