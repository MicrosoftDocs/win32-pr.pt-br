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
# <a name="event-based-notifications"></a><span data-ttu-id="9aa92-108">Notificações de Event-Based</span><span class="sxs-lookup"><span data-stu-id="9aa92-108">Event-Based Notifications</span></span>

<span data-ttu-id="9aa92-109">Você pode pedir ao sistema para enviar mensagens de joystick para um aplicativo sempre que a posição de um eixo de joystick for alterada por um valor maior do que o *limite de movimento* do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9aa92-109">You can ask the system to send joystick messages to an application whenever the position of a joystick axis changes by a value greater than the *movement threshold* of the device.</span></span> <span data-ttu-id="9aa92-110">O limite de movimento é a distância em que o joystick deve ser movido antes que uma mensagem de alteração de posição de joystick seja enviada para uma janela que tenha capturado o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9aa92-110">The movement threshold is the distance the joystick must be moved before a joystick position change message is sent to a window that has captured the device.</span></span> <span data-ttu-id="9aa92-111">Para obter mais informações, [**consulte \_ mm JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)ou [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).</span><span class="sxs-lookup"><span data-stu-id="9aa92-111">For more information, see [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1ZMOVE**](mm-joy1zmove.md), [**MM\_JOY2MOVE**](mm-joy2move.md), or [**MM\_JOY2ZMOVE**](mm-joy2zmove.md).</span></span>

<span data-ttu-id="9aa92-112">O limite é inicialmente zero.</span><span class="sxs-lookup"><span data-stu-id="9aa92-112">The threshold is initially zero.</span></span> <span data-ttu-id="9aa92-113">Você pode definir o limite de movimento usando a função [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) .</span><span class="sxs-lookup"><span data-stu-id="9aa92-113">You can set the movement threshold by using the [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) function.</span></span> <span data-ttu-id="9aa92-114">Você pode recuperar a frequência de sondagem mínima do joystick usando a função [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="9aa92-114">You can retrieve the minimum polling frequency of the joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span>

 

 