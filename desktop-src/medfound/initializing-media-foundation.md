---
description: Inicializando Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inicializando Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202ab57db5821b252001a723eb8765493eb86362111da5c54e5e16e9fca4219a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268916"
---
# <a name="initializing-media-foundation"></a>Inicializando Media Foundation

Antes de usar Microsoft Media Foundation interfaces, você deve chamar a [**função MFStartup.**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Passe a constante **MF \_ VERSION**.


```C++
    hr = MFStartup(MF_VERSION);
```



A [**função MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) inicializa o Media Foundation plataforma. Se **MFStartup** retornar MF E BAD STARTUP VERSION, isso significa que seu aplicativo foi compilado usando uma versão dos headers do Media Foundation que não corresponderá às \_ \_ \_ DLLs Media Foundation em \_ seu sistema.

Para cada chamada para [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), seu aplicativo deve chamar [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).


```C++
MFShutdown();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[APIs Media Foundation Plataforma de Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



