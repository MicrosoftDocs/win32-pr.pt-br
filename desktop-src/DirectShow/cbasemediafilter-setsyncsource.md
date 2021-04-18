---
description: 'O método setsyncprovider define um relógio de referência para o objeto. Esse método implementa o método IMediaFilter:: setsincronizate.'
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Método CBaseMediaFilter. setsyncize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748644"
---
# <a name="cbasemediafiltersetsyncsource-method"></a><span data-ttu-id="1a664-104">Método CBaseMediaFilter. setsyncize</span><span class="sxs-lookup"><span data-stu-id="1a664-104">CBaseMediaFilter.SetSyncSource method</span></span>

<span data-ttu-id="1a664-105">O `SetSyncSource` método define um relógio de referência para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1a664-105">The `SetSyncSource` method sets a reference clock for the object.</span></span> <span data-ttu-id="1a664-106">Esse método implementa o método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="1a664-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a664-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a664-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="1a664-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a664-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a664-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="1a664-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="1a664-110">Ponteiro para a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) do relógio ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1a664-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a664-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a664-111">Return value</span></span>

<span data-ttu-id="1a664-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1a664-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a664-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a664-113">Requirements</span></span>



| <span data-ttu-id="1a664-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a664-114">Requirement</span></span> | <span data-ttu-id="1a664-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1a664-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a664-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a664-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1a664-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a664-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1a664-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a664-118">Library</span></span><br/> | <dl> <span data-ttu-id="1a664-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1a664-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a664-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a664-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a664-121">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="1a664-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




