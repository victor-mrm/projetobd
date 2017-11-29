# projetobd

Perguntas:


1- Verificar a conversa entre o usuário 1 e 2 e mostrar a data.


2- Mostrar todos os amigos do usuário 1.

3- Mostrar historicos das mensagens enviadas na 05/08/2017.


4- Mostrar a quantidade de mensagens enviadas no total.


5- Mostre o nome de todos os usuário com email "webnode".


6-Mostre o nome de todos os usuários que são amigos do usuário de id 1.


```sql
select usuario.nome, amizade.usuario_id1

from amizade

inner join usuario

on usuario.id = amizade.usuario_id1

where amizade.usuario_id = 1;
```


7-Mostre o nome de todos os usuários que  NÃO são amigos do usuário de id 1.


```sql
select id,nome,status from usuario where id not in(select usuario.id
from amizade

inner join usuario

on usuario.id = amizade.usuario_id1

where amizade.usuario_id = 1 or amizade.usuario_id1 = 1 ) and id <> 1;
```

