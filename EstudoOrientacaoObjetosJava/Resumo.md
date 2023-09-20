# Assuntos

- Conceito de POO
- Pacotes e Visibilidade de recursos
- Classes e Construtores
- Java Beans e UML
- Pilares do POO
- Enums e Interfaces

# Conceitos de POO

Á medida que a tecnologia vem evoluindo, as linguagens de programação também.

Linguagem de baixo nível --> Linguagem próximo as linguagens de máquina
Linguagem de alto nível  --> Disponibiliza proposta de sintaxe (forma de escrita) mais próxima da interpretação humana. Ex: Java, JavaScript, Python e C++.

Exemplo de Hello World

Python 

```
print("Hello, world");

```

Assembly 

```
; Exemplo de um Hello World em Assembly
; ld -m elf_i386 -s -o hello hello.o
section .text align=0

global _start

mensagem db 'Hello world', 0x0a

len equ $ - mensagem

_start:
    mov eax, 4 ;SYS_write
    mov ebx, 1 ;Número do file descriptor (1=stdout)
    mov ecx, mensagem ;Ponteiro para a string.
    mov edx, len ; tamanho da mensagem
    int 0x80

    mov eax, 1
    int 0x8

```
Em uma simples linha executa uma operação que em uma outra linguagem como Assembly utilizaria-se muitas linhas e com complexidade muito maiores.

## Programação estruturada 

Paradigma da programação que visa melhor clareza, a qualidade e o tempo de desenvolvimento de um programa de computador, fazendo uso das construções de fluxo de controle estruturado (if/then/else) e repetições (while e for), com estruturas de blocos e sub-rotinas.

# A programação estruturada 

Permite implementar algoritmos com estruturas sequênciais denominados procedimentos lineares que podem afetar valores de variáveis de escopo local ou global.

# A porgramação orientada a objetos

POO é um paradigma de programação baseado em conceito de "objetos" que podem conter dados dna forma de campos, conhecidos como atributose códigos na forma de procedimentos conhecido como métodos, permite abstrair cenários do mundo real e criar e converter em algoritmos de fácil compreenção e fácil reutilização.

# Em Java 

Os arquivos são distribuídos com extensão .java denominados classe.
As classes são compostas de:
Identificador, Caracteristicas e Comportamentos

```
    
    public class nomeClasse{

    }

```

- Classe (class) Representa a criação de objetos
- Identificador (identity) Propósito existencial
- Caracteristicas (states) Representam os atributos 
- Comportamentos (behavior) Ações ou métodos 
- Instanciar (new) Ato de criar um objeto a partir da estrutura definida da classe/objeto constroi um objeto que representa o contexto da classe.

Class Students --> states(atributos) --> behaviors --> (métodos/comportamentais)
--> instancias(new Students) --> contém uma represntação completa desse mapa.

# As classes correspondem a estrutura dos objetos.

Tipos de classes

- Classe de modelo(model) representam o domínio da aplicação ex: Cliente, Pedido etc...
- Classe de serviço (service) Contém as regras de negócio e validação de nosso sistema
- Classe de repositório (repository) Contém a integração com banco de dados.
- Classes de controle (controller) Disponibilizar alguma comunicação externa http/web/webseriveces/api(s).
- Classe utilitária (util) Contém recursos comuns à toda aplicação.

# Pacotes

Os pacotes ou (packages) É uma alternativa de organização do projeto com a finalidade de facilitar a busca por arquivos durante a manutenção do projeto.

Os packages sao sub-diretórios a partir da pasta src do projeto. 

Convensão/sugestão ao criar pacotes imaginando que a empresa chama-se PowerSoft

- Comercial: com.powersoft
- Governamental: gov.powersoft
- Código aberto: org.powersoft

Mediante a finalidade da classe criamos então os pacotes model, repository, service, controller etc.
Esses sub-pacotes por convensão serão criados 
ex: 
com.powersoft.model com.posersoft.service.Usuario
com.powersoft.controller.UsuarioController

A localização de uma classe é definida pela palavra reservada:

```
    package
    import ...
    import ...

    public class MinhaClasse{
        //atributos metodos e códigos.
    }

```

# Observação para trabalhar com o eclipse

Precisamos configurar a jdk em Window-->Preferences--> JRE Definition















