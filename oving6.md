Vi er nå blitt kjent med Heroku- Målet er å få en "Hello world" spring booot applikasjon opp å kjøre
på platformen, og få automatisk deployment, hver gang vi pusher endringer til master branch i GIT.

_*[Dere kan bruke Repository](https://github.com/PGR301-2018/heroku_example) som utgangspunkt. Dere kan gjøre git clone, kopiere filene til egen katalog, og fjerne .git katalogen.

* Dere skal lage et eget *privat* GitHub repository og sjekke inn disse filene der. Dere må erstatte verdier i pipeline.yml filen, som er laget for dette eksempel repoet.

# Hemmeligheter Concourse trenger

## Github token & Nøkkelpar

For å sjekking om ny versjon av kode er tilgjengelig, og for å gjøre andre API kall. Trenger Concourse "Resource" med navn "git" et token. Lag et Personal Access Token, og ha dette klart.
For å pushe kode (terraform state) til dit eget repo, må du lage en [deploy key med write access](https://developer.github.com/v3/guides/managing-deploy-keys/)

## Heroku API Key

Heroku API Key kan lett finnes under account settings / i Heroku

## Credentials.yml

Kopier disse hemmelighetene inn i en credentials.yml fil

```yaml

github_token=182da69697ca8c7ce12360669c72983716d64550
github_key = |
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEA0ehcT11UEPQtffohtr4h91u9v706UX+8newdlZq2VRMnKusd
MRTb6ONJfbd+xz3yYYhzZY2NID19PGPM/t0BKJZrvtJJH4S7/1VB3aZTzntk9kb7
oYt43pN9PGHvCrV7o7ssHkOZ4RslY9s1bpsuG6WCGzkyzFraNj0X5mZ/5NpsmEqU
R1JWCWwHBptCwzAF1Wg1RN012121wzdsdcfDDSDS+mrO08YnRooyID27+BEr2LA9
n556nZrgi3PUtnwKmelcrRY1v97JZAXqIM69y3RBfqJISRV5w7HsRQA12tn3PgfE
b+zGcq+hC+GOWR86g749C1zAYBbKY9blN3R9+wIDAQABAoIBAQC4qZlj/K/zRk0r
Mb0tHjGVgjD5GIjQn/aYW9te/L+BMptXh4Wj4zzfsey6W459y8KLCVaztYa9ITsm
wIncgSL+yO467paD0urs4t1SGHxL/4Q/oQzH/oI0FT6su19nZWdDEGvsp/4c6hvH
sFZeWsiCa+V8+6Hz481qv+5htDS5Z9KwQPJunXcItbknuKguUEMpYCd9xz9g1D4s
iLqpQRph8YLxjRPZJ4obA5dAEdBgRta/FtG8RIb4Jnbn1Ds6MH5SoWikZp3AVoMR
BZO4RflL9aplEVuKUVtKj+gC48QkUswceePpF+uRGmVYJknmTLFqFtLxt31NJQUN
BxGMS0KxAoGBAPJrD9J+JTkarYo9DNgk9XP4qg/rePG2kDPKzrQii4LrN97joxvz
gluy+72FZ0WFw0OGwwif0SDw3On4D2QddifgWMNpN9GM0sBGRq2Kl0kjaCahE7RP
57j1UdP+x1FIjDYJgEUkts2W/o7nHmAlHTyrxT5tmWtcG261+sNKgH5pAoGBAN2r
AkG7dx+4Y2ADSMSSg3isssZuX3DtnZfkwE00hKyGMskaPkt52GhgFSAvSpAsMm1N
8hZscIEq2c611Ztpq2DxCr0W61xOD19y/LnL+b0e8VwqDu7JLjm9a/qMTGzYbZtX
pHV/r5hiv+LHC25n6UCEyxCh2JidZyAeNtxxlBTDAoGABKNzzA1J3QvbojeE1WXv
pGZvqppQ2B8sJzGMPvoiPUEO8p7cch54shR8qKWy0iu7DsG3XaThNYYmU/vBH6NI
rX6ndCXBQas2JSOzGoL6XhXlWkfevqaAwpM/G5VWbwG6XRZVc/092jU3bbiSZjiP
lKecwJMMSneatsWYpL/6MXECgYEAy04pB7i0jTdEja71crUeN/PNFAnvJ1gIDmQT
q7vbY5DBy4hyUi8yuKhHN/mn3YtrxKyUuNREa3OtyNUlUSEdug/Z1YvL2iEOIHEK
Mi5Oo5JZtDou7/s8lmCRRH6hKcNm4+8CO3Iczxri+0+rwFs1p6Mjy+FlErRq/R45
Gv5g3pkCgYBnvRQ1b3s5eddyOUz5iYW/Vshh8Hr73ZlzjIaS7N7x5u5K48Xv1C2g
Hcn1QWh0zj69EcwhmG99DdVg8XXtpSv7GQoBRIhS3qg5UbNGPAexmx+k9pDsWW04
zblEIppkjFxJcc0srC65PSDpCvKa6UrOOik3Bt4u4Rh1NYZ4u/+Rvg==
-----END RSA PRIVATE KEY-----

heroku_email=glenn.bech@gmail.com
heroku_api_token=1fceedcc-5a37-4781-9416-8c4ddf61f59b


```