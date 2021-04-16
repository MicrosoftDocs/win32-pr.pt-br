---
description: O método RegisterMediaTime armazena em cache os carimbos de data/hora do exemplo atual.
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
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
ms.openlocfilehash: ff741e58f74770c8a97c13252302d4ef86868af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751098"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="cd534-103">Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="cd534-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="cd534-104">O método [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) armazena em cache os carimbos de data/hora do exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="cd534-104">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd534-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd534-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="cd534-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd534-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd534-107">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="cd534-107">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="cd534-108">Hora de início da amostra, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="cd534-108">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="cd534-109">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="cd534-109">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="cd534-110">Hora de término da amostra, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="cd534-110">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd534-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd534-111">Return value</span></span>

<span data-ttu-id="cd534-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd534-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cd534-113">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd534-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="cd534-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cd534-114">Return code</span></span>                                                                          | <span data-ttu-id="cd534-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd534-115">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="cd534-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cd534-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cd534-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="cd534-117">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd534-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd534-118">Remarks</span></span>

<span data-ttu-id="cd534-119">Esse método armazena os valores de carimbo de data/hora fornecidos em *StartTime* e *EndTime*.</span><span class="sxs-lookup"><span data-stu-id="cd534-119">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="cd534-120">O método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera os mesmos valores.</span><span class="sxs-lookup"><span data-stu-id="cd534-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="cd534-121">O filtro deve chamar esse método para cada amostra que receber.</span><span class="sxs-lookup"><span data-stu-id="cd534-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="cd534-122">O método é sobrecarregado para aceitar um ponteiro para a amostra ou os próprios valores de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="cd534-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd534-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd534-123">Requirements</span></span>



| <span data-ttu-id="cd534-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd534-124">Requirement</span></span> | <span data-ttu-id="cd534-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cd534-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd534-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd534-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cd534-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd534-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd534-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd534-128">Library</span></span><br/> | <dl> <span data-ttu-id="cd534-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cd534-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




