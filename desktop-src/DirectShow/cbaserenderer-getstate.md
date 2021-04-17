---
description: O método GetState recupera o estado do filtro (em execução, parado ou pausado).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Método CBaseRenderer. GetState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769240"
---
# <a name="cbaserenderergetstate-method"></a><span data-ttu-id="b998f-103">Método CBaseRenderer. GetState</span><span class="sxs-lookup"><span data-stu-id="b998f-103">CBaseRenderer.GetState method</span></span>

<span data-ttu-id="b998f-104">O `GetState` método recupera o estado do filtro (em execução, parado ou pausado).</span><span class="sxs-lookup"><span data-stu-id="b998f-104">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="b998f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b998f-105">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="b998f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b998f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b998f-107">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="b998f-107">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="b998f-108">Intervalo de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b998f-108">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="b998f-109">*State*</span><span class="sxs-lookup"><span data-stu-id="b998f-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="b998f-110">Ponteiro para uma variável que recebe um membro do tipo enumerado de [**\_ estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , indicando o estado do filtro.</span><span class="sxs-lookup"><span data-stu-id="b998f-110">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b998f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b998f-111">Return value</span></span>

<span data-ttu-id="b998f-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b998f-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b998f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b998f-113">Return code</span></span>                                                                                                | <span data-ttu-id="b998f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b998f-114">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="b998f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b998f-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="b998f-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b998f-116">Success.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b998f-117"><dt>**VFW \_ S \_ State \_ intermediário**</dt></span><span class="sxs-lookup"><span data-stu-id="b998f-117"><dt>**VFW\_S\_STATE\_INTERMEDIATE**</dt></span></span> </dl> | <span data-ttu-id="b998f-118">O filtro está em transição para o estado indicado.</span><span class="sxs-lookup"><span data-stu-id="b998f-118">The filter is transitioning to the indicated state.</span></span><br/> |
| <dl> <span data-ttu-id="b998f-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b998f-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="b998f-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b998f-120">**NULL** pointer argument.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="b998f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b998f-121">Remarks</span></span>

<span data-ttu-id="b998f-122">Esse método substitui o método [**CBaseFilter:: GetState**](cbasefilter-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="b998f-122">This method overrides the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method.</span></span> <span data-ttu-id="b998f-123">Quando o renderizador é pausado, ele não conclui a transição de estado até receber um exemplo para renderizar.</span><span class="sxs-lookup"><span data-stu-id="b998f-123">When the renderer is paused, it does not complete the state transition until it receives a sample to render.</span></span> <span data-ttu-id="b998f-124">Se o tempo limite expirar antes da conclusão da transição de estado, o método retornará VFW \_ S \_ State \_ intermediário.</span><span class="sxs-lookup"><span data-stu-id="b998f-124">If the time-out expires before the state transition is complete, the method returns VFW\_S\_STATE\_INTERMEDIATE.</span></span>

## <a name="requirements"></a><span data-ttu-id="b998f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b998f-125">Requirements</span></span>



| <span data-ttu-id="b998f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b998f-126">Requirement</span></span> | <span data-ttu-id="b998f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b998f-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b998f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b998f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b998f-129"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b998f-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b998f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b998f-130">Library</span></span><br/> | <dl> <span data-ttu-id="b998f-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b998f-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b998f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b998f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b998f-133">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="b998f-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




