# Learning API Gateway

API Gateway berfungsi menjembatani client app dengan backend services.
Bayangkan jika kita punya suatu system yang dibangun diatas beberapa service misalnya:

- accounts.mystore.com
- catalogs.mystore.com
- orders.mystore.com

Daripada kita buat beberapa koneksi, Lebih baik kita buat satu koneksi melalui API Gateway.
Selain itu jika lewat API Gateway kita bisa menambahkan fitur authentication dan authorization untuk membedakan client dari web, Android App, dll.
Melalui API Gateway kita juga bisa membatasi request yang kita terima. Contoh fitur lainnya bisa dilihat dari gambar dibawah ini:

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

## API Gateway using KrakenD

## Learning From Books

- [Kong: Becoming a King of API Gateways](https://www.amazon.com/Kong-Becoming-King-API-Gateways-ebook/dp/B07BZG7GPG)



[kong-url]: https://konghq.com/
[kong-benefits]: https://konghq.com/wp-content/uploads/2018/05/kong-benefits-github-readme.png