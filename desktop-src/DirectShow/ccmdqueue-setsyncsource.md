---
description: O método setsyncto define o relógio usado para o tempo.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Método CCmdQueue. setsyncize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751252"
---
# <a name="ccmdqueuesetsyncsource-method"></a><span data-ttu-id="960e3-103">Método CCmdQueue. setsyncize</span><span class="sxs-lookup"><span data-stu-id="960e3-103">CCmdQueue.SetSyncSource method</span></span>

<span data-ttu-id="960e3-104">O `SetSyncSource` método define o relógio usado para o tempo.</span><span class="sxs-lookup"><span data-stu-id="960e3-104">The `SetSyncSource` method sets the clock used for timing.</span></span>

## <a name="syntax"></a><span data-ttu-id="960e3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="960e3-105">Syntax</span></span>


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a><span data-ttu-id="960e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="960e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="960e3-107">*pIrc*</span><span class="sxs-lookup"><span data-stu-id="960e3-107">*pIrc*</span></span> 
</dt> <dd>

<span data-ttu-id="960e3-108">Ponteiro para a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="960e3-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="960e3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="960e3-109">Return value</span></span>

<span data-ttu-id="960e3-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="960e3-110">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="960e3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="960e3-111">Requirements</span></span>



| <span data-ttu-id="960e3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="960e3-112">Requirement</span></span> | <span data-ttu-id="960e3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="960e3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="960e3-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="960e3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="960e3-115"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="960e3-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="960e3-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="960e3-116">Library</span></span><br/> | <dl> <span data-ttu-id="960e3-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="960e3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="960e3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="960e3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960e3-119">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="960e3-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




