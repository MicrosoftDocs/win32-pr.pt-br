---
description: 'O método GetState recupera o estado do objeto (em execução, parado ou pausado). Esse método implementa o método IMediaFilter:: GetState.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Método CBaseMediaFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771868"
---
# <a name="cbasemediafiltergetstate-method"></a><span data-ttu-id="fec83-104">Método CBaseMediaFilter. GetState</span><span class="sxs-lookup"><span data-stu-id="fec83-104">CBaseMediaFilter.GetState method</span></span>

<span data-ttu-id="fec83-105">O `GetState` método recupera o estado do objeto (em execução, parado ou pausado).</span><span class="sxs-lookup"><span data-stu-id="fec83-105">The `GetState` method retrieves the object's state (running, stopped, or paused).</span></span> <span data-ttu-id="fec83-106">Esse método implementa o método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .</span><span class="sxs-lookup"><span data-stu-id="fec83-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec83-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fec83-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="fec83-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fec83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec83-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="fec83-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="fec83-110">Intervalo de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="fec83-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="fec83-111">*State*</span><span class="sxs-lookup"><span data-stu-id="fec83-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="fec83-112">Ponteiro para uma variável que recebe um membro do tipo enumerado de [**\_ estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , indicando o estado do objeto.</span><span class="sxs-lookup"><span data-stu-id="fec83-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the object's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec83-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fec83-113">Return value</span></span>

<span data-ttu-id="fec83-114">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="fec83-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec83-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fec83-115">Remarks</span></span>

<span data-ttu-id="fec83-116">Na classe base, todas as transições de estado são síncronas e o parâmetro *dwMilliSecsTimeout* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="fec83-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="fec83-117">Se uma classe derivada executar transições de estado assíncronas, ela deverá substituir esse método para aguardar durante as transições de estado, com um tempo limite de milissegundos de *dwMilliSecsTimeout* .</span><span class="sxs-lookup"><span data-stu-id="fec83-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec83-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec83-118">Requirements</span></span>



| <span data-ttu-id="fec83-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec83-119">Requirement</span></span> | <span data-ttu-id="fec83-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fec83-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec83-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fec83-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fec83-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fec83-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fec83-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fec83-123">Library</span></span><br/> | <dl> <span data-ttu-id="fec83-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fec83-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec83-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fec83-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec83-126">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="fec83-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




