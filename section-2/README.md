
 Chyba bola v URL adrese, na ktoru chcel NGINX server smeroval poziadavky. 
 Ta bola nespravne zadana, kedze port aplikacie nie je 8080, ale 3000.



## Prevencia
- Pouzivat premenne prostredia (ENV) pre porty.
- Implementovat health checky v docker-compose.
