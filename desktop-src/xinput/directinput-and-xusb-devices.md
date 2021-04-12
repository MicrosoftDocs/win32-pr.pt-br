---
title: Dispositivos DirectInput e XUSB
description: O driver para a classe de controlador comum do Xbox (XUSB) no Windows implementa a interface de modo kernel para a DLL XINPUT.
ms.assetid: 8bf47b07-a1b6-7721-2136-3853e72c71ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2b6d2857502c0e0209d94fb6d933618c180fd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294458"
---
# <a name="directinput-and-xusb-devices"></a>Dispositivos DirectInput e XUSB

O driver para a classe de controlador comum do Xbox (XUSB) no Windows implementa a interface de modo kernel para a DLL XINPUT. Para fornecer uma boa experiência para títulos herdados que usam a API do [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) com o dispositivo de controlador comum, o driver também exporta uma interface de classe de dispositivos de interface humana (HID), que é selecionada pelo DirectInput. Escolhemos o mapeamento de XUSB para HID com base no comportamento típico em um conjunto de aplicativos de jogos para a versão original do XINPUT e atualizamos o mapeamento para subtipos mais recentes. Este tópico descreve o mapeamento do.

## <a name="human-interface-device-hid"></a>HID (Dispositivo de Interface Humana)

O padrão HID é um padrão do Comitê de barramento serial universal (USB) originalmente proposto pela Microsoft para generalizar protocolos para dispositivos de entrada. Ele consiste em uma linguagem de descrição de código de byte e pode expressar gamepads, mouses, joysticks, controles de limitação e de leme e controladores de vários eixos. Como esse padrão é tão generalizado, você pode ter dificuldade em escrever software que consuma a entrada de dispositivos arbitrários. Portanto, para a API do [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) centrada em jogos, desenvolvemos um submapeamento específico de tipos para encorajar os fabricantes de hardware a dar suporte por meio de seus drivers.

