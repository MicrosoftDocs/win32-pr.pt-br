---
description: O método setsyncize notifica a classe base do relógio de referência atual.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Método CBaseStreamControl. setsyncize (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759325"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a><span data-ttu-id="d00b9-103">Método CBaseStreamControl. setsyncize</span><span class="sxs-lookup"><span data-stu-id="d00b9-103">CBaseStreamControl.SetSyncSource method</span></span>

<span data-ttu-id="d00b9-104">O `SetSyncSource` método notifica a classe base do relógio de referência atual.</span><span class="sxs-lookup"><span data-stu-id="d00b9-104">The `SetSyncSource` method notifies the base class of the current reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="d00b9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d00b9-105">Syntax</span></span>


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a><span data-ttu-id="d00b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d00b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d00b9-107">*pRefClock*</span><span class="sxs-lookup"><span data-stu-id="d00b9-107">*pRefClock*</span></span> 
</dt> <dd>

<span data-ttu-id="d00b9-108">Ponteiro para a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) do relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="d00b9-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface of the reference clock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d00b9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d00b9-109">Return value</span></span>

<span data-ttu-id="d00b9-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d00b9-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d00b9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d00b9-111">Remarks</span></span>

<span data-ttu-id="d00b9-112">Chame esse método de dentro do método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) do filtro.</span><span class="sxs-lookup"><span data-stu-id="d00b9-112">Call this method from inside the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span> <span data-ttu-id="d00b9-113">A classe **CBaseStreamControl** usa a interface **IReferenceClock** para garantir que ela não descarte amostras muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d00b9-113">The **CBaseStreamControl** class uses the **IReferenceClock** interface to ensure that it does not discard samples too quickly.</span></span>

## <a name="examples"></a><span data-ttu-id="d00b9-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d00b9-114">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a><span data-ttu-id="d00b9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d00b9-115">Requirements</span></span>



| <span data-ttu-id="d00b9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d00b9-116">Requirement</span></span> | <span data-ttu-id="d00b9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d00b9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d00b9-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d00b9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d00b9-119"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d00b9-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d00b9-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d00b9-120">Library</span></span><br/> | <dl> <span data-ttu-id="d00b9-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d00b9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d00b9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d00b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00b9-123">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="d00b9-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




