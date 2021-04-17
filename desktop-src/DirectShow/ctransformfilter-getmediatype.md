---
description: O método GetMediaType recupera um tipo de mídia preferencial para o pino de saída.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Método CTransformFilter. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752688"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="03dcb-103">Método CTransformFilter. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="03dcb-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="03dcb-104">O `GetMediaType` método recupera um tipo de mídia preferencial para o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="03dcb-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="03dcb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03dcb-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="03dcb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03dcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03dcb-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="03dcb-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="03dcb-108">Valor de índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="03dcb-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="03dcb-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="03dcb-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="03dcb-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="03dcb-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03dcb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03dcb-111">Return value</span></span>

<span data-ttu-id="03dcb-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03dcb-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="03dcb-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="03dcb-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="03dcb-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="03dcb-114">Return code</span></span>                                                                                            | <span data-ttu-id="03dcb-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="03dcb-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="03dcb-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="03dcb-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="03dcb-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="03dcb-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="03dcb-118"><dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt></span><span class="sxs-lookup"><span data-stu-id="03dcb-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="03dcb-119">Índice fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="03dcb-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="03dcb-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="03dcb-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="03dcb-121">Índice menor que zero.</span><span class="sxs-lookup"><span data-stu-id="03dcb-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="03dcb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="03dcb-122">Remarks</span></span>

<span data-ttu-id="03dcb-123">O método [**CTransformOutputPin:: GetMediaType**](ctransformoutputpin-getmediatype.md) do pino de saída chama esse método.</span><span class="sxs-lookup"><span data-stu-id="03dcb-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="03dcb-124">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="03dcb-124">The derived class must implement this method.</span></span> <span data-ttu-id="03dcb-125">Para obter mais informações, consulte [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="03dcb-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03dcb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03dcb-126">Requirements</span></span>



| <span data-ttu-id="03dcb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="03dcb-127">Requirement</span></span> | <span data-ttu-id="03dcb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="03dcb-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03dcb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03dcb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="03dcb-130"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03dcb-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="03dcb-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03dcb-131">Library</span></span><br/> | <dl> <span data-ttu-id="03dcb-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="03dcb-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03dcb-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="03dcb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03dcb-134">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="03dcb-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




