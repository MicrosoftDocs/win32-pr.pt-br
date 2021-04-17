---
description: 'O método EnumMediaTypes enumera os tipos de mídia preferenciais do PIN. Esse método implementa o método IPin:: EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Método CBasePin. EnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54aaddbbcde26791b6c55665bfbbb7ff62048238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752713"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="c97a1-104">Método CBasePin. EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="c97a1-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="c97a1-105">O `EnumMediaTypes` método enumera os tipos de mídia preferenciais do PIN.</span><span class="sxs-lookup"><span data-stu-id="c97a1-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="c97a1-106">Esse método implementa o método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="c97a1-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c97a1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c97a1-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="c97a1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c97a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97a1-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="c97a1-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="c97a1-110">Endereço de uma variável que recebe um ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="c97a1-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97a1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c97a1-111">Return value</span></span>

<span data-ttu-id="c97a1-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c97a1-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c97a1-113">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c97a1-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="c97a1-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c97a1-114">Return code</span></span>                                                                                   | <span data-ttu-id="c97a1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c97a1-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c97a1-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c97a1-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c97a1-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c97a1-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="c97a1-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c97a1-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c97a1-119">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="c97a1-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="c97a1-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c97a1-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c97a1-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c97a1-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c97a1-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c97a1-122">Remarks</span></span>

<span data-ttu-id="c97a1-123">Os Pins de entrada não são necessários para enumerar os tipos preferenciais.</span><span class="sxs-lookup"><span data-stu-id="c97a1-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="c97a1-124">Os Pins de saída devem enumerar pelo menos um tipo preferencial.</span><span class="sxs-lookup"><span data-stu-id="c97a1-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="c97a1-125">Caso contrário, ambos os Pins podem não ter um tipo preferencial, tornando impossível uma conexão.</span><span class="sxs-lookup"><span data-stu-id="c97a1-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="c97a1-126">A interface **IEnumMediaTypes** funciona como um enumerador com padrão.</span><span class="sxs-lookup"><span data-stu-id="c97a1-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="c97a1-127">Para obter mais informações, consulte [Enumerando objetos em um grafo de filtro](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="c97a1-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="c97a1-128">Se o método tiver sucesso, a interface **IEnumMediaTypes** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="c97a1-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="c97a1-129">Certifique-se de liberá-lo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="c97a1-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="c97a1-130">A classe base [**CEnumMediaTypes**](cenummediatypes.md) implementa **IEnumMediaTypes**.</span><span class="sxs-lookup"><span data-stu-id="c97a1-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="c97a1-131">Ele chama o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) do PIN para enumerar os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="c97a1-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97a1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c97a1-132">Requirements</span></span>



| <span data-ttu-id="c97a1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c97a1-133">Requirement</span></span> | <span data-ttu-id="c97a1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c97a1-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97a1-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c97a1-135">Header</span></span><br/>  | <dl> <span data-ttu-id="c97a1-136"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c97a1-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c97a1-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c97a1-137">Library</span></span><br/> | <dl> <span data-ttu-id="c97a1-138"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c97a1-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97a1-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c97a1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97a1-140">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="c97a1-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




