🌐 Projeto IoT com FIWARE – Monitoramento de Luminosidade (Smart Lamp)

📌 Descrição
Este projeto tem como objetivo demonstrar a integração entre dispositivos IoT e a plataforma FIWARE, utilizando um ESP32 equipado com um sensor LDR para monitoramento de luminosidade e controle de uma lâmpada (LED onboard).

A solução permite:

📡 Enviar dados de luminosidade (edge → cloud)
🎛️ Controlar o estado da lâmpada via FIWARE (cloud → edge)
🔄 Comunicação via protocolo MQTT
🌍 Gerenciamento de contexto com Orion Context Broker
🧠 Arquitetura da Solução

A arquitetura está dividida em três camadas:

🔝 Application
Postman (envio de comandos e consultas)
Integração via API REST (NGSI v2)
⚙️ Back-end (FIWARE)
Orion Context Broker
IoT Agent MQTT
Mosquitto MQTT Broker
MongoDB
📡 IoT / Edge
ESP32 (Wokwi / físico)
Sensor LDR (entrada analógica)
LED onboard (atuador)
🔄 Fluxo de Dados
📤 Edge → Cloud
ESP32 lê o valor do LDR
Publica no MQTT Broker
IoT Agent recebe e traduz
Orion atualiza a entidade
📥 Cloud → Edge
Postman envia comando (ON/OFF)
Orion recebe
IoT Agent traduz para MQTT
ESP32 recebe e controla o LED
🧰 Tecnologias Utilizadas
ESP32
Arduino (C++)
Wokwi Simulator
FIWARE
Orion Context Broker
IoT Agent MQTT
Mosquitto MQTT Broker
MongoDB
Docker / Docker Compose
Postman
