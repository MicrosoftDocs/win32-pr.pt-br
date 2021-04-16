---
description: Inicializando Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inicializando Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105768613"
---
# <a name="initializing-media-foundation"></a>Inicializando Media Foundation

Antes de usar qualquer Microsoft Media Foundation objetos ou interfaces, você deve chamar a função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Passe a versão constante **MF \_**.


```C++
    hr = MFStartup(MF_VERSION);
```



A função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Inicializa a plataforma Media Foundation. Se **MFStartup** retornar MF \_ e \_ \_ versão de inicialização inválida \_ , significa que seu aplicativo foi compilado usando uma versão dos cabeçalhos de Media Foundation que não corresponde ao Media Foundation DLLs no seu sistema.

Para cada chamada para [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), seu aplicativo deve chamar [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).


```C++
MFShutdown();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



