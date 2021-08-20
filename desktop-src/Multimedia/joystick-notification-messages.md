---
title: Mensagens de notificação do Conector
description: Mensagens de notificação do Conector
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- porões, notificações
- joysticks, mensagens
- colocação,posição
- buttons,buttons
- MM_JOY1 mensagens
- MM_JOY2 mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27113adeb6f9fd4444f8fc30431df0eab686db667fa2674e81d7f5d4e568be64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140335"
---
# <a name="joystick-notification-messages"></a>Mensagens de notificação do Conector

As mensagens do Button notificam seu aplicativo de que um mouse alterou a posição ou que um de seus botões alterou os estados. As mensagens que começam com MM MM MM1 serão enviadas para a função se o aplicativo solicitar a entrada do conector usando o identificador INPUTID1 e as mensagens MM MM2 serão enviadas se o aplicativo solicitar a entrada do conector usando o \_ \_ identificador USBID2.

As mensagens na tabela a seguir identificam o status dos botões de mouse:



| Mensagem                                         | Descrição                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**MM \_ MM MM1BUTTONDOWN**](mm-joy1buttondown.md) | Foi pressionado um botão em button em button em BUTTONID1.              |
| [**MM \_ MM MM1BUTTONUP**](mm-joy1buttonup.md)     | Foi lançado um botão no button no button em BUTTONID1.             |
| [**MM \_ MM MM1MOVE**](mm-joy1move.md)             | O Joystick LTDID1 alterou a posição na direção x ou y. |
| [**MM \_ MM MM1ZMOVE**](mm-joy1zmove.md)           | O Botão DEID1 alterou a posição na direção z.       |
| [**MM \_ MMBUTTONDOWN**](mm-joy2buttondown.md) | Foi pressionado um botão no button no mouse EMID2.              |
| [**MM \_ MM2BUTTONUP**](mm-joy2buttonup.md)     | Foi lançado um botão no button on button ONID2.             |
| [**MM \_ MM2MOVE**](mm-joy2move.md)             | A posição de 100000012 foi alterada por Meio de Uma Direção X ou Y  |
| [**MM \_ MM2ZMOVE**](mm-joy2zmove.md)           | O Botão DEID2 alterou a posição na direção z.       |



 

Todas as mensagens relatam botões inexistentes conforme liberado.

 

 




