---
title: Conectando-se a um driver de captura
description: Conectando-se a um driver de captura
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- macro capDriverDisconnect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2161279f5b8b8dc528ee548d0a6a8ad6e9b397f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759630"
---
# <a name="connecting-to-a-capture-driver"></a>Conectando-se a um driver de captura

O exemplo a seguir conecta a janela de captura com o identificador *hWndC* ao driver MSVIDEO e, em seguida, desconecta-os usando a macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) :


```C++
fOK = SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0, 0L); 
// 
// Or, use the macro to connect to the MSVIDEO driver: 
// fOK = capDriverConnect(hWndC, 0); 
// 
// Place code to set up and capture video here. 
// 
capDriverDisconnect (hWndC); 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




