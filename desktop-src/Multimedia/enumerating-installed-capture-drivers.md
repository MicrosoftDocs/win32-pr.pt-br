---
title: Enumerando os drivers de captura instalados
description: Enumerando os drivers de captura instalados
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- função capGetDriverDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8fe85103259354bcc3b42834ecaff03d660eb408cda8191e5e0abea7393d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988645"
---
# <a name="enumerating-installed-capture-drivers"></a>Enumerando os drivers de captura instalados

O exemplo a seguir usa a função [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) para obter os nomes e as versões dos drivers de captura instalados.


```C++
char szDeviceName[80];
char szDeviceVersion[80];

for (wIndex = 0; wIndex < 10; wIndex++) 
{
    if (capGetDriverDescription(
            wIndex, 
            szDeviceName, 
            sizeof (szDeviceName), 
            szDeviceVersion, 
            sizeof (szDeviceVersion)
        )) 
    {
        // Append name to list of installed capture drivers
        // and then let the user select a driver to use.
    }
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




