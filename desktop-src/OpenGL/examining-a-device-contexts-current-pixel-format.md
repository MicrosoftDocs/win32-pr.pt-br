---
title: Examinando um formato de pixel atual de contextos de dispositivo
description: Use as funções GetPixelFormat e DescribePixelFormat para examinar o formato de pixel atual de um contexto de dispositivo, conforme mostrado no fragmento de código a seguir.
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- OpenGL em Windows,pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b76dd8db71356b16a5a258669ffe2938d0982ab5e1417389840610c57a0fcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361366"
---
# <a name="examining-a-device-contexts-current-pixel-format"></a>Examinando um formato de pixel atual de contextos de dispositivo

Use as [**funções GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) e [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) para examinar o formato de pixel atual de um contexto de dispositivo, conforme mostrado no fragmento de código a seguir.


```C++
PIXELFORMATDESCRIPTOR  pfd;
HDC    hdc;
int    iPixelFormat;
 
// if the device context has a current pixel format ...  
if (iPixelFormat = GetPixelFormat(hdc)) { 
 
    // obtain a detailed description of that pixel format  
    DescribePixelFormat(hdc, iPixelFormat, 
                             sizeof(PIXELFORMATDESCRIPTOR), &pfd); 
    }
```



 

 




