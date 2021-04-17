---
title: Mensagens de notificação de joystick
description: Mensagens de notificação de joystick
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- joysticks, notificações
- joysticks, mensagens
- joysticks, posição
- joysticks, botões
- MM_JOY1 mensagens
- MM_JOY2 mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770163"
---
# <a name="joystick-notification-messages"></a>Mensagens de notificação de joystick

As mensagens do joystick notificam seu aplicativo de que um joystick alterou a posição ou que um de seus botões alterou os Estados. As mensagens que começam com MM \_ JOY1 serão enviadas para a função se seu aplicativo solicitar entrada do joystick usando o identificador JOYSTICKID1 e \_ as mensagens mm JOY2 forem enviadas se seu aplicativo solicitar entrada do joystick usando o identificador JOYSTICKID2.

As mensagens na tabela a seguir identificam o status dos botões do joystick:



| Mensagem                                         | Descrição                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**\_JOY1BUTTONDOWN mm**](mm-joy1buttondown.md) | Um botão no joystick JOYSTICKID1 foi pressionado.              |
| [**\_JOY1BUTTONUP mm**](mm-joy1buttonup.md)     | Foi lançado um botão no joystick JOYSTICKID1.             |
| [**\_JOY1MOVE mm**](mm-joy1move.md)             | O joystick JOYSTICKID1 alterou a posição na direção x ou y. |
| [**\_JOY1ZMOVE mm**](mm-joy1zmove.md)           | O joystick JOYSTICKID1 alterou a posição na direção z.       |
| [**\_JOY2BUTTONDOWN mm**](mm-joy2buttondown.md) | Um botão no joystick JOYSTICKID2 foi pressionado.              |
| [**\_JOY2BUTTONUP mm**](mm-joy2buttonup.md)     | Foi lançado um botão no joystick JOYSTICKID2.             |
| [**\_JOY2MOVE mm**](mm-joy2move.md)             | O joystick JOYSTICKID2 alterou a posição na direção x ou y  |
| [**\_JOY2ZMOVE mm**](mm-joy2zmove.md)           | O joystick JOYSTICKID2 alterou a posição na direção z.       |



 

Todas as mensagens relatam botões inexistentes como liberadas.

 

 




