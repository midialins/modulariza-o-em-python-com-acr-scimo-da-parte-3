Python para SO – Modularização

Repositório desenvolvido para a disciplina de Sistemas Operacionais, com foco em modularização em Python, procedimentos, funções, passagem de parâmetros e execução dos programas em Docker.

Linguagem: Python

Versão utilizada no Docker: Python 3.10.20

Objetivo

Praticar a organização de programas Python utilizando:
- procedimentos sem retorno;
- funções com retorno;
- passagem e ausência de passagem de parâmetros;
- variáveis globais e locais;
- função main();
- modularização;
- recursividade;
- execução dos programas em contêiner Docker.
- 
Parte 1 – Modularização em Python

Exercícios 18 a 26

Refazer os exercícios utilizando procedimentos sem retorno e sem passagem de parâmetros, com uso de variáveis globais.

Os programas devem ser organizados com:

def main():
    # programa principal
    pass

if __name__ == "__main__":
    main()

Arquivos correspondentes:
- Ex18.py
- Ex19.py
- Ex20.py
- Ex21.py
- Ex22.py
- Ex23.py
- Ex24.py
- Ex25.py
- Ex26.py

Exercícios 27 a 29

Refazer os exercícios utilizando procedimentos com passagem de parâmetros, trabalhando com variáveis locais.

Arquivos correspondentes:
- Ex27.py
- Ex28.py
- Ex29.py

Exercício 3a – Fatorial

Criar uma função que:
- receba um valor inteiro como parâmetro;
- calcule o seu fatorial;
- retorne o resultado.
O main() deve solicitar o valor ao usuário, chamar a função, armazenar o retorno em uma variável e exibir o resultado.

Exemplo da função:
def fatorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * fatorial(n - 1)

Arquivo:
- 3a.py

Exercício 3b – Série com fatorial

Modificar o exercício 3a e acrescentar uma função que receba dois parâmetros inteiros e retorne a divisão do primeiro pelo segundo.

def divisao(a, b):
    return a / b
O programa solicita o valor de N e utiliza as funções para calcular:
\[
1 + \frac{1}{1!} + \frac{1}{2!} + \frac{1}{3!} + \cdots + \frac{1}{N!}
\]

Arquivo:
- 3b.py

Parte 2 – Docker

Criar um contêiner utilizando a imagem:
python:3.10.20

O diretório dos exercícios da Parte 1 deve ser mapeado como volume para dentro do contêiner.
Exemplo:
docker run -it --name python_modularizacao -v "$(pwd)":/app -w /app python:3.10.20 bash

Dentro do contêiner, um exercício pode ser executado com:
python Ex18.py
ou:
python 3a.py

Para acessar novamente o contêiner criado:
docker start -ai python_modularizacao

Evidências da execução
Para a entrega da Parte 2, devem ser registrados prints mostrando:
1. o comando utilizado para criar o contêiner Docker;
2. o comando utilizado para executar o contêiner;
3. a aplicação Python sendo executada no terminal.
Os prints podem ser adicionados posteriormente ao repositório em uma pasta como:
prints/
Exemplo:

Modularizacao_Python/
│
├── prints/
│   ├── docker_criacao.png
│   ├── docker_execucao.png
│   └── programa_em_execucao.png
│
└── ...
Conceitos trabalhados

Este projeto pratica principalmente:
- modularização;
- funções e procedimentos;
- passagem de parâmetros;
- variáveis globais e locais;
- retorno de valores com return;
- estrutura main();
- recursividade;
- estruturas de repetição;
- Docker e mapeamento de volumes.

