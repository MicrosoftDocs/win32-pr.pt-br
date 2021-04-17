---
description: 'O método getsyncprovider recupera o relógio de referência que o filtro está usando. Esse método implementa o método IMediaFilter:: getsync.'
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Método CBaseFilter. getsyncize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749639"
---
# <a name="cbasefiltergetsyncsource-method"></a><span data-ttu-id="2bf72-104">Método CBaseFilter. getsyncize</span><span class="sxs-lookup"><span data-stu-id="2bf72-104">CBaseFilter.GetSyncSource method</span></span>

<span data-ttu-id="2bf72-105">O `GetSyncSource` método recupera o relógio de referência que o filtro está usando.</span><span class="sxs-lookup"><span data-stu-id="2bf72-105">The `GetSyncSource` method retrieves the reference clock that the filter is using.</span></span> <span data-ttu-id="2bf72-106">Esse método implementa o método [**IMediaFilter:: getsync**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="2bf72-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf72-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bf72-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="2bf72-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bf72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf72-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="2bf72-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="2bf72-110">Endereço de uma variável que recebe um ponteiro para a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) do relógio.</span><span class="sxs-lookup"><span data-stu-id="2bf72-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf72-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bf72-111">Return value</span></span>

<span data-ttu-id="2bf72-112">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="2bf72-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf72-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bf72-113">Remarks</span></span>

<span data-ttu-id="2bf72-114">Se o filtro não estiver usando um relógio de referência, *\* pClock* será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2bf72-114">If the filter is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="2bf72-115">Quando o método retornar, se *\* pClock* for não **nulo**, a interface **IReferenceClock** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="2bf72-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="2bf72-116">Certifique-se de liberá-lo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="2bf72-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bf72-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bf72-117">Requirements</span></span>



| <span data-ttu-id="2bf72-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bf72-118">Requirement</span></span> | <span data-ttu-id="2bf72-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2bf72-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf72-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2bf72-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2bf72-121"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf72-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2bf72-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bf72-122">Library</span></span><br/> | <dl> <span data-ttu-id="2bf72-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf72-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf72-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bf72-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf72-125">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="2bf72-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




