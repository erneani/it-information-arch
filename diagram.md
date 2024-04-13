# Polos Tecnológicos do Brasil

## Uma análise de Arquitetura da Informação

```plantuml
@startuml
package "Diagrama de Polos de Tecnologia no Brasil" #FFFFFF {
  class "Parque Tecnológico" {
    + Nome
    + Área de Atuação
  }

  class Governança {
    + Acordos
    + Leis
    + Resoluções
    + Regimentos
    + Documentações
  }

  class Serviços {
    + Pesquisa
    + Tecnologia
    + Capacitação
    + Infraestrutura
  }

  class Infraestrutura {
    + Investimento
    + Tipo
  }

  class Prêmio {
    + Nome
    + Ano
    + Instituição Provedora
  }

  class Instituição {
    + Nome
    + Tipo
    + Razão Social
    + Faturamento
    + Eficiência
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

  class Funcionário {
    + Nome
    + Identificador
    + Cargo
    + Salário
    + Tipo
    + Gênero
  }

  class Tecnologia {
    + Nome
    + Área
    + Campo do Saber
    + Investimento
  }

  "Parque Tecnológico" "1" --* "1" "Localização" : Fica em
  "Parque Tecnológico" "1" --* "1" "Governança" : Possui
  "Parque Tecnológico" "1" --* "many" "Infraestrutura" : Possui
  "Parque Tecnológico" "1" --* "many" Instituição : Possui
  "Parque Tecnológico" "1" --* "many" Serviços : Oferece
  "Parque Tecnológico" "many" --* "many" Prêmio : Recebe

  "Instituição" "1" --* "many" Funcionário : Possui
  "Instituição" "1" --* "many" Tecnologia : Desenvolve

  "Instituição" --* Pública : É uma
  "Instituição" --* Privada : É uma
  "Instituição" --* ONG : É uma
  "Instituição" --* PPP : É uma

  "Funcionário" --* Pesquisador : É um
  "Funcionário" --* Tecnólogo : É um
  "Funcionário" --* Professor : É um
  "Funcionário" --* Gerente : É um

  Tecnologia --* Método : É um
  Tecnologia --* Ferramenta : É uma
  Tecnologia --* Processo: É um
}
@enduml
```
