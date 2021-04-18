---
description: 'O método EnumPins enumera os Pins neste filtro. Esse método implementa o método IBaseFilter:: EnumPins.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Método CBaseFilter. EnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749853"
---
# <a name="cbasefilterenumpins-method"></a><span data-ttu-id="5b48f-104">Método CBaseFilter. EnumPins</span><span class="sxs-lookup"><span data-stu-id="5b48f-104">CBaseFilter.EnumPins method</span></span>

<span data-ttu-id="5b48f-105">O `EnumPins` método enumera os Pins neste filtro.</span><span class="sxs-lookup"><span data-stu-id="5b48f-105">The `EnumPins` method enumerates the pins on this filter.</span></span> <span data-ttu-id="5b48f-106">Esse método implementa o método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) .</span><span class="sxs-lookup"><span data-stu-id="5b48f-106">This method implements the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b48f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b48f-107">Syntax</span></span>


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5b48f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b48f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b48f-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="5b48f-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="5b48f-110">Endereço de uma variável que recebe um ponteiro para a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="5b48f-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b48f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b48f-111">Return value</span></span>

<span data-ttu-id="5b48f-112">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b48f-112">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="5b48f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5b48f-113">Return code</span></span>                                                                                   | <span data-ttu-id="5b48f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b48f-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="5b48f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5b48f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5b48f-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="5b48f-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="5b48f-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5b48f-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5b48f-118">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="5b48f-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="5b48f-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5b48f-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5b48f-120">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="5b48f-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b48f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b48f-121">Remarks</span></span>

<span data-ttu-id="5b48f-122">Esse método cria uma instância da classe base [**CEnumPins**](cenumpins.md) e retorna um ponteiro para esse objeto, do tipo **IEnumPins**.</span><span class="sxs-lookup"><span data-stu-id="5b48f-122">This method creates an instance of the [**CEnumPins**](cenumpins.md) base class, and returns a pointer to that object, of type **IEnumPins**.</span></span> <span data-ttu-id="5b48f-123">A classe **CEnumPins** chama o método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) do filtro para enumerar os Pins no filtro.</span><span class="sxs-lookup"><span data-stu-id="5b48f-123">The **CEnumPins** class calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to enumerate the pins on the filter.</span></span>

<span data-ttu-id="5b48f-124">Se esse método tiver sucesso, a interface **IEnumPins** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="5b48f-124">If this method succeeds, the **IEnumPins** interface has an outstanding reference count.</span></span> <span data-ttu-id="5b48f-125">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="5b48f-125">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b48f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b48f-126">Requirements</span></span>



| <span data-ttu-id="5b48f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b48f-127">Requirement</span></span> | <span data-ttu-id="5b48f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5b48f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b48f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b48f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5b48f-130"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b48f-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5b48f-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b48f-131">Library</span></span><br/> | <dl> <span data-ttu-id="5b48f-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5b48f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b48f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b48f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b48f-134">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="5b48f-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




