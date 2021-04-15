---
description: A função DumpGraph envia informações sobre um grafo de filtro para o local de saída de depuração. Ignorado em compilações de varejo.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Função DumpGraph (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747572"
---
# <a name="dumpgraph-function"></a><span data-ttu-id="c90ac-104">Função DumpGraph</span><span class="sxs-lookup"><span data-stu-id="c90ac-104">DumpGraph function</span></span>

<span data-ttu-id="c90ac-105">A `DumpGraph` função envia informações sobre um grafo de filtro para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="c90ac-105">The `DumpGraph` function sends information about a filter graph to the debug output location.</span></span> <span data-ttu-id="c90ac-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="c90ac-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c90ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c90ac-107">Syntax</span></span>


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a><span data-ttu-id="c90ac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c90ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c90ac-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="c90ac-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="c90ac-110">Ponteiro para a interface [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="c90ac-110">Pointer to the [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface on the filter graph manager.</span></span>

</dd> <dt>

<span data-ttu-id="c90ac-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="c90ac-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="c90ac-112">Nível de log.</span><span class="sxs-lookup"><span data-stu-id="c90ac-112">Logging level.</span></span> <span data-ttu-id="c90ac-113">A função gera uma \_ mensagem de rastreamento de log com o nível de log especificado.</span><span class="sxs-lookup"><span data-stu-id="c90ac-113">The function generates a LOG\_TRACE message with the specified logging level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c90ac-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c90ac-114">Return value</span></span>

<span data-ttu-id="c90ac-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c90ac-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c90ac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c90ac-116">Requirements</span></span>



| <span data-ttu-id="c90ac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c90ac-117">Requirement</span></span> | <span data-ttu-id="c90ac-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c90ac-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c90ac-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c90ac-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c90ac-120"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c90ac-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c90ac-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c90ac-121">Library</span></span><br/> | <dl> <span data-ttu-id="c90ac-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c90ac-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c90ac-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c90ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c90ac-124">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="c90ac-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




