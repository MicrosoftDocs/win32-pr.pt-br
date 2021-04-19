---
description: 'O método Run executa o filtro. Esse método implementa o método IMediaFilter:: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Método CBaseFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749037"
---
# <a name="cbasefilterrun-method"></a><span data-ttu-id="12ea3-104">Método CBaseFilter. Run</span><span class="sxs-lookup"><span data-stu-id="12ea3-104">CBaseFilter.Run method</span></span>

<span data-ttu-id="12ea3-105">O `Run` método executa o filtro.</span><span class="sxs-lookup"><span data-stu-id="12ea3-105">The `Run` method runs the filter.</span></span> <span data-ttu-id="12ea3-106">Esse método implementa o método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="12ea3-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12ea3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12ea3-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="12ea3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12ea3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ea3-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="12ea3-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="12ea3-110">Tempo de referência correspondente ao tempo de transmissão 0.</span><span class="sxs-lookup"><span data-stu-id="12ea3-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ea3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12ea3-111">Return value</span></span>

<span data-ttu-id="12ea3-112">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="12ea3-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="12ea3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="12ea3-113">Remarks</span></span>

<span data-ttu-id="12ea3-114">Se o filtro for interrompido, esse método pausará o filtro chamando o método [**CBaseFilter::P ause**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="12ea3-114">If the filter is stopped, this method pauses the filter by calling the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="12ea3-115">Em seguida, ele chama o método [**CBasePin:: Run**](cbasepin-run.md) em cada um dos Pins conectados do filtro.</span><span class="sxs-lookup"><span data-stu-id="12ea3-115">It then calls the [**CBasePin::Run**](cbasepin-run.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="12ea3-116">Por fim, ele define a variável de membro de [**\_ estado CBaseFilter:: m**](cbasefilter-m-state.md) para o estado \_ em execução.</span><span class="sxs-lookup"><span data-stu-id="12ea3-116">Finally, it sets the [**CBaseFilter::m\_State**](cbasefilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="12ea3-117">O tempo de fluxo é calculado como o tempo de referência atual menos *tStart*.</span><span class="sxs-lookup"><span data-stu-id="12ea3-117">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="12ea3-118">Um exemplo de mídia com um carimbo de data/hora igual a zero deve ser renderizado no horário *tStart*.</span><span class="sxs-lookup"><span data-stu-id="12ea3-118">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ea3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12ea3-119">Requirements</span></span>



| <span data-ttu-id="12ea3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ea3-120">Requirement</span></span> | <span data-ttu-id="12ea3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="12ea3-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12ea3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12ea3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12ea3-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12ea3-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="12ea3-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12ea3-124">Library</span></span><br/> | <dl> <span data-ttu-id="12ea3-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="12ea3-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ea3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="12ea3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ea3-127">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="12ea3-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




