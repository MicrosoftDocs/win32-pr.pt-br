---
description: Inciando DMOs codec
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Inciando DMOs codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180fcb6a3de7c581f48c7f78981e12b544963cbfb590e521d43413732bcc1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957546"
---
# <a name="instantiating-codec-dmos"></a>Inciando DMOs codec

Você pode criar um codec DMO chamando a [**função COM CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) Você deve passar o identificador de classe do DMO, o identificador de interface **de IMediaObject** e um ponteiro para **um ponteiro IMediaObject.**

Os identificadores de classe dos DMOs codec são definidos como constantes no arquivo de header wmcodecdsp.h.

A constante para o identificador de interface **IMediaObject** é IID \_ IMediaObject.

O exemplo de código a seguir demonstra como criar uma instância de um codec DMO:


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com DMOs codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
