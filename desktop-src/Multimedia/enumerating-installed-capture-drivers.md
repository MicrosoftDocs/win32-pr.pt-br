---
title: Enumerando os drivers de captura instalados
description: Enumerando os drivers de captura instalados
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- função capGetDriverDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a053b2de7a69a712914926dbd2ab72be9d1732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916371"
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

 

 




