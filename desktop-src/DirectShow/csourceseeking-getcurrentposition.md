---
description: O método GetCurrentPosition recupera a posição atual, em relação à duração total do fluxo. Não implementado.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Método CSourceSeeking. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752080"
---
# <a name="csourceseekinggetcurrentposition-method"></a><span data-ttu-id="b05cd-104">Método CSourceSeeking. GetCurrentPosition</span><span class="sxs-lookup"><span data-stu-id="b05cd-104">CSourceSeeking.GetCurrentPosition method</span></span>

<span data-ttu-id="b05cd-105">O `GetCurrentPosition` método recupera a posição atual, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="b05cd-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="b05cd-106">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="b05cd-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="b05cd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b05cd-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="b05cd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b05cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b05cd-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="b05cd-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="b05cd-110">Ponteiro para uma variável que recebe a posição atual, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="b05cd-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b05cd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b05cd-111">Return value</span></span>

<span data-ttu-id="b05cd-112">Retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="b05cd-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b05cd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b05cd-113">Remarks</span></span>

<span data-ttu-id="b05cd-114">Os filtros de origem normalmente não dão suporte a esse método.</span><span class="sxs-lookup"><span data-stu-id="b05cd-114">Source filters typically do not support this method.</span></span> <span data-ttu-id="b05cd-115">Em vez disso, os filtros de renderização relatam a posição atual por meio da classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="b05cd-115">Instead, renderer filters report the current position through the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="b05cd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b05cd-116">Requirements</span></span>



| <span data-ttu-id="b05cd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b05cd-117">Requirement</span></span> | <span data-ttu-id="b05cd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b05cd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b05cd-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b05cd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b05cd-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b05cd-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b05cd-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b05cd-121">Library</span></span><br/> | <dl> <span data-ttu-id="b05cd-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b05cd-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b05cd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b05cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b05cd-124">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="b05cd-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




