---
title: Funções de wrapper de plug-in
description: Funções de wrapper que permitem chamar uma função pública em qualquer adaptador anexado ao pipeline sem adquirir manualmente um ponteiro para o adaptador.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- API de Windows Biometric Framework de API Windows Biometric Framework, funções de wrapper de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822915"
---
# <a name="plug-in-wrapper-functions"></a><span data-ttu-id="97eaf-104">Funções de wrapper de plug-in</span><span class="sxs-lookup"><span data-stu-id="97eaf-104">Plug-in Wrapper Functions</span></span>

<span data-ttu-id="97eaf-105">A API de Windows Biometric Framework inclui funções de wrapper que permitem chamar uma função pública em qualquer adaptador anexado ao pipeline sem adquirir manualmente um ponteiro para o adaptador.</span><span class="sxs-lookup"><span data-stu-id="97eaf-105">The Windows Biometric Framework API includes wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span> <span data-ttu-id="97eaf-106">Cada wrapper verifica os argumentos de entrada, recupera um ponteiro de adaptador e chama a função solicitada.</span><span class="sxs-lookup"><span data-stu-id="97eaf-106">Each wrapper checks the input arguments, retrieves an adapter pointer, and calls the requested function.</span></span> <span data-ttu-id="97eaf-107">Por exemplo, o wrapper **WbioEngineSetHashAlgorithm** tem a assinatura a seguir.</span><span class="sxs-lookup"><span data-stu-id="97eaf-107">For example, the **WbioEngineSetHashAlgorithm** wrapper has the following signature.</span></span>


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



<span data-ttu-id="97eaf-108">A função verifica se o argumento de *pipeline* não é **nulo**, se existe um adaptador de mecanismo e se a função [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) existe.</span><span class="sxs-lookup"><span data-stu-id="97eaf-108">The function verifies that the *Pipeline* argument is not **NULL**, that an engine adapter exists, and that the [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) function exists.</span></span> <span data-ttu-id="97eaf-109">Todas as funções de wrapper são definidas no \_ arquivo de cabeçalho WinBio Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="97eaf-109">All wrapper functions are defined in the Winbio\_adapter.h header file.</span></span> <span data-ttu-id="97eaf-110">Os tópicos a seguir discutem os wrappers disponíveis.</span><span class="sxs-lookup"><span data-stu-id="97eaf-110">The following topics discuss the available wrappers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="97eaf-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="97eaf-111">In this section</span></span>



| <span data-ttu-id="97eaf-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="97eaf-112">Topic</span></span>                                                               | <span data-ttu-id="97eaf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="97eaf-113">Description</span></span>                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97eaf-114">Wrappers do adaptador do mecanismo</span><span class="sxs-lookup"><span data-stu-id="97eaf-114">Engine Adapter Wrappers</span></span>](engine-adapter-wrappers.md)<br/>   | <span data-ttu-id="97eaf-115">Funções que você pode usar para chamar funções em seu adaptador de mecanismo.</span><span class="sxs-lookup"><span data-stu-id="97eaf-115">Functions that you can use to call functions on your engine adapter.</span></span> <span data-ttu-id="97eaf-116">Essas funções são definidas em WinBio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="97eaf-116">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="97eaf-117">Wrappers do adaptador do sensor</span><span class="sxs-lookup"><span data-stu-id="97eaf-117">Sensor Adapter Wrappers</span></span>](sensor-adapter-wrappers.md)<br/>   | <span data-ttu-id="97eaf-118">Funções que você pode usar para chamar funções no adaptador do sensor.</span><span class="sxs-lookup"><span data-stu-id="97eaf-118">Functions that you can use to call functions on your sensor adapter.</span></span> <span data-ttu-id="97eaf-119">Essas funções são definidas em WinBio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="97eaf-119">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="97eaf-120">Wrappers do adaptador de armazenamento</span><span class="sxs-lookup"><span data-stu-id="97eaf-120">Storage Adapter Wrappers</span></span>](storage-adapter-wrappers.md)<br/> | <span data-ttu-id="97eaf-121">Funções que você pode usar para chamar funções em seu adaptador de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="97eaf-121">Functions that you can use to call functions on your storage adapter.</span></span> <span data-ttu-id="97eaf-122">Essas funções são definidas em WinBio \_ Adapter. h.</span><span class="sxs-lookup"><span data-stu-id="97eaf-122">These functions are defined in Winbio\_adapter.h.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="97eaf-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97eaf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97eaf-124">Referência de plug-in</span><span class="sxs-lookup"><span data-stu-id="97eaf-124">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> </dl>

 

 





