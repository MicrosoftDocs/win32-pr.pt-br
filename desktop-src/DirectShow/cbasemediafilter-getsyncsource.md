---
description: 'O método getsyncprovider recupera o relógio de referência que o objeto está usando. Esse método implementa o método IMediaFilter:: getsync.'
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Método CBaseMediaFilter. getsyncize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748227"
---
# <a name="cbasemediafiltergetsyncsource-method"></a><span data-ttu-id="a6a68-104">Método CBaseMediaFilter. getsyncize</span><span class="sxs-lookup"><span data-stu-id="a6a68-104">CBaseMediaFilter.GetSyncSource method</span></span>

<span data-ttu-id="a6a68-105">O `GetSyncSource` método recupera o relógio de referência que o objeto está usando.</span><span class="sxs-lookup"><span data-stu-id="a6a68-105">The `GetSyncSource` method retrieves the reference clock that the object is using.</span></span> <span data-ttu-id="a6a68-106">Esse método implementa o método [**IMediaFilter:: getsync**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="a6a68-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a68-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6a68-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="a6a68-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6a68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a68-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="a6a68-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a68-110">Endereço de uma variável que recebe um ponteiro para a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) do relógio.</span><span class="sxs-lookup"><span data-stu-id="a6a68-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a68-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6a68-111">Return value</span></span>

<span data-ttu-id="a6a68-112">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="a6a68-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a68-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6a68-113">Remarks</span></span>

<span data-ttu-id="a6a68-114">Se o objeto não estiver usando um relógio de referência, *\* pClock* será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a6a68-114">If the object is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="a6a68-115">Quando o método retornar, se *\* pClock* for não **nulo**, a interface **IReferenceClock** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="a6a68-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="a6a68-116">Certifique-se de liberá-lo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="a6a68-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a68-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6a68-117">Requirements</span></span>



| <span data-ttu-id="a6a68-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a68-118">Requirement</span></span> | <span data-ttu-id="a6a68-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a6a68-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a68-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6a68-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a6a68-121"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6a68-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a6a68-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6a68-122">Library</span></span><br/> | <dl> <span data-ttu-id="a6a68-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a6a68-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a68-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6a68-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a68-125">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="a6a68-125">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




