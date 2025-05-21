# 🧱 Sensor de Umidade para Concreto com Arduino

Este projeto apresenta um protótipo funcional de um **sensor de umidade para concreto**, utilizando **Arduino** e um **sensor de umidade do solo**. Ele foi desenvolvido para demonstrar como é possível aplicar tecnologias simples na **manutenção preventiva de estruturas de concreto**, monitorando sua umidade e prevenindo falhas estruturais.

---

## 📦 Materiais Utilizados

- 1x Arduino Uno (ou placa compatível, como BlackBoard da Robocore)
- 1x Sensor de umidade do solo (FC-28)
- 1x Display LCD 16x2 com módulo I2C
- Protoboard
- Cabos jumper (macho-macho)
- Esponja ou pedaço de concreto úmido para simulação
## 🔌 Esquema de Ligações

### 📍 Sensor de Umidade (FC-28)
- **VCC** → 5V no Arduino  
- **GND** → GND no Arduino  
- **A0** → A0 no Arduino  

### 📍 Módulo LCD I2C
- **VCC** → 5V no Arduino *(ou 3.3V dependendo do módulo)*
- **GND** → GND no Arduino  
- **SDA** → A4 no Arduino Uno  
- **SCL** → A5 no Arduino Uno  

> Obs: Ajuste o **potenciômetro** do módulo I2C (o parafuso azul atrás do LCD) para que o texto fique visível na tela.

---

## 🧠 Funcionamento

1. O sensor mede o nível de umidade do concreto (ou esponja).
2. O valor lido é enviado para o **display LCD**, indicando o percentual de umidade.
3. Pode ser usado para simular 3 etapas:
   - Concreto molhado (alta umidade)
   - Em secagem (umidade média)
   - Seco (umidade baixa)

---

## 💻 Código Arduino

O código está comentado e pode ser ajustado conforme o sensor ou display. Veja o arquivo `projeto.sensor.ino` no repositório.

---

## 🖼️ Demonstração

- Apresentação do protótipo em tempo real com uma esponja úmida. Ou com amostras de concreto em estágios diferentes de umidade.
- Indicar as mudanças de leitura no display à medida que a umidade varia.
- Destaque na **aplicação prática na engenharia civil**, como um sistema de alerta para infiltrações ou secagem incorreta.

---

## 📚 Bibliotecas Necessárias

- [LiquidCrystal_I2C](https://github.com/fdebrabander/Arduino-LiquidCrystal-I2C-library) (ou similar)

Instale pela IDE do Arduino:  
**Sketch → Incluir Biblioteca → Gerenciar Bibliotecas → "LiquidCrystal I2C"**

---

## 📌 Observações

- Este projeto utiliza um sensor de solo comum, que **não foi projetado especificamente para concreto**. A demonstração é conceitual.
- Evite deixar o sensor em contato direto com concreto úmido por muito tempo — pode corroer os contatos.
