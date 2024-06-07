# Instruções do teste

Crie um código html e javascript simples para manipulação de texto onde ao entrar com um texto com comandos, realizo alterações no texto e retorno um resultado.

Os comandos por caracteres são:

* h: para mover o cursos para a esqueda.
* l: para mover o cursor para a direita.
* r<char>: atualiza o caracter na posição atual pelo <char>.
* [N]h: move o cursor N caracteres para a esquerda.
* [N]l: move o cursor N caracteres para a direita.
* [N]r<char>: atualiza N caracteres, começando pela posição do cursor, pelo <char> e move o cursor de posição.

## Exemplos:
```
Entrada de texto: Hello Grupo Boticario
Comandos: hhlllllhihhi
Saída: Hello Grupo Boticario - cursor: 3

Entrada de texto: Hello Grupo Boticario
Comandos: rhllllllrgllllllrb
Saída: hello grupo boticario - cursor: 12

Entrada de texto: Hello Grupo Boticario
Comandos: rh6lrg6lrb2h
Saída: hello grupo boticario - cursor: 10

Entrada de texto: Hello Grupo Boticario
Comandos: 9999lrO
Saída: Hello Grupo BoticariO - cursor: 20

Entrada de texto: Hello Grupo Boticario
Comandos: 21rA
Saída: AAAAAAAAAAAAAAAAAAAAA - cursor: 20
```

# Explicação do Código:

### HTML:
* Cria um formulário com dois campos de entrada (texto e comandos) e um botão para executar a manipulação.
* Um elemento div com ID resultado para exibir a saída.

### JavaScript:
* A função manipularTexto() é chamada ao clicar no botão.
* A função pega os valores dos campos de entrada texto e comandos.
* A variável cursor inicializa a posição do cursor no início do texto.
* Um loop percorre cada caractere dos comandos:
  * h: Move o cursor para a esquerda.
  * l: Move o cursor para a direita.
  * r<char>: Substitui o caractere na posição do cursor pelo char.
  * [N]h: Move o cursor N caracteres para a esquerda.
  * [N]l: Move o cursor N caracteres para a direita.
  * [N]r<char>: Substitui N caracteres pelo char a partir da posição do cursor.

* O resultado final é exibido na div com ID resultado.

### Como Usar:
* Copie e cole o código HTML e JavaScript em um arquivo HTML.
* Abra o arquivo HTML em um navegador.
* Digite o texto no campo "Texto" e os comandos no campo "Comandos".
* Clique no botão "Manipular" para executar a manipulação e ver o resultado.


### Observações:
* O código assume que os comandos são válidos. Ele não valida a entrada para evitar erros.
* Você pode adicionar mais funcionalidades e validações ao código para torná-lo mais robusto.
O código é um exemplo básico e pode ser adaptado para atender a necessidades mais específicas.
