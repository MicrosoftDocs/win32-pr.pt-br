---
title: Capturando a entrada do Conector
description: Capturando a entrada do Conector
ms.assetid: 1214fe5a-5a6a-4c6c-9b77-94eeb73f60da
keywords:
- joysticks, capturando entrada
- capturando a entrada do conector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d4e98d4e27e8bc5cc444ffe386aaab6ce2f1c3e8469588f6fe931358dd99a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989057"
---
# <a name="capturing-joystick-input"></a>Capturando a entrada do Conector

A maior parte do código que controla o ltda está na função de janela principal. Na parte a seguir do manipulador de mensagens, o aplicativo chama [**osetSetCapture para**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) capturar a entrada do usb USBID1.


```C++
case WM_CREATE: 
    if(joySetCapture(hWnd, JOYSTICKID1, NULL, FALSE)) 
    { 
        MessageBeep(MB_ICONEXCLAMATION); 
        MessageBox(hWnd, "Couldn't capture the joystick.", NULL, 
            MB_OK | MB_ICONEXCLAMATION); 
        PostMessage(hWnd,WM_CLOSE,0,0L); 
    } 
    break; 
 
```



 

 