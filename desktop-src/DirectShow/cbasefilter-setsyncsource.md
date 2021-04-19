---
description: 'O método setsyncto define um relógio de referência para o filtro. Esse método implementa o método IMediaFilter:: setsincronizate.'
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Método CBaseFilter. setsyncize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8eaab23f1afd7e7b502d6828bc3f10cbfec49410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748650"
---
# <a name="cbasefiltersetsyncsource-method"></a><span data-ttu-id="f8890-104">Método CBaseFilter. setsyncize</span><span class="sxs-lookup"><span data-stu-id="f8890-104">CBaseFilter.SetSyncSource method</span></span>

<span data-ttu-id="f8890-105">O método **Setsyncto** define um relógio de referência para o filtro.</span><span class="sxs-lookup"><span data-stu-id="f8890-105">The **SetSyncSource** method sets a reference clock for the filter.</span></span> <span data-ttu-id="f8890-106">Esse método implementa o método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="f8890-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8890-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8890-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="f8890-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8890-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8890-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="f8890-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="f8890-110">Ponteiro para a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) do relógio ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f8890-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8890-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8890-111">Return value</span></span>

<span data-ttu-id="f8890-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f8890-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8890-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8890-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8890-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8890-114">Requirements</span></span>



| <span data-ttu-id="f8890-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8890-115">Requirement</span></span> | <span data-ttu-id="f8890-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f8890-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8890-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8890-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f8890-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8890-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8890-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8890-119">Library</span></span><br/> | <dl> <span data-ttu-id="f8890-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f8890-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8890-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8890-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8890-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="f8890-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




