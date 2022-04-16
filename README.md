# grs.web
![Status](https://img.shields.io/badge/Status-Pre_project-brightgreen)


projeto de controle para meu setup de programação, inclui controle para nanoleafs, ambilight, fitas endereçadas alem, destes itens tambem possuir alguns sensores

## ✔Objetivos✔

Controlar os seguintes dispositivos (todos com a construção do hardware de forma caseira):

| Item A Ser Controlado                                                | Comunicação via:  |
|----------------------------------------------------------------------|-------------------|
| [Ambilight](https://duckduckgo.com/?q=ambiligjt&iax=images&ia=images)| Cabos             |
| [Nanoleafs](https://duckduckgo.com/?q=nanoleafs&iax=images&ia=images)| Cabos             |
| Leds no teto                                                         | RF                |
| Leds entre a mesa e a parede                                         | Cabos             |
| Relogio de 7 segmentos feito com fita endereçada                     | RF                |
| Leds do pc                                                           | Cabos             |

## 🤖Formas De Controle🤖

O setup será controlado via **API** e tambem via hardware oque irá facilitar a integração com outros aplicativos como:

- Web Site de controle
- Alexa
- Controle Via Mensagem (Telegram ou Whatsapp)
- Através de movimento e botões (ativar luzes brancas etc)

E algumas possibilidades de controle futuros seriam
- Via outro hardware (Camera, Alarme etc)
- Ou até mesmo via algum bot Futuro

## 👀Sensores e suas funções🙄

O projeto consistem em varios dispositivos escravos (slave) e 1 mestre sendo o esp32 conectado a api.

Entre os slaves estão estes sensores que de tempo em tempo serão requisitado o envio de dados(terá varios transceptores)

| Sensor                 | Tipo         | Utilidade                                                                                                                    | Aonde | Tipo de comunicação      |
|------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------|-------|--------------------------|
| Movimento              | pir HC-SR505 | Ativar as luzes de forma Mãos-livres                                                                                         | teto  | RF                       |
| Sensor de som          | KY-038       | Modos ativados por som ou modos ritmicos                                                                                     | mesa  | fio (velocidade de comunicação) |
| Humidade               | dht11        | Exibir para o user                                                                                                           | mesa  | fio                      |
| Temperatura            | dht11        | Exibir para o user e aplicar temperaturas de cores(quando tiver quente puxar para cores frias etc)                           | mesa  | fio                      |
| Sensor de luminosidade | TEMT6000     | Juntamente com o sensor pir, ira ver se esta escuro e tiver movimento dentro de determinada hora entao irá acender as luzes  | teto  | RF                       |
| Dados sobre o pc       | usb          | Monitor de desempenho pc, e alertas por cores                                                                                | mesa  | usb                      |
| Dados sobre o monitor  | usb          | Ambilight                                                                                                                    | mesa  | usb                      |

## 💻Hardware utilizado🔌


Para realizar a montagem deste projeto foi utilizado os seguites itens:

Atuadores/ sinalizadores:
- Tela lcd 16x2 i2c
- Varios metros de fita led: 5V LED WS2812
- Nrf24l01 Transceptor Wireless 2.4GHz

Microcontroladores: 
- cotrolador principal: 1 ESP 32
- controlador secundario p/ Ambilight: Arduino uno ou nano

Sensores:
- Sensor de Movimento pir HC-SR505
- Sensor de som KY-038 
- Sensor de Humidade e Temperatura dht11
- Sensor de luminosidade TEMT6000

Outros
- Encoder e Botão para a interface
- Case de um antigo leitor de cd/dvd de desktop
- fios


## ✔️Status do projeto✔️

Projeto está: Em desenvolvimento

## 📱Contato📱


Autor do projeto e da documentação: 
* Github -> [@Gustavors1608](https://github.com/gustavors1608)
* Instagram -> [@Gustavo_stroschon](https://instagram.com/gustavo_stroschon)
