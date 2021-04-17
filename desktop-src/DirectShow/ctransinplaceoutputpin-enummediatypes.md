---
description: 'O método EnumMediaTypes enumera os tipos de mídia preferenciais do PIN. Esse método implementa o método IPin:: EnumMediaTypes.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Método CTransInPlaceOutputPin. EnumMediaTypes (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d214004412264272c64d0efaf20a5da7e1ca3cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783395"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a><span data-ttu-id="65d8c-104">Método CTransInPlaceOutputPin. EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="65d8c-104">CTransInPlaceOutputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="65d8c-105">O `EnumMediaTypes` método enumera os tipos de mídia preferenciais do PIN.</span><span class="sxs-lookup"><span data-stu-id="65d8c-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="65d8c-106">Esse método implementa o método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="65d8c-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d8c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65d8c-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="65d8c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65d8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d8c-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="65d8c-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="65d8c-110">Recebe um ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="65d8c-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d8c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65d8c-111">Return value</span></span>

<span data-ttu-id="65d8c-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65d8c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="65d8c-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="65d8c-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="65d8c-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="65d8c-114">Return code</span></span>                                                                                           | <span data-ttu-id="65d8c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="65d8c-115">Description</span></span>                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="65d8c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="65d8c-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="65d8c-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="65d8c-117">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="65d8c-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="65d8c-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="65d8c-119">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="65d8c-119">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="65d8c-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="65d8c-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="65d8c-121">Ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="65d8c-121">**NULL** pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="65d8c-122"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="65d8c-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="65d8c-123">O pino de entrada do filtro não está conectado.</span><span class="sxs-lookup"><span data-stu-id="65d8c-123">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65d8c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="65d8c-124">Remarks</span></span>

<span data-ttu-id="65d8c-125">Esse método retorna a interface **IEnumMediaTypes** do pino de saída upstream.</span><span class="sxs-lookup"><span data-stu-id="65d8c-125">This method returns the **IEnumMediaTypes** interface from the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d8c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d8c-126">Requirements</span></span>



| <span data-ttu-id="65d8c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d8c-127">Requirement</span></span> | <span data-ttu-id="65d8c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="65d8c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d8c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65d8c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="65d8c-130"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65d8c-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65d8c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65d8c-131">Library</span></span><br/> | <dl> <span data-ttu-id="65d8c-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="65d8c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d8c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="65d8c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d8c-134">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="65d8c-134">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




