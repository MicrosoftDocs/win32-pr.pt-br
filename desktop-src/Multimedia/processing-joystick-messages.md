---
title: Processando mensagens do joystick
description: Processando mensagens do joystick
ms.assetid: d21a9d49-1fc0-4899-9083-87c3cf4e0e62
keywords:
- joysticks, mensagens
- MM_JOY1MOVE mensagem
- MM_JOY1BUTTONDOWN mensagem
- MM_JOY1BUTTONUP mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f2337d392c0104dcb49839b19c5fb615481ee2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005320"
---
# <a name="processing-joystick-messages"></a><span data-ttu-id="d8f76-107">Processando mensagens do joystick</span><span class="sxs-lookup"><span data-stu-id="d8f76-107">Processing Joystick Messages</span></span>

<span data-ttu-id="d8f76-108">O exemplo a seguir ilustra como um aplicativo pode responder a movimentos e alterações de joystick nos Estados de botão.</span><span class="sxs-lookup"><span data-stu-id="d8f76-108">The following example illustrates how an application could respond to joystick movements and changes in the button states.</span></span> <span data-ttu-id="d8f76-109">Quando o joystick muda de posição, o aplicativo move o cursor e, se um dos botões é pressionado, desenha um buraco de marcador na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d8f76-109">When the joystick changes position, the application moves the cursor and, if either button is pressed, draws a bullet hole on the desktop.</span></span> <span data-ttu-id="d8f76-110">Quando um botão de joystick é pressionado, o aplicativo desenha um orifício na área de trabalho e reproduz um som continuamente até que um botão seja liberado.</span><span class="sxs-lookup"><span data-stu-id="d8f76-110">When a joystick button is pressed, the application draws a hole on the desktop and plays a sound continuously until a button is released.</span></span> <span data-ttu-id="d8f76-111">As mensagens a serem observadas são [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md)e [**mm \_ JOY1BUTTONUP**](mm-joy1buttonup.md).</span><span class="sxs-lookup"><span data-stu-id="d8f76-111">The messages to watch are [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1BUTTONDOWN**](mm-joy1buttondown.md), and [**MM\_JOY1BUTTONUP**](mm-joy1buttonup.md).</span></span>


```C++
case MM_JOY1MOVE :                     // changed position 
    if((UINT) wParam & (JOY_BUTTON1 | JOY_BUTTON2)) 
        DrawFire(hWnd); 
    DrawSight(lParam);                 // calculates new cursor position 
    break; 
case MM_JOY1BUTTONDOWN :               // button is down 
    if((UINT) wParam & JOY_BUTTON1) 
    { 
        PlaySound(lpButton1, SND_LOOP | SND_ASYNC | SND_MEMORY); 
        DrawFire(hWnd); 
    } 
    else if((UINT) wParam & JOY_BUTTON2) 
    { 
        PlaySound(lpButton2, SND_ASYNC | SND_MEMORY |  SND_LOOP); 
        DrawFire(hWnd); 
    } 
    break; 
case MM_JOY1BUTTONUP :                 // button is up 
    sndPlaySound(NULL, 0);             // stops the sound 
    break; 

```



 

 




