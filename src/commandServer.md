```sh
curl --request POST \
  --url http://localhost:3333/account \
  --header 'Content-Type: application/json' \
  --data '{
	"cpf" : "12345678910",
	"name" : "Joselito sem Noção"
}'

curl --request GET \
  --url http://localhost:3333/statement \
  --header 'cpf: 12345678910'

curl --request POST \
  --url http://localhost:3333/deposit \
  --header 'Content-Type: application/json' \
  --header 'cpf: 12345678910' \
  --data '{
	"description": "Transferência",
	"amount": 3600.00
}'

curl --request POST \
  --url http://localhost:3333/withdraw \
  --header 'Content-Type: application/json' \
  --header 'cpf: 12345678910' \
  --data '{
	"amount": 100
}'

curl --request GET \
  --url 'http://localhost:3333/statement/date?date=2021-09-13' \
  --header 'cpf: 12345678910'

curl --request PUT \
  --url http://localhost:3333/account \
  --header 'Content-Type: application/json' \
  --header 'cpf: 12345678910' \
  --data '{
	"name" : "Boça"
}'

curl --request GET \
  --url http://localhost:3333/account \
  --header 'cpf: 12345678910'

curl --request DELETE \
  --url http://localhost:3333/account \
  --header 'cpf: 12345678910'

curl --request GET \
  --url http://localhost:3333/balance \
  --header 'cpf: 12345678910'
```