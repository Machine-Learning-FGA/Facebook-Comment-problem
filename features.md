# Features

O dataset apresenta 53 features divididas em 4 categorias da seguinte forma:

| Categoria | Essenciais| Página | Dia da seamana | Outros |
|--|:-:|:-:|:-:|:-:|
| **Quantidade** | 30 | 4 | 14 | 5 |

Cada categoria é detalhada a seguir.

##  Essenciais (30)

Nesta categoria, estão features que descrevem o padrão de comentários em diferentes intervalos de tempo. Das 30, 5 são diretamente relacionadas à contagem de comentários e são listadas a seguir. As outras 25 são derivadas das primeiras pelos cálculos de mínimo, máximo, média, mediana e desvio padrão para cada uma.

* **C1**: Contagem de comentários antes da data base selecionada
* **C2**: Contagem de comentários 24h após a data base selecionada 
* **C3**: Contagem de comentários 48h após a data base selecionada
* **C4**: Contagem de comentários nas primeiras 24h após a publicação do documento, mas antes da data base selecionada
* **C5**: Diferença entre C2 e C3

## Página (4)

Esta categoria agrupa as seguintes características da página:

* **Curtidas**
* **Categoria**
* **Checkins**
* **Talking About**: Contagem de usuários interagindo com a página; agrega diferentes atividades como comentários, curtidas em posts, compartilhamentos

## Dia da semana (14)

Estas features são indicadores binários para representar o dia da semana no qual o documento foi publicado e o dia da semana da data base selecionada, sendo 7 para cada.

## Outros (5)

Estas outras 5 características elencadas são relacionadas a:

* Tamanho do documento
* Intervalo de tempo entre a data de publicação e a data base selecionada para análise
* Promoção da publicação
* Contagem de compartilhamentos
