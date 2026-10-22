<div align="center">

# Sonda Diferencial de Baja Tensión de hasta 250Vp (seno: 176,78Vrms) @ 100kHz

*Un proyecto para mediciones seguras y precisas con osciloscopio. Basado en componentes disponibles en cualquier laboratorio o tienda de electrónica.*

[![Licencia: CC BY-NC-SA 3.0](https://img.shields.io/badge/Licencia-CC%20BY--NC--SA%203.0-orange.svg)](LICENSE.md)
[![Hardware: KiCad](https://img.shields.io/badge/Hardware-KiCad-blue.svg)](https://kicad.org/)
[![3D Print: STL](https://img.shields.io/badge/3D%20Print-STL-green.svg)](#)

</div>

---

## 1. Descripción del Proyecto

Esta **Sonda Diferencial** ha sido diseñada para permitir mediciones de señales flotantes usando un solo canal de un osciloscopio convencional sin riesgo de cortocircuitos a tierra o daños en el equipo de medición.

El circuito atenúa y convierte señales diferenciales en una señal referenciada a masa (*single-ended*) apta para las entradas estándar BNC (Vo: 3Vpp).

### Esquemático del Circuito

<div align="center">
  <img src="img/esquema.png" alt="Esquemático de la Sonda Diferencial" width="800">
  <p><em>Figura 1: Esquemático general del circuito de la sonda diferencial.</em></p>
</div>

---

## 2. Licencia y Restricciones

Este proyecto está bajo la licencia **Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported (CC BY-NC-SA 3.0)**.

* **Atribución (BY):** Debe dar crédito de manera adecuada, brindar un enlace a la licencia e indicar si se han realizado cambios.
* **No Comercial (NC):** <u>No puede utilizar este material para una finalidad comercial</u> ni para obtener una ventaja monetaria directa/indirecta sin la autorización previa del autor.
* **Compartir Igual (SA):** Si remezcla, transforma o crea a partir del material, debe distribuir sus contribuciones bajo la misma licencia que el original.

---

## 3. Lista de Materiales (BOM)

A continuación se detalla la lista completa de componentes extraída directamente de KiCad:

| Designador | Valor / Descripción | Cantidad | Encapsulado / Footprint |
| :--- | :--- | :---: | :--- |
| **U1, U2** | TL082 (Op-Amp JFET Dual) | 2 | Package_DIP:DIP-8_W7.62mm_Socket |
| **U3** | LM358 (Op-Amp Dual) | 1 | Package_DIP:DIP-8_W7.62mm_Socket |
| **Q1** | MMBT2222A (Transistor NPN) | 1 | Package_TO_SOT_SMD:SOT-23 |
| **D1** | Z8V2 (Diodo Zener 8.2V) | 1 | Diode_THT:D_DO-41_SOD81_P12.70mm |
| **D2** | SM4007 (Diodo Rectificador) | 1 | Diode_SMD:D_MELF |
| **D3, D4, D9** | 1N4733A (Diodo Zener 5.1V) | 3 | Diode_THT:D_DO-41_SOD81_P10.16mm |
| **D5, D6, D7, D8** | LL4148 (Diodo de Señal) | 4 | Diode_SMD:D_MiniMELF |
| **D10** | LED 3mm (Power ON) | 1 | LED_THT:LED_D3.0mm |
| **D11** | LED 3mm (Low Battery) | 1 | LED_THT:LED_D3.0mm |
| **C1, C9, C13, C16, C19** | 10uF (Electrolítico) | 5 | Capacitor_THT:CP_Radial_D5.0mm_P2.00mm |
| **C10** | 100uF (Electrolítico) | 1 | Capacitor_THT:CP_Radial_D8.0mm_P3.50mm |
| **C11, C14, C17** | 1uF (Electrolítico) | 3 | Capacitor_THT:CP_Radial_D4.0mm_P2.00mm |
| **C3, C5, C8, C12, C15, C18** | 100nF | 6 | Capacitor_SMD:C_1206_3216Metric |
| **C2, C7** | 1nF | 2 | Capacitor_SMD:C_1206_3216Metric |
| **C4, C6** | Compensación | 2 | Capacitor_SMD:C_1206_3216Metric |
| **R3, R6** | 1M (Resistencia Alto Voltaje) | 2 | Resistor_THT:R_Axial_DIN0411 |
| **R4, R5, R8, R9, R11, R13** | 10k | 6 | Resistor_SMD:R_1206_3216Metric |
| **R15, R16** | 4k7 | 2 | Resistor_SMD:R_1206_3216Metric |
| **R7, R10** | 220 | 2 | Resistor_SMD:R_1206_3216Metric |
| **R21, R22** | 0 (Jumper) | 2 | Resistor_SMD:R_1206_3216Metric |
| **R1** | 470 | 1 | Resistor_SMD:R_1206_3216Metric |
| **R2** | 100k | 1 | Resistor_SMD:R_1206_3216Metric |
| **R12** | 100 | 1 | Resistor_SMD:R_1206_3216Metric |
| **R14** | 2k2 | 1 | Resistor_SMD:R_1206_3216Metric |
| **R17** | 22k | 1 | Resistor_SMD:R_1206_3216Metric |
| **R18** | 33k | 1 | Resistor_SMD:R_1206_3216Metric |
| **R19** | 1.2k | 1 | Resistor_SMD:R_1206_3216Metric |
| **R20** | 910 | 1 | Resistor_SMD:R_1206_3216Metric |
| **RV1, RV2** | 1k (Trimmer) | 2 | Potentiometer_THT:Potentiometer_Piher_PT-6-V |
| **J1** | Conector BNC Salida | 1 | Connector_Coaxial:BNC_Amphenol_B6252HB |
| **J2** | Clema 2P Alimentación 9V | 1 | TerminalBlock_MX126-5.0-02P |
| **J3, J4** | Pin Header +Vi / -Vi | 2 | Connector_PinHeader_2.54mm_1x01 |

<div align="center">
  <img src="img/sonda.png" alt="Sonda Diferencial" width="700px">
</div>

---

## 4. Cálculos del Sistema

* **Cálculos de alimentación del TL082:** 
  El voltaje efectivo que maneja el OP-AMP debe estar dentro de los márgenes de alimentación. Configurado diferencialmente con 8Vpp, entrega un `Vo_max = 5Vpp` (referenciado a tierra virtual de `+/- 2.5Vp`).
* **Voltaje pico de salida:** Debe ser `<= 5V` para adaptarse al rango de entrada de los osciloscopios convencionales.
* **Consumo total estimado:** 
  * Regulador: 2mA
  * Amplificador diferencial: 7mA
  * Buffer: 4mA
  * GND Virtual: 4mA
  * Detector de voltaje: 5mA
  * LED Rojo (Low Batt): 2.5mA
  * LED Verde (Power ON): 2.5mA
  * **Total:** `27mA` / **Potencia:** `221mW` (< 230mW requeridos).

---

## 5. Aplicaciones

* Medición en fuentes de alimentación conmutadas (SMPS) y etapas de potencia.
* Análisis de variadores de frecuencia (VFD) y drivers de motores.
* Diseño y prueba de circuitos Inverter y convertidores DC-DC.
* Medición segura en líneas de corriente alterna (AC) sin aislar el osciloscopio de tierra.

---

## 6. Demostración de Uso

1. Conecte la salida BNC de la sonda diferencial al Canal 1 de su osciloscopio mediante un cable coaxial de 50&Omega;.
2. Alimente la sonda (batería interna de 9V). El umbral de indicador de batería baja (*low-batt*) está calculado en 8.3Vdc.
3. Seleccione el factor de atenuación correcto en el osciloscopio (ej. 100x).
4. Conecte las puntas de prueba a los puntos flotantes de su circuito.

<div align="center">
  <img src="img/demo.jpg" alt="Demostración de Uso" width="600">
  <p><em>Figura 2: Prueba de la sonda midiendo una señal en etapa de potencia.</em></p>
</div>
