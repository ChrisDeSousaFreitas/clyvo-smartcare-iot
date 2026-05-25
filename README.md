# 🐾 Clyvo SmartCare - IoT Telemetry Prototype

**FIAP - Challenge Disruptive Architectures: IOT, IOB & Generative IA**

## 👥 Equipe (ADS/2TDSPO)
* Bruno Andrade Zanatelli - RM 563736
* Christian de Sousa Freitas - RM 566098
* Matheus Enrico de Souza - RM 562532
* Pedro Pereira Biasolli da Fonseca - RM 562521
* Rodrigo Tiezzi - RM 562975

## 📹 Apresentação e Pitch
Confira o vídeo de demonstração do funcionamento da arquitetura e simulação do hardware na nuvem:
▶️ **[https://youtu.be/RGIobytVwZM]**

## 📌 O Problema
A monitorização da saúde de animais de estimação baseia-se na observação humana, o que leva frequentemente a diagnósticos tardios de stress, dores ou problemas cardíacos. O projeto visa resolver a lacuna de comunicação entre o bem-estar do pet e a percepção do tutor.

## 🚀 A Solução (IoT)
Foi desenvolvido o protótipo de uma **Coleira Inteligente (Smart Collar)** utilizando um microcontrolador ESP32. O dispositivo recolhe dados vitais (simulados via conversor A/D) e processa uma classificação básica do estado do animal ("Descansando", "Atividade Normal", "Stress"). Os dados são transmitidos via Wi-Fi utilizando o protocolo leve de mensageria **MQTT**.

## 🛠️ Tecnologias Utilizadas
* **ESP32:** Microcontrolador principal com módulo Wi-Fi integrado.
* **C++ (Arduino Core):** Linguagem utilizada para a programação de firmware.
* **PubSubClient:** Biblioteca para gestão das publicações e subscrições MQTT.
* **HiveMQ Public Broker:** Servidor na nuvem que faz o roteamento das mensagens.
* **Wokwi Simulator:** Ambiente de testes de hardware.

## ⚙️ Instruções de Uso
1. Acesse a simulação do hardware no Wokwi: **[Insira o link do seu projeto Wokwi aqui]**
2. Inicie a simulação (botão Play). Aguarde a mensagem "Conectado ao Broker!" no console.
3. Em outra aba, abra o [HiveMQ Websocket Client](https://www.hivemq.com/demos/websocket-client/).
4. Conecte-se e subscreva o tópico `clyvocare/pet1/#`.
5. Altere o valor do potenciômetro no Wokwi e observe os dados (BPM e Status) atualizando no Dashboard em tempo real.

## 📊 Resultados Parciais e Prova de Conceito
A prova de conceito (PoC) demonstrou viabilidade técnica e estrutural. A arquitetura *Publish/Subscribe* do MQTT garantiu o envio de dados com baixíssima latência. O script realiza a classificação *edge* (no próprio dispositivo), mitigando a sobrecarga na nuvem e evidenciando uma aplicação robusta e escalável de IoT voltada para a saúde animal.