# 🍷 Projeto de Monitoramento Ambiental para a Vinheria Agnello

Este projeto foi desenvolvido como parte do Checkpoint 02 da disciplina de **Engenharia de Software – Edge Computing & Computer Systems** da FIAP. O objetivo é monitorar as condições ambientais (luminosidade, temperatura e umidade) da Vinheria Agnello, garantindo a conservação adequada dos vinhos e proporcionando uma experiência digital semelhante à loja física.

## 📋 Descrição do Projeto

A Vinheria Agnello deseja expandir sua atuação para o meio digital com um sistema que simula o atendimento presencial e, ao mesmo tempo, garanta o controle ambiental ideal para conservação dos vinhos.

O sistema implementado realiza o monitoramento em tempo real dos seguintes parâmetros:

- **Luminosidade**
- **Temperatura**
- **Umidade**

Com base nas leituras dos sensores, o sistema exibe informações em um **Display LCD** e aciona **LEDs** e um **Buzzer** como alertas visuais e sonoros.

## 🛠️ Tecnologias Utilizadas

- Plataforma de simulação: [Wokwi](https://wokwi.com/)
- Microcontrolador: Arduino UNO
- Sensores:
  - Sensor de luminosidade (LDR)
  - Sensor de temperatura e umidade DHT11 ou DHT22
- Atuadores:
  - LEDs (vermelho, amarelo, verde)
  - Buzzer
  - Display LCD (com ou sem módulo I2C)
- Linguagem: C++ (Arduino IDE)

## ⚙️ Funcionalidades do Sistema

### Luminosidade

| Nível de Luz      | LED         | Display                | Buzzer |
|-------------------|-------------|-------------------------|--------|
| Escuro            | Verde       | -                       | Off    |
| Meia luz          | Amarelo     | "Ambiente a meia luz"  | Off    |
| Muito claro       | Vermelho    | "Ambiente muito claro" | Ligado |

### Temperatura

- Faixa ideal: **10°C a 15°C**
- Acima de 15°C:
  - Display: “Temp. Alta”
  - LED Amarelo
  - Buzzer Ligado
- Abaixo de 10°C:
  - Display: “Temp. Baixa”
  - LED Amarelo
  - Buzzer Ligado
- Dentro da faixa:
  - Display: “Temperatura OK” + valor

### Umidade

- Faixa ideal: **50% a 70%**
- Acima de 70%:
  - Display: “Umidade Alta”
  - LED Vermelho
  - Buzzer Ligado
- Abaixo de 50%:
  - Display: “Umidade Baixa”
  - LED Vermelho
  - Buzzer Ligado
- Dentro da faixa:
  - Display: “Umidade OK” + valor

### Leitura e Atualização dos Dados

- As leituras são feitas a cada **5 segundos**
- Cada valor exibido é a **média de 5 leituras consecutivas**

## 🔗 Links Importantes

- 🔌 [Simulação no Wokwi](https://wokwi.com/projects/431033573807243265)
- 📽️ [Vídeo explicativo do projeto](https://www.youtube.com/watch?v=Fe03LMVl0Uk)

## 🎓 Integrantes

- Paulo Cesar de Govea Junior - (RM:566034)
- Guilherme Vilela Perez - (RM:564422)
- Gustavo Panham Dourado - (RM:563904)
- Christian Schunck de Almeida - (RM:563850)
- Thomas Jeferson Santana Wang - (RM565104)

## 🧠 Dificuldades e Soluções

- **Integração do sensor DHT11**: Foi necessário utilizar a biblioteca `DHT.h` e ajustar a leitura para obter médias.
- **Display LCD com I2C**: A comunicação I2C facilitou a montagem e economizou pinos no Arduino.

## 📅 Entrega

- **Data do Hands-On**: 16/05/2025

## 📜 Licença

Este projeto é acadêmico e está sujeito às regras da disciplina. Todos os direitos reservados © 2025 Prof. Lucas D. Augusto e equipe docente da FIAP.

