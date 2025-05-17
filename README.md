# 📊 Estatísticas de Partidas - League of Legends

Este projeto tem como objetivo registrar e analisar estatísticas pessoais de partidas no League of Legends, com foco em desempenho por campeão, rota e confrontos (matchups).

## 📁 Estrutura do JSON

O arquivo JSON armazena informações organizadas por campeão e inclui dados como rota, data de início, vitórias, derrotas e desempenho detalhado contra campeões adversários.

### 🧩 Estrutura genérica

```json
[
  {
    "nome-do-campeão": {
      "name": "string",
      "lane": "string",
      "startDate": "string (dd-mm-aaaa)",
      "win": number,
      "lose": number,
      "matchups": [
        {
          "nome-do-oponente": {
            "game-número": {
              "win": number,
              "lose": number,
              "anormal": "string",
              "dificultLane": "string (low | medium | high)",
              "date": "string (dd-mm-aaaa)",
              "kda": "string (ex: 9/1/7)"
            }
          }
        }
      ]
    }
  }
]
```

### 🔍 Campos disponíveis

- **name**: Nome do campeão (`string`)
- **lane**: Rota jogada (ex: `"mid"`, `"top"`, etc.)
- **startDate**: Data de início dos registros (`string`, formato `dd-mm-aaaa`)
- **win / lose**: Contadores de vitórias e derrotas (`number`)
- **matchups**: Lista de confrontos contra outros campeões

#### Dentro de `matchups`

- **nome-do-oponente**: Nome do campeão adversário
- **game-número**: Identificação da partida (ex: `game-1`, `game-2`)
  - **win / lose**: Resultado da partida (`number`)
  - **anormal**: Observações como `"jg quit"`, `"afk"` ou `"none"` (`string`)
  - **dificultLane**: Nível de dificuldade da lane (`"low"`, `"medium"`, `"high"`)
  - **date**: Data da partida (`string`, formato `dd-mm-aaaa`)
  - **kda**: Estatísticas de abates/mortes/assistências (`string`, ex: `"3/0/1"`)

## 📌 Objetivo

Este JSON serve para:

- Acompanhamento de performance por campeão.
- Estudo e análise de matchups específicos.
- Registro de observações importantes sobre cada partida.

## 🚀 Futuras melhorias

- Ferramenta para geração automática de gráficos.
- Interface visual ou dashboard.
- Filtros interativos por data, rota ou adversário.

## 📄 Licença

Este projeto está sob a licença MIT. Você pode usar, modificar e adaptar livremente.
