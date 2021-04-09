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
# <a name="joystick-notifications"></a><span data-ttu-id="f987f-107">Notificações do joystick</span><span class="sxs-lookup"><span data-stu-id="f987f-107">Joystick Notifications</span></span>

<span data-ttu-id="f987f-108">Você pode capturar mensagens do joystick diretos para serem enviadas a uma função usando a função [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) .</span><span class="sxs-lookup"><span data-stu-id="f987f-108">You can capture direct joystick messages to be sent to a function by using the [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) function.</span></span> <span data-ttu-id="f987f-109">Somente um aplicativo por vez pode capturar mensagens de um joystick, mas você pode consultar o joystick de outro aplicativo usando a função [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) ou [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .</span><span class="sxs-lookup"><span data-stu-id="f987f-109">Only one application at a time can capture messages from a joystick, but you can query the joystick from another application by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) or [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

> [!Note]  
> <span data-ttu-id="f987f-110">Uma mensagem de joystick pode falhar ao acessar o aplicativo que capturou o joystick se um segundo aplicativo usa **joyGetPos** ou **joyGetPosEx** para consultar o joystick quase ao mesmo tempo em que a mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="f987f-110">A joystick message can fail to reach the application that captured the joystick if a second application uses **joyGetPos** or **joyGetPosEx** to query the joystick at approximately the same time that the message is sent.</span></span> <span data-ttu-id="f987f-111">Nesse caso, o segundo aplicativo poderia interceptar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f987f-111">In this case, the second application could intercept the message.</span></span>

 

<span data-ttu-id="f987f-112">Se você quiser capturar mensagens de dois joysticks anexados ao sistema, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) duas vezes, uma vez para cada joystick.</span><span class="sxs-lookup"><span data-stu-id="f987f-112">If you want to capture messages from two joysticks attached to the system, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) twice, once for each joystick.</span></span> <span data-ttu-id="f987f-113">Sua janela recebe mensagens separadas e distintas para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f987f-113">Your window receives separate and distinct messages for each device.</span></span>

<span data-ttu-id="f987f-114">Você pode liberar um joystick capturado usando a função [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) .</span><span class="sxs-lookup"><span data-stu-id="f987f-114">You can release a captured joystick by using the [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) function.</span></span> <span data-ttu-id="f987f-115">Se um aplicativo não liberar o joystick antes de terminar, o joystick será lançado automaticamente logo depois que a janela de captura for destruída.</span><span class="sxs-lookup"><span data-stu-id="f987f-115">If an application does not release the joystick before ending, the joystick is automatically released shortly after the capture window is destroyed.</span></span>

<span data-ttu-id="f987f-116">Não é possível capturar um joystick não conectado.</span><span class="sxs-lookup"><span data-stu-id="f987f-116">You cannot capture an unplugged joystick.</span></span> <span data-ttu-id="f987f-117">A função **joySetCapture** retornará JOYERR \_ desconectado se o dispositivo especificado estiver desconectado.</span><span class="sxs-lookup"><span data-stu-id="f987f-117">The **joySetCapture** function returns JOYERR\_UNPLUGGED if the specified device is unplugged.</span></span>

 

 