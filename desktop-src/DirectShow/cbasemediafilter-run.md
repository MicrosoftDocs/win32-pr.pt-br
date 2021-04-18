---
description: 'O método Run executa o objeto. Esse método implementa o método IMediaFilter:: Run.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Método CBaseMediaFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749635"
---
# <a name="cbasemediafilterrun-method"></a><span data-ttu-id="58652-104">Método CBaseMediaFilter. Run</span><span class="sxs-lookup"><span data-stu-id="58652-104">CBaseMediaFilter.Run method</span></span>

<span data-ttu-id="58652-105">O `Run` método executa o objeto.</span><span class="sxs-lookup"><span data-stu-id="58652-105">The `Run` method runs the object.</span></span> <span data-ttu-id="58652-106">Esse método implementa o método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="58652-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="58652-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58652-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="58652-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58652-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58652-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="58652-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="58652-110">Tempo de referência correspondente ao tempo de transmissão 0.</span><span class="sxs-lookup"><span data-stu-id="58652-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58652-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58652-111">Return value</span></span>

<span data-ttu-id="58652-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58652-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="58652-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="58652-113">Remarks</span></span>

<span data-ttu-id="58652-114">Se o objeto for interrompido, esse método pausará o objeto chamando o método [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="58652-114">If the object is stopped, this method pauses the object by calling the [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md) method.</span></span> <span data-ttu-id="58652-115">Em seguida, ele define a variável de membro de [**\_ estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) para o estado \_ em execução.</span><span class="sxs-lookup"><span data-stu-id="58652-115">It then sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="58652-116">O tempo de fluxo é calculado como o tempo de referência atual menos *tStart*.</span><span class="sxs-lookup"><span data-stu-id="58652-116">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="58652-117">Um exemplo de mídia com um carimbo de data/hora igual a zero deve ser renderizado no horário *tStart*.</span><span class="sxs-lookup"><span data-stu-id="58652-117">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="58652-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58652-118">Requirements</span></span>



| <span data-ttu-id="58652-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="58652-119">Requirement</span></span> | <span data-ttu-id="58652-120">Valor</span><span class="sxs-lookup"><span data-stu-id="58652-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58652-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58652-121">Header</span></span><br/>  | <dl> <span data-ttu-id="58652-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58652-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="58652-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58652-123">Library</span></span><br/> | <dl> <span data-ttu-id="58652-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="58652-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58652-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="58652-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58652-126">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="58652-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




