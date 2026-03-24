# Projeto FIWARE + ESP32 (Smart Lamp IoT)

## 📖 Descrição do Projeto

Este projeto tem como objetivo implementar uma **Prova de Conceito (PoC)** utilizando a plataforma FIWARE integrada a um **ESP32 DEVKIT V1**, simulado no Wokwi.

A solução simula um sistema de **monitoramento de luminosidade para vinherias**, utilizando um sensor LDR, além de permitir o controle remoto de um LED (lâmpada) via protocolo MQTT.

---

## 🎯 Objetivos

* Implementar o FIWARE no Google Cloud
* Criar uma entidade lógica representando uma lâmpada inteligente
* Simular um sistema IoT com ESP32
* Enviar dados de luminosidade para o FIWARE
* Receber comandos remotos para controle do LED
* Validar comunicação via MQTT e Postman

---

## 🧠 Arquitetura da Solução

* ESP32 (simulado no Wokwi)
* Sensor LDR (leitura de luminosidade)
* Broker MQTT
* FIWARE (Orion Context Broker)
* Postman (envio de comandos)

Fluxo:

ESP32 → MQTT → FIWARE
FIWARE → MQTT → ESP32

---

## ⚙️ Tecnologias Utilizadas

* FIWARE
* Google Cloud Platform
* ESP32 DEVKIT V1
* Wokwi
* MQTT
* Postman
* Linguagem C++ (Arduino)

---

## 🔌 Funcionamento do Sistema

O ESP32 realiza duas funções principais:

### 📡 Envio de dados

* Lê o valor do sensor LDR (simulado por potenciômetro)
* Converte o valor para porcentagem (0 a 100)
* Publica no tópico MQTT:

```
/TEF/lamp002/attrs/l
```

### 💡 Controle da lâmpada

* Recebe comandos via MQTT:

```
/TEF/lamp002/cmd
```

* Comandos:

  * `lamp002@on|` → Liga LED
  * `lamp002@off|` → Desliga LED

* Envia status para o broker:

```
/TEF/lamp002/attrs
```

---

## 📄 Código do Projeto

O código foi desenvolvido em C++ utilizando Arduino e está disponível no repositório.

## Autores:

* Giovanna Oliveira Ferreira Dias – RM 566647
* Maria Laura Druzeic – RM 566634
* Marianne Mukai Nishikawa – RM 568001
  

## ☁️ Configuração do FIWARE

* Plataforma instalada no Google Cloud
* Broker MQTT configurado
* Comunicação com Orion Context Broker validada
* Health Check executado com sucesso

---

## 🧪 Simulação (Wokwi)

🔗 Link da simulação:
*https://wokwi.com/projects/459135998760928257*

---

## 🎥 Vídeo Demonstrativo

🔗 Link do vídeo (máx. 3 minutos):
*(coloque aqui seu vídeo em time-lapse)*

O vídeo demonstra:

* Envio de dados de luminosidade
* Comunicação com FIWARE
* Controle do LED via Postman

---

## 📬 Testes com Postman

Utilizado para enviar comandos ao dispositivo:

Exemplo de comando:

```
lamp002@on|
lamp002@off|
```

---

## ✅ Resultados Obtidos

* Comunicação IoT funcionando corretamente
* Integração ESP32 + MQTT + FIWARE validada
* Controle remoto do dispositivo operacional
* Envio contínuo de dados de luminosidade

---

