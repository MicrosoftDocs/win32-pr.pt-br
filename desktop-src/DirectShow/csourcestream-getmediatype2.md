---
description: O método GetMediaType recupera um tipo de mídia preferencial.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Método CSourceStream. GetMediaType (origem. h)-parâmetro pMediaType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8306da8451d4af7da8ce4f4c7d4d3f6fd367e1ec
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389182"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a><span data-ttu-id="d65a1-103">Método CSourceStream. GetMediaType (origem. h)</span><span class="sxs-lookup"><span data-stu-id="d65a1-103">CSourceStream.GetMediaType method (Source.h)</span></span>

<span data-ttu-id="d65a1-104">O `GetMediaType` método recupera um tipo de mídia preferencial.</span><span class="sxs-lookup"><span data-stu-id="d65a1-104">The `GetMediaType` method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d65a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d65a1-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="d65a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d65a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d65a1-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="d65a1-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="d65a1-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d65a1-108">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d65a1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d65a1-109">Return value</span></span>

<span data-ttu-id="d65a1-110">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d65a1-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d65a1-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d65a1-111">Return code</span></span>                                                                                            | <span data-ttu-id="d65a1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d65a1-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d65a1-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-113"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="d65a1-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="d65a1-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="d65a1-115"><dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-115"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="d65a1-116">Índice fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="d65a1-116">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="d65a1-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="d65a1-118">Índice menor que zero.</span><span class="sxs-lookup"><span data-stu-id="d65a1-118">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="d65a1-119"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="d65a1-120">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="d65a1-120">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="d65a1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d65a1-121">Remarks</span></span>

<span data-ttu-id="d65a1-122">Há duas versões desse método.</span><span class="sxs-lookup"><span data-stu-id="d65a1-122">There are two versions of this method.</span></span> <span data-ttu-id="d65a1-123">Uma versão substitui o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) e usa um valor de índice como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d65a1-123">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="d65a1-124">A outra versão foi projetada para recuperar um único tipo de mídia, portanto, ele não tem o parâmetro de índice.</span><span class="sxs-lookup"><span data-stu-id="d65a1-124">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="d65a1-125">O método de parâmetro único retorna E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="d65a1-125">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="d65a1-126">O método de dois parâmetros verifica se o parâmetro *iPosition* é zero e, em seguida, chama a versão de parâmetro único.</span><span class="sxs-lookup"><span data-stu-id="d65a1-126">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="d65a1-127">Dependendo do número de tipos de mídia aos quais o PIN dá suporte, você deve substituir um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="d65a1-127">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="d65a1-128">Se o PIN der suporte a exatamente um tipo de mídia, substitua a versão de parâmetro único.</span><span class="sxs-lookup"><span data-stu-id="d65a1-128">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="d65a1-129">Preencha o tipo de mídia ao qual o PIN dá suporte.</span><span class="sxs-lookup"><span data-stu-id="d65a1-129">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="d65a1-130">Se o PIN der suporte a mais de um tipo de mídia, substitua a versão de dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d65a1-130">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="d65a1-131">Substitua também o método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="d65a1-131">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d65a1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d65a1-132">Requirements</span></span>



| <span data-ttu-id="d65a1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d65a1-133">Requirement</span></span> | <span data-ttu-id="d65a1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d65a1-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d65a1-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d65a1-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d65a1-136"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-136"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d65a1-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d65a1-137">Library</span></span><br/> | <dl> <span data-ttu-id="d65a1-138"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d65a1-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d65a1-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d65a1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d65a1-140">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="d65a1-140">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




