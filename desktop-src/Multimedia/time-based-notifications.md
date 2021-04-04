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
ms.openlocfilehash: 15dff2a6140bd993157f20e92488afce1b646e20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917161"
---
# <a name="time-based-notifications"></a><span data-ttu-id="65641-107">Notificações de Time-Based</span><span class="sxs-lookup"><span data-stu-id="65641-107">Time-Based Notifications</span></span>

<span data-ttu-id="65641-108">Você pode notificar o sistema operacional para enviar mensagens de joystick para um aplicativo em intervalos de tempo regulares, definindo o parâmetro *fChanged* de [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) como **false** e especificando o comprimento do intervalo entre mensagens sucessivas.</span><span class="sxs-lookup"><span data-stu-id="65641-108">You can notify the operating system to send joystick messages to an application at regular time intervals by setting the *fChanged* parameter of [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to **FALSE** and by specifying the interval length between successive messages.</span></span> <span data-ttu-id="65641-109">Para fazer isso, atribua o parâmetro *uPeriod* a um valor entre as frequências de sondagem mínima e máxima para o joystick.</span><span class="sxs-lookup"><span data-stu-id="65641-109">To do this, assign the *uPeriod* parameter a value between the minimum and maximum polling frequencies for the joystick.</span></span> <span data-ttu-id="65641-110">Você pode determinar esse intervalo usando a função [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , que preenche os membros **wPeriodMin** e **wPeriodMax** na estrutura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) .</span><span class="sxs-lookup"><span data-stu-id="65641-110">You can determine this range by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function, which fills the **wPeriodMin** and **wPeriodMax** members in the [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure.</span></span> <span data-ttu-id="65641-111">Se o valor de *uPeriod* estiver fora do intervalo de frequências de sondagem válidas para o joystick, o driver do joystick usará a frequência de sondagem mínima ou máxima, o que estiver mais próximo do valor *uPeriod* .</span><span class="sxs-lookup"><span data-stu-id="65641-111">If the *uPeriod* value is outside the range of valid polling frequencies for the joystick, the joystick driver uses the minimum or maximum polling frequency, whichever is closer to the *uPeriod* value.</span></span>

> [!Note]  
> <span data-ttu-id="65641-112">O Windows configura um evento de temporizador com cada chamada para **joySetCapture**.</span><span class="sxs-lookup"><span data-stu-id="65641-112">Windows sets up a timer event with each call to **joySetCapture**.</span></span>

 

 

 