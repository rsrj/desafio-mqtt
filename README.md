# Desafio MQTT

Resolução do desafio proposto como etapa de processo seletivo para vaga de Desenvolvedor de Sistemas Embarcados.

O projeto foi desenvolvido utilizando o framework ESP-IDF, junto com a extensão do PlatformIO para VSCode.
Como broker público foi utilizado o eclipse, disponível em: "mqtt://mqtt.eclipseprojects.io". Para monitorar as mensagens dos tópicos utilizou-se o aplicativo para smartphone Android MyMQTT, inscrito nos tópicos "/led" e "/erro".

Quando a mensagem JSON {“action”: 1} é enviada ao tópico "/led", o LED conectado a GPIO 2 é acendido, e quando a mensagem {“action”: 0} é enviada, o LED é desligado. Caso a chave "action" não seja encontrada, ou seja encontrada com valor inválido, uma mensagem de JSON com o endereço MAC do dispositivo é enviada para o tópico "/erro".

O programa foi testado utilizando uma placa ESP32 NodeMCU de 38 pinos.
