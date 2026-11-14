# ESP32_DEVKIT_V1_PROTOBOARD_90 — R01 (2026-11-14)

Primeira revisão, derivada do PICO_RP2040_PROTOBOARD_90 (R03).

## O que tem
- Esquemático: capa + ESP32 + BARRA_90 (30 redes), ERC simulado 0, textos sem sobreposição.
- PCB 93,22 × 51,97 mm, 2 camadas, sem via, DevKit deslocada 5,08 mm para a antena não ficar sobre o J1.
- Keepout ANTENA_KEEPOUT (F.Cu + B.Cu: sem trilha, via e zona) sob a antena.
- Net class POWER (0,6 mm) por netclass_patterns: 3V3, VIN, GND.
- Frente: nomes dos pinos, GND em caixa, grupos com acento correto; logos ZAT ELECTRONIC, KiCad e OSHW (iguais aos do PICO_RP2040_PROTOBOARD_90, "Not in schematic").
- Verso: mapa dos 25 GPIO, tabela de alimentação/EN e quadro ATENÇÃO 3,3 V.

## Verificações feitas aqui
| Item | Resultado |
|---|---|
| Esquemático × PCB | 0 diferenças (29 redes) |
| Serigrafia frente/verso (sobreposição, pads +0,15, borda) | 0 |
| Cobre–borda | 1,92 mm |
| Furo NPTH–borda / furo–trilha | 1,21 / 1,02 mm |
| Trilhas no keepout da antena | 0 |
| Folga mínima entre redes | 0,30 mm |

## Antes de fabricar (no KiCad 10)
1. Biblioteca global ZAT_Connector: símbolo `Conn_01x30` e footprint `PinHeader_1x30_P2.54mm_Horizontal_EdgeMount` já gravados (backup `ZAT_Connector.kicad_sym.bak_20261114`).
2. Abrir o PCB → **B** (refill zones) → **Inspect → Design Rules Checker** e **ERC** no esquemático: devem dar 0.
3. Conferir a DevKit física: há clones com fileiras a 25,4 mm (este) e a 22,86 mm — medir antes de soldar.
