---
description: 'O método setpositiones define a posição atual e a posição de parada. Esse método implementa o método IMediaSeeking:: setposicionations.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Método CPosPassThru. setpositiones (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748018"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="fcb86-104">Método CPosPassThru. setpositiones</span><span class="sxs-lookup"><span data-stu-id="fcb86-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="fcb86-105">O `SetPositions` método define a posição atual e a posição de parada.</span><span class="sxs-lookup"><span data-stu-id="fcb86-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="fcb86-106">Esse método implementa o método [**IMediaSeeking:: Setposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="fcb86-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb86-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcb86-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fcb86-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcb86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcb86-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="fcb86-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb86-110">Ponteiro para uma variável que especifica a posição atual, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="fcb86-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="fcb86-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="fcb86-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb86-112">Combinação bit-a-de de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="fcb86-112">Bitwise combination of flags.</span></span> <span data-ttu-id="fcb86-113">Consulte [**IMediaSeeking:: Setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="fcb86-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="fcb86-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="fcb86-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb86-115">Ponteiro para uma variável que especifica a hora de parada, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="fcb86-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="fcb86-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="fcb86-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="fcb86-117">Combinação bit-a-de de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="fcb86-117">Bitwise combination of flags.</span></span> <span data-ttu-id="fcb86-118">Consulte [**IMediaSeeking:: Setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="fcb86-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcb86-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcb86-119">Return value</span></span>

<span data-ttu-id="fcb86-120">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="fcb86-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb86-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcb86-121">Requirements</span></span>



| <span data-ttu-id="fcb86-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcb86-122">Requirement</span></span> | <span data-ttu-id="fcb86-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fcb86-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb86-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcb86-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fcb86-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcb86-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fcb86-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcb86-126">Library</span></span><br/> | <dl> <span data-ttu-id="fcb86-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fcb86-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcb86-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcb86-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb86-129">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="fcb86-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




