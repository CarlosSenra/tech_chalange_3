# Projeto Fiap Tech Chalenge 3

## Sobre o Projeto

Este projeto realiza uma **Análise Exploratória de Dados (EDA)** completa do dataset público de voos dos Estados Unidos, focando em **atrasos e cancelamentos**. O objetivo é entender os padrões operacionais da aviação civil e preparar os dados para modelagem de machine learning.

## Objetivos

- Compreender a estrutura e qualidade dos dados
- Identificar padrões temporais e sazonalidade
- Analisar atrasos e cancelamentos
- Investigar correlações entre variáveis
- Preparar features para modelos preditivos
- Ajustar modelos supervisionados e não supervisionados.

## Dados para o projeto

São utilizados três csv's:

| Arquivo | Descrição | Registros | Colunas |
|---------|-----------|-----------|---------|
| `flights.csv` | Dataset principal com dados de voos | 5.819.079 | 31 |
| `airlines.csv` | Informações das companhias aéreas | 14 | 2 |
| `airports.csv` | Informações dos aeroportos | 322 | 7 |

## Dicionário de variáveis

### Variáveis de Identificação

| Variável | Descrição | Tipo |
|----------|-----------|------|
| `AIRLINE` | Código da companhia aérea (ex: AA=American Airlines) | Categórica |
| `FLIGHT_NUMBER` | Número do voo | Inteiro |
| `TAIL_NUMBER` | Número de registro da aeronave | Texto |
| `ORIGIN_AIRPORT` | Código IATA do aeroporto de origem (ex: ATL) | Categórica |
| `DESTINATION_AIRPORT` | Código IATA do aeroporto de destino | Categórica |

### Variáveis de Horários (formato HHMM)

| Variável | Descrição | Unidade |
|----------|-----------|---------|
| `SCHEDULED_DEPARTURE` | Horário de partida programado | HHMM |
| `DEPARTURE_TIME` | Horário real de partida | HHMM |
| `WHEELS_OFF` | Horário em que o avião decolou | HHMM |
| `WHEELS_ON` | Horário em que as rodas tocaram o solo | HHMM |
| `SCHEDULED_ARRIVAL` | Horário de chegada programado | HHMM |
| `ARRIVAL_TIME` | Horário de chegada real | HHMM |

### Variáveis de Atrasos e Tempos (em minutos)

| Variável | Descrição | Observação |
|----------|-----------|------------|
| `DEPARTURE_DELAY` | Atraso na partida | Negativo = adiantado |
| `ARRIVAL_DELAY` | Atraso na chegada | Negativo = adiantado |
| `TAXI_OUT` | Tempo taxiando até a decolagem | Tempo no solo antes do voo |
| `TAXI_IN` | Tempo taxiando até o portão | Tempo no solo após pouso |
| `AIR_TIME` | Tempo efetivo no ar | Duração do voo |
| `SCHEDULED_TIME` | Tempo total programado | Duração planejada |
| `ELAPSED_TIME` | Tempo total real | Duração efetiva total |

### Variáveis de Distância

| Variável | Descrição | Unidade |
|----------|-----------|---------|
| `DISTANCE` | Distância entre origem e destino | Milhas |

### Variáveis de Status do Voo

| Variável | Descrição | Valores |
|----------|-----------|---------|
| `DIVERTED` | Indica se o voo foi desviado | 1=Sim, 0=Não |
| `CANCELLED` | Indica se o voo foi cancelado | 1=Sim, 0=Não |
| `CANCELLATION_REASON` | Motivo do cancelamento | A=Airline, B=Weather, C=NAS, D=Security |

### Variáveis de Tipos Específicos de Atraso (em minutos)

| Variável | Descrição | Quando Registrado |
|----------|-----------|-------------------|
| `AIR_SYSTEM_DELAY` | Atraso por controle de tráfego aéreo | Apenas quando ocorre |
| `SECURITY_DELAY` | Atraso por problemas de segurança | Apenas quando ocorre |
| `AIRLINE_DELAY` | Atraso causado pela companhia aérea | Apenas quando ocorre |
| `LATE_AIRCRAFT_DELAY` | Atraso por chegada tardia da aeronave | Apenas quando ocorre |
| `WEATHER_DELAY` | Atraso por condições meteorológicas | Apenas quando ocorre |


# Instalação

```bash
# Clonar repositório
git clone git@github.com:CarlosSenra/tech_chalange_3.git
cd tech_chalange_3

# Criar ambiente virtual
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate  # Windows

# Instalar dependências
pip install -r requirements.txt
```

## 👥 Autor

- [Carlos Rafael Senra Brito](https://github.com/CarlosSenra)

**Desenvolvido com ❤️ para o Tech Challenge Fase 3**
