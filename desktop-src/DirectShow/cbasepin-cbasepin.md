---
description: Construtor de CBasePin. CBasePin-método de construtor.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Construtor CBasePin. CBasePin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11dea6bd5bc3f766e5f93a04022dab5ba6e51a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099424"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="e2d66-103">Construtor CBasePin. CBasePin</span><span class="sxs-lookup"><span data-stu-id="e2d66-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="e2d66-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="e2d66-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2d66-105">Syntax</span></span>


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="e2d66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d66-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="e2d66-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d66-108">Cadeia de caracteres que contém o nome de depuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2d66-108">String containing the debug name for the object.</span></span> <span data-ttu-id="e2d66-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="e2d66-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2d66-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="e2d66-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d66-111">Ponteiro para o filtro que criou este pin.</span><span class="sxs-lookup"><span data-stu-id="e2d66-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="e2d66-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="e2d66-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d66-113">Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="e2d66-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="e2d66-114">Pode ser a mesma seção crítica que o bloqueio de filtro, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="e2d66-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2d66-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="e2d66-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d66-116">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="e2d66-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="e2d66-117">Inicialize o valor para S \_ OK antes de criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="e2d66-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="e2d66-118">O valor será alterado somente se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="e2d66-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="e2d66-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="e2d66-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d66-120">Cadeia de caracteres largos contendo o nome do PIN.</span><span class="sxs-lookup"><span data-stu-id="e2d66-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="e2d66-121">Para obter mais informações, consulte [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="e2d66-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2d66-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="e2d66-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d66-123">Membro da enumeração [**de \_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando a direção do PIN.</span><span class="sxs-lookup"><span data-stu-id="e2d66-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2d66-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2d66-124">Remarks</span></span>

<span data-ttu-id="e2d66-125">A seção crítica especificada por *pLock* serializa o estado do PIN, incluindo seu status de conexão, a escolha do alocador, o tipo de mídia e o status das operações de liberação.</span><span class="sxs-lookup"><span data-stu-id="e2d66-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="e2d66-126">Não use essa seção crítica para serializar operações de streaming.</span><span class="sxs-lookup"><span data-stu-id="e2d66-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="e2d66-127">Para obter mais informações, consulte [fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="e2d66-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="e2d66-128">Um filtro pode criar Pins em seu método construtor, portanto, neste ponto, o ponteiro *pFilter* pode não se referir a um objeto válido.</span><span class="sxs-lookup"><span data-stu-id="e2d66-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="e2d66-129">Armazene o ponteiro, mas não o referencie enquanto estiver dentro do construtor do PIN.</span><span class="sxs-lookup"><span data-stu-id="e2d66-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d66-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d66-130">Requirements</span></span>



| <span data-ttu-id="e2d66-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d66-131">Requirement</span></span> | <span data-ttu-id="e2d66-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e2d66-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d66-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2d66-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e2d66-134"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2d66-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2d66-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2d66-135">Library</span></span><br/> | <dl> <span data-ttu-id="e2d66-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e2d66-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2d66-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e2d66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d66-138">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e2d66-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




