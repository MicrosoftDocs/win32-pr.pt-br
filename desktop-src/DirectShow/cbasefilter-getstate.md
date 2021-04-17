---
description: 'O método GetState recupera o estado do filtro (em execução, parado ou pausado). Esse método implementa o método IMediaFilter:: GetState.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Método CBaseFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749042"
---
# <a name="cbasefiltergetstate-method"></a><span data-ttu-id="9e05a-104">Método CBaseFilter. GetState</span><span class="sxs-lookup"><span data-stu-id="9e05a-104">CBaseFilter.GetState method</span></span>

<span data-ttu-id="9e05a-105">O `GetState` método recupera o estado do filtro (em execução, parado ou pausado).</span><span class="sxs-lookup"><span data-stu-id="9e05a-105">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span> <span data-ttu-id="9e05a-106">Esse método implementa o método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .</span><span class="sxs-lookup"><span data-stu-id="9e05a-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e05a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e05a-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="9e05a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e05a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e05a-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="9e05a-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="9e05a-110">Intervalo de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="9e05a-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="9e05a-111">*State*</span><span class="sxs-lookup"><span data-stu-id="9e05a-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="9e05a-112">Ponteiro para uma variável que recebe um membro do tipo enumerado de [**\_ estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , indicando o estado do filtro.</span><span class="sxs-lookup"><span data-stu-id="9e05a-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e05a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e05a-113">Return value</span></span>

<span data-ttu-id="9e05a-114">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="9e05a-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e05a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e05a-115">Remarks</span></span>

<span data-ttu-id="9e05a-116">Na classe base, todas as transições de estado são síncronas e o parâmetro *dwMilliSecsTimeout* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9e05a-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="9e05a-117">Se uma classe derivada executar transições de estado assíncronas, ela deverá substituir esse método para aguardar durante as transições de estado, com um tempo limite de milissegundos de *dwMilliSecsTimeout* .</span><span class="sxs-lookup"><span data-stu-id="9e05a-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

<span data-ttu-id="9e05a-118">Se o filtro não entregar dados enquanto estiver em pausa, substitua o `GetState` método para retornar o valor VFW \_ S \_ \_ não consegue se marcar quando o filtro está em pausa (consulte [entregando exemplos](delivering-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="9e05a-118">If your filter does not deliver data while paused, override the `GetState` method to return the value VFW\_S\_CANT\_CUE when the filter is paused (see [Delivering Samples](delivering-samples.md)).</span></span> <span data-ttu-id="9e05a-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9e05a-119">For example:</span></span>


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="9e05a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e05a-120">Requirements</span></span>



| <span data-ttu-id="9e05a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e05a-121">Requirement</span></span> | <span data-ttu-id="9e05a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9e05a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e05a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e05a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9e05a-124"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e05a-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9e05a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e05a-125">Library</span></span><br/> | <dl> <span data-ttu-id="9e05a-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9e05a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e05a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e05a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e05a-128">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="9e05a-128">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




