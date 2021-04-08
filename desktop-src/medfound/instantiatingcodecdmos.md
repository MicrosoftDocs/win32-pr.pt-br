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
# <a name="instantiating-codec-dmos"></a><span data-ttu-id="e0ed7-103">Criando uma instância do codec DMOs</span><span class="sxs-lookup"><span data-stu-id="e0ed7-103">Instantiating Codec DMOs</span></span>

<span data-ttu-id="e0ed7-104">Você pode criar um codec DMO chamando a função com [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="e0ed7-104">You can create a codec DMO by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="e0ed7-105">Você deve passar o identificador de classe do DMO, o identificador de interface de **IMediaObject** e um ponteiro para um ponteiro **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="e0ed7-105">You must pass the class identifier of the DMO, the interface identifier of **IMediaObject**, and a pointer to an **IMediaObject** pointer.</span></span>

<span data-ttu-id="e0ed7-106">Os identificadores de classe do codec DMOs são definidos como constantes no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="e0ed7-106">The class identifiers of the codec DMOs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="e0ed7-107">A constante para o identificador de interface **IMediaObject** é \_ IMediaObject de IID.</span><span class="sxs-lookup"><span data-stu-id="e0ed7-107">The constant for the **IMediaObject** interface identifier is IID\_IMediaObject.</span></span>

<span data-ttu-id="e0ed7-108">O exemplo de código a seguir demonstra como criar uma instância de um codec DMO:</span><span class="sxs-lookup"><span data-stu-id="e0ed7-108">The following code example demonstrates how to create an instance of a codec DMO:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e0ed7-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0ed7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ed7-110">Trabalhando com codec DMOs</span><span class="sxs-lookup"><span data-stu-id="e0ed7-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
