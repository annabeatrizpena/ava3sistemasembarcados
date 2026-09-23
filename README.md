# Sistema de Sinalização de Parada para Ônibus com CPLD

## Descrição

Este projeto apresenta o desenvolvimento de um sistema de sinalização de parada para ônibus, utilizando um sistema embarcado para controlar LEDs, um buzzer e dois botões. O sistema simula a solicitação de parada realizada por um passageiro. Ao pressionar o botão de parada, uma indicação visual e sonora é acionada. O LED amarelo permanece aceso enquanto a solicitação estiver ativa, enquanto o buzzer emite um alerta sonoro durante três segundos. Quando a porta do ônibus é aberta, a solicitação é considerada atendida e o sistema retorna ao estado inicial.

## Componentes utilizados

* STM32L031K6
* LED amarelo
* LED azul
* Buzzer
* Botão de solicitação de parada
* Botão de abertura da porta
* Resistores para os LEDs

## Ligações

| Componente                | Pino |
| ------------------------- | ---- |
| LED amarelo               | D2   |
| LED azul                  | D3   |
| Buzzer                    | D4   |
| Porta / botão de abertura | D5   |
| Botão de parada           | D6   |

Os dois botões são configurados como entradas digitais utilizando `INPUT_PULLUP`. Dessa forma, permanecem em estado **HIGH** normalmente e o acionamento é identificado quando o sinal passa para **LOW**.

## Funcionamento

O sistema possui três estados principais.

### 1. Estado inicial

Ao iniciar o sistema, o **LED azul permanece aceso**, indicando que o sistema está aguardando uma solicitação de parada.

### 2. Solicitação de parada

Quando o passageiro pressiona o **botão de parada**, o sistema registra a solicitação.

### 3. Solicitação atendida

Quando o botão que representa a **abertura da porta** é acionado, o sistema entende que a solicitação foi atendida.

## Simulação

A simulação foi realizada no Wokwi (https://wokwi.com/projects/475967892306044929) para verificar o comportamento do sistema nos diferentes estados de funcionamento. 

## Referências

WOKWI. Wokwi: online electronics simulator. Wokwi B.V., [s.d.]. Disponível em: https://wokwi.com/. Acesso em: 23 set. 2026. 

## Autora

Anna Beatriz Pena
