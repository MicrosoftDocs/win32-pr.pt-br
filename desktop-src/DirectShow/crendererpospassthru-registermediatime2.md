---
description: O método RegisterMediaTime armazena em cache os carimbos de data/hora do exemplo atual. Esse método usa os parâmetros *StartTime* e *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)-parâmetros StartTime e EndTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187827"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a><span data-ttu-id="96a66-104">Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)-parâmetros StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="96a66-104">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h) - StartTime and EndTime parameters</span></span>

<span data-ttu-id="96a66-105">O método [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) armazena em cache os carimbos de data/hora do exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="96a66-105">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a66-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96a66-106">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="96a66-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96a66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96a66-108">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="96a66-108">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="96a66-109">Hora de início da amostra, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="96a66-109">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="96a66-110">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="96a66-110">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="96a66-111">Hora de término da amostra, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="96a66-111">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96a66-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96a66-112">Return value</span></span>

<span data-ttu-id="96a66-113">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96a66-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="96a66-114">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="96a66-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="96a66-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="96a66-115">Return code</span></span>                                                                          | <span data-ttu-id="96a66-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="96a66-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="96a66-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96a66-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="96a66-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="96a66-118">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96a66-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="96a66-119">Remarks</span></span>

<span data-ttu-id="96a66-120">Esse método armazena os valores de carimbo de data/hora fornecidos em *StartTime* e *EndTime*.</span><span class="sxs-lookup"><span data-stu-id="96a66-120">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="96a66-121">O método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera os mesmos valores.</span><span class="sxs-lookup"><span data-stu-id="96a66-121">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="96a66-122">O filtro deve chamar esse método para cada amostra que receber.</span><span class="sxs-lookup"><span data-stu-id="96a66-122">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="96a66-123">O método é sobrecarregado para aceitar um ponteiro para a amostra ou os próprios valores de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="96a66-123">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a66-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96a66-124">Requirements</span></span>



| <span data-ttu-id="96a66-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="96a66-125">Requirement</span></span> | <span data-ttu-id="96a66-126">Valor</span><span class="sxs-lookup"><span data-stu-id="96a66-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a66-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96a66-127">Header</span></span>  | <span data-ttu-id="96a66-128">Ctlutil. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="96a66-128">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="96a66-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96a66-129">Library</span></span> | <span data-ttu-id="96a66-130">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="96a66-130">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




