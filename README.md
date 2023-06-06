# Criação de Site em Nuvem
### Endereço da aplicação: https://brenomendesmoura.github.io/UNI.LIBRARY-Projeto/

<HR>

# Dados da Turma <br>
Dia da semana: Sexta Feira <br>
Período: Noturno <br>

### Integrantes

|RA| NOME COMPLETO| CURSO | TURMA |
| ------------ | ------------ | ------------ | ------------ |
|3021103570|Breno Mendes Moura|TADS|05A|
|3021100282|Victor de souza bernardo|TADS|05A|
|3021104031|Cesar Augusto Martins Vallim|TADS|05A|
|3021103269|Elias Yuri Yoshy Miyashiro|TADS|05A|
|3022201058|Acsa Cristina Sena|TADS|02A|
|3022200274|Matheus souza Martins|TADS|02A|

<hr>



https://user-images.githubusercontent.com/80074264/235515739-305f4a94-2c43-413a-951c-af9a2d480297.mp4



## Descrição do Projeto
UNI.LIBRARY, uma biblioteca digital especializada em Animes. Utilizando a mesma API do my anime list, realizamos requisições para que o usuário saiba as seguimentações e continuações dos animes que está sendo assistido. 
  No site nós retornamos informações relevantes para o mundo GEEK, como por exemplo:
  - EM ALTA, animes promovidos pela API e retornando em formato de vídeo;
  - ANIMES POPULARES, retornando os 30 animes com mais membros no forum do my anime list;
  - TOP 10 ANIMES, retorna os animes mais votados do momento;
  - ANIMES RECOMENDADOS, animes com as melhores avaliações do my anime list;
  - NOVIDADES, retornamos em formato de vídeo os animes recentes e mais visualizados do YOUTUBE.
  
 ### Idealização do projeto:
 O projeto foi idealizado no semestre passado, mas com requisições básicas e funcionalidades não tão exploradas. Nessa nova versão retornamos mais informações, mais funcionalidades e um front-end mais adequado ao tema proposto.
  
<hr>
  
#### Funcionalidades adicionadas:
- Adição de campo de pesquisa separado por categoria sem view_modal;
- Adição de traillers para ilustrar o anime categorizado no youtube em 1080p;
- Adição de um botão "Descubra" para retornar um anime aleatório;
- Adição de slides e scrolls automáticos com a função "smooth" em javascript;
  
<hr>
  
#### Alterações:
  
- Alteramos o fundo e cor de determinados elementos, utilizamos o site [colorhunt](https://colorhunt.co/) para observarmos as tonalidades;
  
- Alteramos todo o front end, desde o nav-bar até o footer. Montamos um front-end padronizado de acordo com o mercado de stream;


<hr>
  
## Utilização da API
  API: https://docs.api.jikan.moe/#tag/top/operation/getTopAnime
  <br>
  A api é gratuita, mas existe uma limitação na quantidade de requests por minuto.
  A requisição é padronizada e geralmente retorna os mesmos campos e varíaveis dentro do arquivo json,
  Caso você faça uma requisição nesse estilo
  ```javascript
var request = new XMLHttpRequest();

request.open('GET', 'https://api.jikan.moe/v4/anime/{id}/{request}/{parameter}');

request.onreadystatechange = function () {
  if (this.readyState === 4) {
    console.log('Status:', this.status);
    console.log('Headers:', this.getAllResponseHeaders());
    console.log('Body:', this.responseText);
  }
};

request.send();
```
  
  Receberá uma resposta como essa:
```javascript
`{
"data": [
{}
],
"pagination": {
"last_visible_page": 0,
"has_next_page": true,
"items": {}
}
}`
```
  
<br>
| Consequentemente deverá manipular essa informação e navegar utilizando .map para definir as variáveis que deverá aparecer no site.
| <br>
| Essa é uma das ideias iniciais ao desenvolver, uma maneira simples de explicar a requisição por trás,
| <br>
| Mas o script utilizado dentro do projeto vai um pouco além disso.
  
  


