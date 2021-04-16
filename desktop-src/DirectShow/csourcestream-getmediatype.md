---
description: O método GetMediaType recupera um tipo de mídia preferencial. Esse método usa os parâmetros *iPosition* e *pMediaType* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Método CSourceStream. GetMediaType (origem. h)-parâmetros iPosition e pMediaType
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187939"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a><span data-ttu-id="caa52-104">Método CSourceStream. GetMediaType (origem. h)-parâmetros iPosition e pMediaType</span><span class="sxs-lookup"><span data-stu-id="caa52-104">CSourceStream.GetMediaType method (Source.h) - iPosition and pMediaType parameters</span></span>

<span data-ttu-id="caa52-105">O método **GetMediaType** recupera um tipo de mídia preferencial.</span><span class="sxs-lookup"><span data-stu-id="caa52-105">The **GetMediaType** method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="caa52-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="caa52-106">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="caa52-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="caa52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caa52-108">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="caa52-108">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="caa52-109">Valor de índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="caa52-109">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="caa52-110">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="caa52-110">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="caa52-111">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="caa52-111">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caa52-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="caa52-112">Return value</span></span>

<span data-ttu-id="caa52-113">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="caa52-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="caa52-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="caa52-114">Return code</span></span>                                                                                            | <span data-ttu-id="caa52-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="caa52-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="caa52-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="caa52-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="caa52-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="caa52-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="caa52-118"><dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt></span><span class="sxs-lookup"><span data-stu-id="caa52-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="caa52-119">Índice fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="caa52-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="caa52-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="caa52-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="caa52-121">Índice menor que zero.</span><span class="sxs-lookup"><span data-stu-id="caa52-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="caa52-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="caa52-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="caa52-123">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="caa52-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="caa52-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="caa52-124">Remarks</span></span>

<span data-ttu-id="caa52-125">Há duas versões desse método.</span><span class="sxs-lookup"><span data-stu-id="caa52-125">There are two versions of this method.</span></span> <span data-ttu-id="caa52-126">Uma versão substitui o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) e usa um valor de índice como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="caa52-126">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="caa52-127">A outra versão foi projetada para recuperar um único tipo de mídia, portanto, ele não tem o parâmetro de índice.</span><span class="sxs-lookup"><span data-stu-id="caa52-127">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="caa52-128">O método de parâmetro único retorna E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="caa52-128">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="caa52-129">O método de dois parâmetros verifica se o parâmetro *iPosition* é zero e, em seguida, chama a versão de parâmetro único.</span><span class="sxs-lookup"><span data-stu-id="caa52-129">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="caa52-130">Dependendo do número de tipos de mídia aos quais o PIN dá suporte, você deve substituir um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="caa52-130">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="caa52-131">Se o PIN der suporte a exatamente um tipo de mídia, substitua a versão de parâmetro único.</span><span class="sxs-lookup"><span data-stu-id="caa52-131">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="caa52-132">Preencha o tipo de mídia ao qual o PIN dá suporte.</span><span class="sxs-lookup"><span data-stu-id="caa52-132">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="caa52-133">Se o PIN der suporte a mais de um tipo de mídia, substitua a versão de dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="caa52-133">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="caa52-134">Substitua também o método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="caa52-134">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="caa52-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caa52-135">Requirements</span></span>



| <span data-ttu-id="caa52-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="caa52-136">Requirement</span></span> | <span data-ttu-id="caa52-137">Valor</span><span class="sxs-lookup"><span data-stu-id="caa52-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caa52-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="caa52-138">Header</span></span>  | <span data-ttu-id="caa52-139">Source. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="caa52-139">Source.h (include Streams.h)</span></span>                                                                                    |
| <span data-ttu-id="caa52-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="caa52-140">Library</span></span> | <span data-ttu-id="caa52-141">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="caa52-141">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="caa52-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="caa52-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caa52-143">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="caa52-143">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




