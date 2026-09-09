# 🕹️ Protótipo de Controlador Arcade de Baixo Custo (ESP32-C3 Mini)

> **Projeto Acadêmico - TCC**  
> Desenvolvimento de um controlador modular de baixo custo para jogos arcade amadores, mitigando limitações de pinos (GPIO) e ruídos elétricos. Este repositório tem como principal finalidade armazenar os códigos utilizados.

---

## 📌 Índice
- [Sobre o Projeto](#-sobre-o-projeto)
- [Arquitetura de Hardware](#-arquitetura-de-hardware)
- [Tecnologias e Ferramentas](#-tecnologias-e-ferramentas)
- [Autor](#-autor)

---

## 💻 Sobre o Projeto

Este projeto apresenta um protótipo funcional de controlador embarcado voltado para fliperamas e simuladores retrô. O núcleo do sistema é o microcontrolador **ESP32-C3 Mini**. A pesquisa e o desenvolvimento focaram em resolver problemas comuns enfrentados por hobbistas: a escassez de portas lógicas nativas da placa compacta, o efeito *bounce* de botões mecânicos e a queima de componentes por surtos elétricos induzidos por atuadores (como eletroímãs). O desenvolvimento do projeto consta no documento TCC referente a este projeto.

---

## 🛠️ Arquitetura de Hardware

Abaixo estão listados os componentes principais dimensionados para o módulo:

* **Microcontrolador:** ESP32-C3 Mini (32-bits RISC-V, 160 MHz)
* **Expansão de Portas:** CI PCF8574 (I2C)
* **Isolamento de Sinal:** Optoisoladores 4N25
* **Atuadores suportados:** Módulos Relé de 4 canais e Eletroímãs (12V / 0.5A)
* **Entradas:** Até 12 Botões mecânicos e portas logicas para até 2 Joysticks direcionais

---

## 🚀 Tecnologias e Ferramentas

- **IDE:** Arduino IDE (ambiente principal de compilação e gravação)
- **Linguagem:** C / C++
- **Protocolos de Comunicação:** I2C (Inter-Integrated Circuit) e USB-HID / Serial

---

## ✉️ Autor

* **Andre Henrique do Monte Rodrigues Junior**
* 📧 E-mail: ahdmrj.emt@gmail.com
* 📍 Faculdade Matias Machline (FMM) – Manaus-AM, Brasil
