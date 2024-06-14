# [DIO](www.dio.me) - Trilha Java Básico

## Autores
- [Paulo Costa](https://github.com/paulowdev)

## POO - Desafio

### Modelagem e Diagramação de um Componente iPhone

Neste desafio, você será responsável por modelar e diagramar a representação UML do componente iPhone, abrangendo suas funcionalidades como Reprodutor Musical, Aparelho Telefônico e Navegador na Internet.

#### Contexto
Com base no vídeo de lançamento do iPhone de 2007 (link abaixo), você deve elaborar a diagramação das classes e interfaces utilizando uma ferramenta UML de sua preferência. Em seguida, implemente as classes e interfaces no formato de arquivos `.java`.

[Lançamento iPhone 2007](https://www.youtube.com/watch?v=9ou608QQRq8)
- Minutos relevantes: 00:15 até 00:55

#### Funcionalidades a Modelar
1. **Reprodutor Musical**
   - Métodos: `tocar()`, `pausar()`, `selecionarMusica(String musica)`
2. **Aparelho Telefônico**
   - Métodos: `ligar(String numero)`, `atender()`, `iniciarCorreioVoz()`
3. **Navegador na Internet**
   - Métodos: `exibirPagina(String url)`, `adicionarNovaAba()`, `atualizarPagina()`

### Objetivo
1. Criar um diagrama UML que represente as funcionalidades descritas acima.
2. Implementar as classes e interfaces correspondentes em Java (Opcional).

### Resultado do desafio - Diagrama UML (Mermaid)
```mermaid
classDiagram
    class IPhone {
        - String modelo
        - int capacidade
        + void tocar()
        + void pausar()
        + void selecionarMusica(String musica)
        + void ligar(String numero)
        + void atender()
        + void iniciarCorreioVoz()
        + void exibirPagina(String url)
        + void adicionarNovaAba()
        + void atualizarPagina()
    }

    class ReprodutorMusical {
        <<interface>>
        + void tocar()
        + void pausar()
        + void selecionarMusica(String musica)
    }

    class AparelhoTelefonico {
        <<interface>>
        + void ligar(String numero)
        + void atender()
        + void iniciarCorreioVoz()
    }

    class NavegadorInternet {
        <<interface>>
        + void exibirPagina(String url)
        + void adicionarNovaAba()
        + void atualizarPagina()
    }

    IPhone ..|> ReprodutorMusical
    IPhone ..|> AparelhoTelefonico
    IPhone ..|> NavegadorInternet
```
