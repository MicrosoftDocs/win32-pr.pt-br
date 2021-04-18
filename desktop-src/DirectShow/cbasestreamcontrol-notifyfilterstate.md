---
description: O método NotifyFilterState notifica o PIN quando o estado do filtro é alterado.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Método CBaseStreamControl. NotifyFilterState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751903"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a><span data-ttu-id="f9f48-103">Método CBaseStreamControl. NotifyFilterState</span><span class="sxs-lookup"><span data-stu-id="f9f48-103">CBaseStreamControl.NotifyFilterState method</span></span>

<span data-ttu-id="f9f48-104">O `NotifyFilterState` método notifica o PIN quando o estado do filtro é alterado.</span><span class="sxs-lookup"><span data-stu-id="f9f48-104">The `NotifyFilterState` method notifies the pin when the filter's state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f48-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9f48-105">Syntax</span></span>


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a><span data-ttu-id="f9f48-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9f48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9f48-107">*novo \_ estado*</span><span class="sxs-lookup"><span data-stu-id="f9f48-107">*new\_state*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f48-108">Especifica o novo estado, como um membro da enumeração [**de \_ estado do filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="f9f48-108">Specifies the new state, as a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="f9f48-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="f9f48-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f9f48-110">Especifica a hora de início.</span><span class="sxs-lookup"><span data-stu-id="f9f48-110">Specifies the start time.</span></span> <span data-ttu-id="f9f48-111">Se o estado do novo filtro for \_ em execução, passe o valor do método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="f9f48-111">If the new filter state is State\_Running, pass in the value from the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span> <span data-ttu-id="f9f48-112">Caso contrário, use o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f9f48-112">Otherwise, use the default value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9f48-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9f48-113">Return value</span></span>

<span data-ttu-id="f9f48-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f9f48-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9f48-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9f48-115">Remarks</span></span>

<span data-ttu-id="f9f48-116">Esse método faz com que o método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) pare de esperar.</span><span class="sxs-lookup"><span data-stu-id="f9f48-116">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="f9f48-117">Chame esse método sempre que o filtro proprietário mudar de estado.</span><span class="sxs-lookup"><span data-stu-id="f9f48-117">Call this method whenever the owning filter changes state.</span></span>

## <a name="examples"></a><span data-ttu-id="f9f48-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9f48-118">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a><span data-ttu-id="f9f48-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9f48-119">Requirements</span></span>



| <span data-ttu-id="f9f48-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9f48-120">Requirement</span></span> | <span data-ttu-id="f9f48-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f9f48-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f48-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9f48-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f9f48-123"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9f48-123"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f9f48-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9f48-124">Library</span></span><br/> | <dl> <span data-ttu-id="f9f48-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f9f48-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9f48-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9f48-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f48-127">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="f9f48-127">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




