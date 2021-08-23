---
title: Conectando-se a um driver de captura
description: Conectando-se a um driver de captura
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- macro capDriverDisconnect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34e606c439143400f1ea1845db37e7faf93009350254c173c4003400c3996f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144859"
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

 

 




