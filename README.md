# 🕹️ Protótipo de Controlador Arcade de Baixo Custo (ESP32-C3 Mini)

> **Projeto Acadêmico - TCC**  
> Desenvolvimento de um controlador modular de baixo custo para jogos arcade amadores, mitigando limitações de pinos (GPIO) e ruídos elétricos.

---

## 📌 Índice
- [Sobre o Projeto](#-sobre-o-projeto)
- [Principais Desafios Superados](#-principais-desafios-superados)
- [Arquitetura de Hardware](#-arquitetura-de-hardware)
- [Tecnologias e Ferramentas](#-tecnologias-e-ferramentas)
- [Como Reproduzir o Projeto](#-como-reproduzir-o-projeto)
- [Autor](#-autor)

---

## 💻 Sobre o Projeto

Este projeto apresenta um protótipo funcional de controlador embarcado voltado para fliperamas e simuladores retrô. O núcleo do sistema é o microcontrolador **ESP32-C3 Mini**. A pesquisa e o desenvolvimento focaram em resolver problemas comuns enfrentados por hobbistas: a escassez de portas lógicas nativas da placa compacta, o efeito *bounce* de botões mecânicos e a queima de componentes por surtos elétricos induzidos por atuadores (como eletroímãs).

---

## ⚙️ Principais Desafios Superados

- **Expansão de I/O:** Ampliação das conexões utilizando o expansor **PCF8574** via protocolo **I2C**, contornando a limitação de apenas 11 pinos GPIO nativos.
- **Proteção Elétrica:** Isolamento completo contra picos de tensão usando optoacopladores **4N25** para acionamento de módulos relé de 12V.
- **Debouncing Híbrido:** Mitigação do efeito *bounce* dos microswitches através de filtros físicos (capacitores de 100nF) e tratamento lógico via software (50ms).
- **Gestão de Boot:** Isolamento elétrico dos *strapping pins* para impedir travamentos na inicialização do firmware.

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

## 💾 Como Reproduzir o Projeto

### Pré-requisitos
* Ter o [Arduino IDE](https://arduino.cc) instalado.
* Placa configurada no gerenciador de placas da Espressif (`esp32` da Espressif Systems).
* Biblioteca para o expansor PCF8574 instalada no seu ambiente.

### Passos para Instalação

1. Copie o código e cole no Arduino IDE.
3. Conecte o ESP32-C3 Mini ao seu computador via cabo USB adequado.
4. Selecione a placa `ESP32C3 Dev Module` e a porta COM correta.
5. Clique em **Carregar (Upload)**.

---

## 📄 Licença e Uso Acadêmico

Este projeto foi desenvolvido no âmbito de pesquisa da **Faculdade Matias Machline (FMM)**. Sinta-se à vontade para clonar, estudar e implementar melhorias para fins educacionais e de hobby.

---

## ✉️ Autor

* **Andre Henrique do Monte Rodrigues Junior**
* 📧 E-mail: ahdmrj.emt@gmail.com
* 📍 Faculdade Matias Machline (FMM) – Manaus-AM, Brasil
