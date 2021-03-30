---
title: Notificações de Event-Based
description: Notificações de Event-Based
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- joysticks, notificações
- joysticks, mensagens
- joysticks, notificações baseadas em evento
- joysticks, limite de movimento
- notificações do joystick com base em eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640557"
---
# <a name="event-based-notifications"></a>Notificações de Event-Based

Você pode pedir ao sistema para enviar mensagens de joystick para um aplicativo sempre que a posição de um eixo de joystick for alterada por um valor maior do que o *limite de movimento* do dispositivo. O limite de movimento é a distância em que o joystick deve ser movido antes que uma mensagem de alteração de posição de joystick seja enviada para uma janela que tenha capturado o dispositivo. Para obter mais informações, [**consulte \_ mm JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)ou [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).

O limite é inicialmente zero. Você pode definir o limite de movimento usando a função [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) . Você pode recuperar a frequência de sondagem mínima do joystick usando a função [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .

 

 