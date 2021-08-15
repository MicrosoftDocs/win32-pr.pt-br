---
title: Notificações de Time-Based
description: Notificações de Time-Based
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- joysticks, notificações
- joysticks, mensagens
- joysticks, notificações baseadas em tempo
- notificações do joystick com base no tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80052d5e728a7a5b00e6177a36c30f470fe80daeafbe39a12aa4c9a883766534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688246"
---
# <a name="time-based-notifications"></a>Notificações de Time-Based

Você pode notificar o sistema operacional para enviar mensagens de joystick para um aplicativo em intervalos de tempo regulares, definindo o parâmetro *fChanged* de [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) como **false** e especificando o comprimento do intervalo entre mensagens sucessivas. Para fazer isso, atribua o parâmetro *uPeriod* a um valor entre as frequências de sondagem mínima e máxima para o joystick. Você pode determinar esse intervalo usando a função [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , que preenche os membros **wPeriodMin** e **wPeriodMax** na estrutura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) . Se o valor de *uPeriod* estiver fora do intervalo de frequências de sondagem válidas para o joystick, o driver do joystick usará a frequência de sondagem mínima ou máxima, o que estiver mais próximo do valor *uPeriod* .

> [!Note]  
> Windows configura um evento de temporizador com cada chamada para **joySetCapture**.

 

 

 