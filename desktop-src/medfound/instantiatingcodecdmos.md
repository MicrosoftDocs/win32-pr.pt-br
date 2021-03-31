---
description: Criando uma instância do codec DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Criando uma instância do codec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920885"
---
# <a name="instantiating-codec-dmos"></a>Criando uma instância do codec DMOs

Você pode criar um codec DMO chamando a função com [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . Você deve passar o identificador de classe do DMO, o identificador de interface de **IMediaObject** e um ponteiro para um ponteiro **IMediaObject** .

Os identificadores de classe do codec DMOs são definidos como constantes no arquivo de cabeçalho wmcodecdsp. h.

A constante para o identificador de interface **IMediaObject** é \_ IMediaObject de IID.

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

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
