# Learn API Management

API Gateway berfungsi menjembatani client app dengan backend services.
Bayangkan jika kita punya suatu system yang dibangun diatas beberapa service misalnya:

- accounts.mystore.com
- catalogs.mystore.com
- orders.mystore.com

Dan semua service perlu authentication karena kita ingin mempublikasi API. 
Biasanya kita membuat satu persatu authentikasi disetiap service.
Dengan API gateway kita bisa menyatukan semuanya, seperti pada gambar dibawah ini.

[![][kong-benefits]][kong-url]

Gambar diatas diambil dari github [kong](https://github.com/Kong/kong), kong adalah salah satu API Gateway opensource.

Seperti pada gambar, API Gateway akan intercept request yang akan masuk kedalam service kita. 

- Authentication
- Monitoring
- Logging
- Security
- ACL
- Caching
- Rate-Limiting

Yang dimana biasanya kita menghandle dilevel service, sekarang tugas itu dipindahkan ke API Gateway.

Beberapa API Gateway / API Management:

- [Kong](https://konghq.com/)
- [KrakenD](https://www.krakend.io/)
- [TYK](https://tyk.io/)
- [IBM API Connect](https://developer.ibm.com/apiconnect/)
- [APIGEE](https://cloud.google.com/apigee)
- [AWS API Gateway](https://aws.amazon.com/api-gateway/)

## API Gateway using Kong

[Kong API Gateway](https://github.com/Kong/kong)

### Install Service & Kong & Konga

```cmd
  cd deployments
  docker-compose up -d
```

## API Gateway using KrakenD

## Learning From Books

- [Kong: Becoming a King of API Gateways](https://www.amazon.com/Kong-Becoming-King-API-Gateways-ebook/dp/B07BZG7GPG)
- [How to Build an Effective API Strategy in 2021](https://nordicapis.com/how-to-build-an-effective-api-strategy-in-2021/)

## What did I learn

Sempat bingung istilah-istilah bahkan ketuker-tuker antara API Gateway, Reverse Proxy, Load Balancing, API Management.

### Load Balancer

Load Balancer bertugas mendistribusikan request yang datang ke beberapa server secara acak.
maksudnya apa, biasanya satu fitur service yang sama bisa ada dibeberapa server.
kenapa begitu? ya karena 1 server saja tidak cukup untuk menerima semua request yang datang.
Dengan menggunakan load balancing, kita bisa membagi request ke beberapa server berbeda.

### Reverse Proxy

Reverse Proxy bertugas sebagai "public request", ini adalah garda terdepan dari aplikasi yang diakses lewat internet.
Fitur ini ada pada setiap webserver, yang digunakan untuk meneruskan ke port lain dari public request ke server kita.

### API Gateway

API Gateway bertugas menjembatani request yang masuk seperti authentication & authorization, rate limiting, dll.

<!-- TODO: cari penjelasan yang lebih bagus -->

### Service Mesh

Service Mesh atau SideCar Proxy Pattern adalah layer proxy tambahan pada service. 
Service Mesh menyediakan `Critical Capability` seperti service discovery, load balancing, encryption, observability, 
traceability, authentication and authorization, and support for the circuit breaker pattern.

### Reference

- [What is a Reverse Proxy vs. Load Balancer?](https://www.nginx.com/resources/glossary/reverse-proxy-vs-load-balancer/)
- [What Is a Service Mesh?](https://www.nginx.com/blog/what-is-a-service-mesh/)


[kong-url]: https://konghq.com/
[kong-benefits]: https://konghq.com/wp-content/uploads/2018/05/kong-benefits-github-readme.png
