---
title: Time-Based notificações
description: Time-Based notificações
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- porões, notificações
- joysticks, mensagens
- notificações baseadas em tempo
- notificações de tempo de base de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80052d5e728a7a5b00e6177a36c30f470fe80daeafbe39a12aa4c9a883766534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688246"
---
# <a name="time-based-notifications"></a>Time-Based notificações

Você pode notificar o sistema operacional para enviar mensagens de chang para um aplicativo em intervalos de tempo regulares definindo o parâmetro *fChanged* de [**intervalSetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) como **FALSE** e especificando o comprimento do intervalo entre mensagens sucessivas. Para fazer isso, atribua ao *parâmetro uPeriod* um valor entre as frequências de sondagem mínima e máxima para o portal. Você pode determinar esse intervalo usando a [**funçãogetGetDevCaps,**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) que preenche os **membros wPeriodMin** e **wPeriodMax** na estrutura [**DECAPS.**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) Se o *valor uPeriod* estiver fora do intervalo de frequências de sondagem válidas para o driver de controle, o driver do portal usará a frequência de sondagem mínima ou máxima, o que estiver mais próximo do *valor uPeriod.*

> [!Note]  
> Windows configura um evento de temporizador com cada chamada para **osetCapture.**

 

 

 