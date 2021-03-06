<h1 align="center">
  json-server-hamburgueria
</h1>



<p align = "center">
Este é o backend da json-server-hamburgueria.
</p>




## **Endpoints**

## Rotas que precisam de autenticação

<h2 align ='center'> Login do usuário </h2>

`POST /login - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "mateus@mail.com",
  "password": "123456"
}
```

`POST /login - FORMATO DA RESPOSTA - STATUS 200`

```json
{
  "accessToken": "qKkZgqleRKAiqvze3MssflsAaBKBB6.eyJlbWFpbCI6ImpvYW8uc2lsdmFAbWFpbC5jb20iLCJpYXQiOjE2MqKkZgqleRKAiqvze3MssflsAaBKBB6QwMCwic3ViIjoiMSJ9.TU5DIB-qKkZgqleRKAiqvze3MssflsAaBKBB6-6jAgg",
  "user": {
    "email": "mateus@mail.com",
    "name": "mateus alves",
    "role": "administrador",
    "id": 1
  }
}
```

<h2 align ='center'> Criar usuário </h2>

`POST /signup - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "jorge@mail.com",
  "password": "123456",
  "name": "jorge guerreiro",
  "role": "usuario"
}
```

`POST /signup - FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InBhdWxvLmZvbnRlc0BtYWlsLmNvbSIsImlhdCI6MTYzNjUzOTAxNywiZXhwIjoxNjM2NTQyNjE3LCJzdWIiOiI0In0.GdiQ0TlmvptXKz9yVSyJK--AJkVoHz2Z8qA-cU9aPbo",
  "user": {
    "email": "jorge@mail.com",
    "name": "jorge guerreiro",
    "role": "usuario",
    "id": 2
  }
}
```

<h2 align ='center'> Listar Produtos </h2>

`GET /products - FORMATO DA RESPOSTA - STATUS 200`

```json
[
  {
      "image": "https://lh3.googleusercontent.com/pw/AM-JKLVzsMug4UtoDzPlo-kCV8xuZChu2NnL05EZUbAnQZn9pPIWflNblkj_j26ANTyzN8gtdEC9PBuGm96NP2eVXtCeuRDrT4HG7HZj5GvhUbCjBNGz9RyL0D2zT_lFis8u1lMw9P582mxFV80jtOKiG-bW=w158-h150-no?authuser=0",
      "name": "Big Kenzie",
      "category": "Sanduíches",
      "price": 19.99,
      "id": 1
    },
    {
      "image": "https://lh3.googleusercontent.com/pw/AM-JKLWCvLcj48eToZuoLpJH6tI40XkZ6sEy70X0sn5xr2veJJio9AbS75a6Ll4jeixtwfuBtAsiRrB6hZxGC1y00Ru2SlUN9iUYwC618z5V4irkPYETn7G7P-EhCYOcHYO9P1pm917Vl6JPVzLvyPZ792sD=s162-no?authuser=0",
      "name": "X-Burguer",
      "category": "Sanduíches",
      "price": 10.99,
      "id": 2
    },
    {
      "image": "https://lh3.googleusercontent.com/pw/AM-JKLWF8mTqijbuKflKozJH2oGJoJZ17zNuXmAGyxM6PC89j42q8-fKZxNcB0kPwpj3jjk17_VIhFXoEjrQ8nlZULhycfdpANt_nYTn3cATg9iAr5YSIzzEViSrTceBbtokyRquqN-0c-Ud3_GmgoMsa2df=w177-h162-no?authuser=0",
      "name": "X-Chicken",
      "category": "Sanduíches",
      "price": 14.99,
      "id": 3
    },
    {
      "image": "https://lh3.googleusercontent.com/pw/AM-JKLX_z8CJ-gjv7Zq-Ncql8Z_jQ1CdJ0_BX_A2CF8vthQ5WfIGJtHXsbuPIJzxFsIpqQdXum__foayg48ey8URMdEzr7E0qNkcHi4vDcX7WE_pt7ktiS2anREaBff5GVpWRMXCOtK076XaAKBX0LwGva9L=w170-h150-no?authuser=0",
      "name": "Combo Kenzie",
      "category": "Sanduíches",
      "price": 20.99,
      "id": 4
    },
    {
      "image": "https://lh3.googleusercontent.com/pw/AM-JKLUQjqBgtLWQ-DFrfUU4k4ETdIDZiAjsNyWdLKkBH85fC9DxgWNgkDPxaKWSpZQ_XpQVhnAe5RuZqkpL08cJB-HGIurhorD8z5kSNrM1Hb_5a3IZbNrOR2mnEwC-WYo20w3weckbStxt3TO-EuK0zSrn=w247-h167-no?authuser=0",
      "name": "Fanta Guaraná",
      "category": "Bebidas",
      "price": 5.99,
      "id": 5
    },
    {
      "image": "https://lh3.googleusercontent.com/pw/AM-JKLU-KdfLBqnfV-ZZzQzrX-7PpvwMqCZ0AG_6TebhiFCDlBRS8yV4j0YWGYjUUwg_fgVcrd9sFfzDtTB3h3029j_4yH4-4Jrylhns4Cap9ALT2aKBOej7s9q9Xd_YECuaaLfWfQlSFOfLRgqWvQaeiOiL=w247-h172-no?authuser=0",
      "name": "Coca Cola",
      "category": "Bebidas",
      "price": 6.99,
      "id": 6
    },
    {
      "image": "https://lh3.googleusercontent.com/pw/AM-JKLWF4LPVhA1pLUxp_FOL8wp5WaDXVjL5_JBHbuHLyiEx1XjzE5T8EJs5B0KoiXZPVdNn2gCwSjeaXH5T8O27cR7EWXivdoe1QQQymspuHyZCfyC6oJG8ZA9h6yhWr0Pr6TVf_X86K4kf37-wvgxpIWdN=w162-h144-no?authuser=0",
      "name": "McShake Ovomaltine",
      "category": "Sobremesas",
      "price": 18,
      "id": 7
    },
    {
      "image": "https://lh3.googleusercontent.com/pw/AM-JKLV8CReP_8yXBE5tBqOunyxws5O6zlRq3Mky8Pn8KUT2mdsrgM5q3U6Zu9dAV5DOghKVAXbZrjF4Sd9nXoYSXd-Eh2_2DTNlTmSBhbf7k-rcOL7s9phSpPpCpQNIsakosg9WvxsfHMh6WeXLN-_Pyt63=s140-no?authuser=0",
      "name": "Sundae Chocolate",
      "category": "Sobremesas",
      "price": 12.99,
      "id": 8
    }
}
```

`POST /carts - FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "userId": 1,
  "products": [
    {
      "title": "Big Kenzie",
      "category": "sanduiches",
      "price": 91.9,
      "id": 1
    }
  ],
  "id": 1
}
```

<h2 align ='center'> Apagar carrinho </h2>

`DELETE /carts/:id - FORMATO DA RESPOSTA - STATUS 200`

```json
{}
```
