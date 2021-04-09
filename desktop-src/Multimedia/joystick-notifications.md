---
title: Notificações do joystick
description: Notificações do joystick
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- joysticks, notificações
- joysticks, mensagens
- joysticks capturados
- joysticks não conectados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007508"
---
# <a name="joystick-notifications"></a>Notificações do joystick

Você pode capturar mensagens do joystick diretos para serem enviadas a uma função usando a função [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) . Somente um aplicativo por vez pode capturar mensagens de um joystick, mas você pode consultar o joystick de outro aplicativo usando a função [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) ou [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

> [!Note]  
> Uma mensagem de joystick pode falhar ao acessar o aplicativo que capturou o joystick se um segundo aplicativo usa **joyGetPos** ou **joyGetPosEx** para consultar o joystick quase ao mesmo tempo em que a mensagem é enviada. Nesse caso, o segundo aplicativo poderia interceptar a mensagem.

 

Se você quiser capturar mensagens de dois joysticks anexados ao sistema, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) duas vezes, uma vez para cada joystick. Sua janela recebe mensagens separadas e distintas para cada dispositivo.

Você pode liberar um joystick capturado usando a função [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) . Se um aplicativo não liberar o joystick antes de terminar, o joystick será lançado automaticamente logo depois que a janela de captura for destruída.

Não é possível capturar um joystick não conectado. A função **joySetCapture** retornará JOYERR \_ desconectado se o dispositivo especificado estiver desconectado.

 

 