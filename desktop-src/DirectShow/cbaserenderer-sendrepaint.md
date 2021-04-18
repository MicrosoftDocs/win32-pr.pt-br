---
description: O método SendRepaint envia um evento Repaint para o Gerenciador do grafo de filtro.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Método CBaseRenderer. SendRepaint (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758860"
---
# <a name="cbaserenderersendrepaint-method"></a><span data-ttu-id="05087-103">Método CBaseRenderer. SendRepaint</span><span class="sxs-lookup"><span data-stu-id="05087-103">CBaseRenderer.SendRepaint method</span></span>

<span data-ttu-id="05087-104">O `SendRepaint` método envia um evento Repaint para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="05087-104">The `SendRepaint` method sends a repaint event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="05087-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05087-105">Syntax</span></span>


```C++
void SendRepaint();
```



## <a name="parameters"></a><span data-ttu-id="05087-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05087-106">Parameters</span></span>

<span data-ttu-id="05087-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="05087-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05087-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05087-108">Return value</span></span>

<span data-ttu-id="05087-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="05087-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05087-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="05087-110">Remarks</span></span>

<span data-ttu-id="05087-111">Esse método envia um evento de [**\_ redesenho de EC**](ec-repaint.md) para o Gerenciador do grafo de filtro se as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="05087-111">This method sends an [**EC\_REPAINT**](ec-repaint.md) event to the filter graph manager if the following conditions are true:</span></span>

-   <span data-ttu-id="05087-112">O pino de entrada está conectado.</span><span class="sxs-lookup"><span data-stu-id="05087-112">The input pin is connected.</span></span>
-   <span data-ttu-id="05087-113">O filtro não está liberando dados.</span><span class="sxs-lookup"><span data-stu-id="05087-113">The filter is not flushing data.</span></span>
-   <span data-ttu-id="05087-114">O fim do fluxo não foi atingido.</span><span class="sxs-lookup"><span data-stu-id="05087-114">The end-of-stream was not reached.</span></span>
-   <span data-ttu-id="05087-115">O sinalizador [**\_ bAbort CBaseRenderer:: m**](cbaserenderer-m-babort.md) é **false**.</span><span class="sxs-lookup"><span data-stu-id="05087-115">The [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag is **FALSE**.</span></span>
-   <span data-ttu-id="05087-116">O sinalizador [**\_ bRepaintStatus CBaseRenderer:: m**](cbaserenderer-m-brepaintstatus.md) é **true**.</span><span class="sxs-lookup"><span data-stu-id="05087-116">The [**CBaseRenderer::m\_bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) flag is **TRUE**.</span></span>

<span data-ttu-id="05087-117">Dependendo do estado do grafo, o \_ evento REpaint do EC pode fazer com que o filtro upstream envie novamente um exemplo; o grafo de filtro para buscar seu local atual ou o Gerenciador de gráficos de filtro para pausar momentaneamente.</span><span class="sxs-lookup"><span data-stu-id="05087-117">Depending on the state of the graph, the EC\_REPAINT event can cause the upstream filter to re-send a sample; the filter graph to seek to its current location; or the filter graph manager to pause momentarily.</span></span> <span data-ttu-id="05087-118">(Confira [**EC \_ Repaint**](ec-repaint.md).) Esse evento é potencialmente ineficiente, portanto, deve ser usado com moderação.</span><span class="sxs-lookup"><span data-stu-id="05087-118">(See [**EC\_REPAINT**](ec-repaint.md).) This event is potentially inefficient, so it should be used sparingly.</span></span> <span data-ttu-id="05087-119">No entanto, os renderizadores de vídeo às vezes precisam atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="05087-119">However, video renderers sometimes need to refresh the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="05087-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05087-120">Requirements</span></span>



| <span data-ttu-id="05087-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05087-121">Requirement</span></span> | <span data-ttu-id="05087-122">Valor</span><span class="sxs-lookup"><span data-stu-id="05087-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05087-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05087-123">Header</span></span><br/>  | <dl> <span data-ttu-id="05087-124"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05087-124"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05087-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05087-125">Library</span></span><br/> | <dl> <span data-ttu-id="05087-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="05087-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05087-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="05087-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05087-128">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="05087-128">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