- [Definição de classe de dispositivo USB para HID v 1.11](https://www.usb.org/document-library/device-class-definition-hid-111)

> [!Important]
> Você também pode acessar dispositivos de entrada HID por meio da [API do RawInput](../inputdev/about-raw-input.md) e processar relatórios de entrada por meio da [API HID](/windows-hardware/drivers/hid/introduction-to-hid-concepts) de nível baixo, mas comentários de vibração não funcionarão como com o [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="mappings"></a>Mapeamentos

O driver XUSB implementa uma interface de classe XUSB e uma interface de classe HID para dispositivos a fim de dar suporte ao uso de XINPUT e do [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) . Esse mapeamento é baseado nas informações de subtipo XUSB. O Driver implementa quatro grupos distintos de mapeamentos.

| Subtipo XUSB                                      | Mapeamento                     |
|---------------------------------------------------|-----------------------------|
| XINPUT \_ DEVSUBTYPE \_ gamepad (subtipo 1)           | Gamepad                     |
| \_Roda DEVSUBTYPE XInput \_ (subtipo 2)             | Wheel                       |
| XINPUT \_ DEVSUBTYPE \_ \_ (subtipo 3)     | Painel de vôo/teclado de disponibilidade     |
| XINPUT \_ DEVSUBTYPE \_ Flight \_ stick (subtipo 4)     | Pente de voo                |
| XINPUT \_ DEVSUBTYPE \_ Dance \_ Pad (subtipo 5)        | Padrão para qualquer subtipo novo |
| XINPUT \_ DEVSUBTYPE \_ guitarra (subtipo 6)            | Guitarra                      |
| XINPUT \_ DEVSUBTYPE \_ \_ de guitarra alternativa (subtipo 7) |                             |
| \_ \_ Kit de tambor XInput DEVSUBTYPE \_ (subtipo 8)         |                             |
| XINPUT \_ DEVSUBTYPE \_ guitarra \_ baixo (subtipo 11)     |                             |
| XINPUT \_ DEVSUBTYPEe \_ \_ Pad (subtipo 19)      |                             |

> [!Note]  
> Os seguintes mapeamentos de HID são estáticos. Isso significa que, mesmo que o relatório de recursos do dispositivo indique que um determinado botão ou eixo não tem suporte, o mapeamento ainda o incluirá, mas sempre relatará um valor fora do Estado ou central.

## <a name="gamepad"></a>Gamepad

Esse é o mapeamento padrão e é projetado em relação ao gamepad padrão do controlador comum do Xbox e é exposto como um tipo de uso de HID do *gamepad* .

| Control                      | Nome de uso de HID | Página de uso | ID de uso   |
|------------------------------|----------------|------------|------------|
| Direcional analógico                   | X, Y           | 0x01       | 0x30, 0x31 |
| Aderência à direita                  | RX, entar         | 0x01       | 0x33, 0x34 |
| Gatilho esquerdo + gatilho direito | Z\*            | 0x01       | 0x32       |
| D-preenchimento, inferior, esquerda, direita  | Opção Hat     | 0x01       | 0x39       |
| Um                            | Botão 1       | 0x09       | 0x01       |
| B                            | Botão 2       | 0x09       | 0x02       |
| X                            | Botão 3       | 0x09       | 0x03       |
| S                            | Botão 4       | 0x09       | 0x04       |
| LB (amortecedor à esquerda)             | Botão 5       | 0x09       | 0x05       |
| RB (supertapar à direita)            | Botão 6       | 0x09       | 0x06       |
| BACK                         | Botão 7       | 0x09       | 0x07       |
| START                        | Botão 8       | 0x09       | 0x08       |
| LSB (botão de aderência à esquerda)      | Botão 9       | 0x09       | 0x09       |
| RSB (botão de aderência à direita)     | Botão 10      | 0x09       | 0x0A       |

> [!Note]  
> ( \* ): Isso é combinado para que Z exiba o comportamento de centralização esperado pela maioria dos títulos para rotação; isso significa que não é possível ver todos os valores possíveis de combinação de gatilho por meio do [DIRECTINPUT](/previous-versions/windows/desktop/ee416842(v=vs.85)) e HID.

## <a name="arcade-stickarcade-pad"></a>Painel de vôo/teclado de disponibilidade

Esse é o mapeamento criado em todo o controlador de estado de vôo e é exposto como um tipo de uso de do *gamepad* . O painel de alta disponibilidade é muito parecido com um pente de vôo, mas em um fator forma menor. Esses designs substituem o gatilho à esquerda analógico e o gatilho direito por botões digitais que relatam o valor mínimo e máximo do eixo.

| Control                     | Nome de uso de HID | Página de uso | ID de uso |
|-----------------------------|----------------|------------|----------|
| D-preenchimento, inferior, esquerda, direita | Opção Hat     | 0x01       | 0x39     |
| Um                           | Botão 1       | 0x09       | 0x01     |
| B                           | Botão 2       | 0x09       | 0x02     |
| X                           | Botão 3       | 0x09       | 0x03     |
| S                           | Botão 4       | 0x09       | 0x04     |
| LB (amortecedor à esquerda)            | Botão 5       | 0x09       | 0x05     |
| RB (supertapar à direita)           | Botão 6       | 0x09       | 0x06     |
| BACK                        | Botão 7       | 0x09       | 0x07     |
| START                       | Botão 8       | 0x09       | 0x08     |
| Gatilho esquerdo                | Botão 9       | 0x09       | 0x09     |
| Gatilho à direita               | Botão 10      | 0x09       | 0x0A     |

Esses dispositivos podem ou não dar suporte a controles adicionais, mas eles não são expostos pelo mapeamento de HID: à esquerda, à direita, LSB (botão à esquerda) e RSB (botão de aderência à direita).

## <a name="wheel"></a>Wheel

Esse mapeamento é projetado em relação à roda de corrida do Xbox e é exposto como um tipo de uso de do *gamepad* .

| Control                                                        | Nome de uso de HID | Página de uso | ID de uso |
|----------------------------------------------------------------|----------------|------------|----------|
| Roda (esquerda do taco X)                                           | X              | 0x01       | 0x30     |
| Pedal do acelerador (gatilho direito) + pedal do freio (gatilho esquerdo) | Z\*            | 0x01       | 0x32     |
| D-preenchimento, inferior, esquerda, direita                                    | Opção Hat     | 0x01       | 0x39     |
| Um                                                              | Botão 1       | 0x09       | 0x01     |
| B                                                              | Botão 2       | 0x09       | 0x02     |
| X                                                              | Botão 3       | 0x09       | 0x03     |
| S                                                              | Botão 4       | 0x09       | 0x04     |
| LB (amortecedor à esquerda)                                               | Botão 5       | 0x09       | 0x05     |
| RB (supertapar à direita)                                              | Botão 6       | 0x09       | 0x06     |
| LSB (botão de aderência à esquerda)                                        | Botão 7       | 0x09       | 0x07     |
| RSB (botão de aderência à direita)                                       | Botão 8       | 0x09       | 0x08     |
| BACK                                                           | Botão 9       | 0x09       | 0x09     |
| START                                                          | Botão 10      | 0x09       | 0x0A     |

> [!Note]  
> ( \* ): Isso é combinado para que Z exiba o comportamento de centralização esperado pela maioria dos títulos para os controles de freio e acelerador; isso significa que não é possível ver todos os valores de combinação de pedal possíveis por meio do [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="flight-stick"></a>Pente de voo

Esse mapeamento é projetado em relação ao pente de vôo do Xbox e é exposto como um tipo de uso do *Joystick* HID.

| Control                     | Nome do uso | Página de uso | ID de uso   |
|-----------------------------|------------|------------|------------|
| Pente de voo (adesivo à esquerda)   | X, Y       | 0x01       | 0x30, 0x31 |
| ÂNGULO de visão da direita (direcional)       | RX, entar     | 0x01       | 0x33, 0x34 |
| Limitação (gatilho direito)    | Z          | 0x01       | 0x32       |
| Leme (gatilho esquerdo)       | Rz         | 0x01       | 0x35       |
| D-preenchimento, inferior, esquerda, direita | Opção Hat | 0x01       | 0x39       |
| Arma primária (A)          | Botão 1   | 0x09       | 0x01       |
| Arma secundária (B)        | Botão 2   | 0x09       | 0x02       |
| X                           | Botão 3   | 0x09       | 0x03       |
| S                           | Botão 4   | 0x09       | 0x04       |
| LB (amortecedor à esquerda)            | Botão 5   | 0x09       | 0x05       |
| RB (supertapar à direita)           | Botão 6   | 0x09       | 0x06       |
| BACK                        | Botão 7   | 0x09       | 0x07       |
| START                       | Botão 8   | 0x09       | 0x08       |
| LSB (botão de aderência à esquerda)     | Botão 9   | 0x09       | 0x09       |
| RSB (botão de aderência à direita)    | Botão 10  | 0x09       | 0x0A       |

> [!Note]  
> Isso se baseia no design do pente de voo final. Como isso difere das definições iniciais do Flight Stick, muitos dispositivos têm uma opção de modo que dá suporte ao modelo antigo versus novo. Esse mapeamento assume o novo modelo.