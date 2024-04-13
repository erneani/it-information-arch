# Polos Tecnológicos do Brasil

## Uma análise de Arquitetura da Informação

```plantuml
@startuml
package "Diagrama de Polos de Tecnologia no Brasil" #FFFFFF {
  class "Polo Tecnológico" {
    + Nome
    + Área de Atuação
  }

  class Localização {
    + Região
    + Estado
    + Município
    + Cidade
    + Bairro
    + Logradouro
    + Complemento
  }

  class Prêmios {
    + Nome
    + Ano
    + Instituição Provedora
  }

  "Polo Tecnológico" -> "Localização" : Está em uma
  "Polo Tecnológico" -> Prêmios : Recebe
}
@enduml
```
