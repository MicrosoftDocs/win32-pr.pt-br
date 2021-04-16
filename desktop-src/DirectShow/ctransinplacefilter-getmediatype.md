---
description: O método GetMediaType recupera um tipo de mídia preferencial para o pino de saída.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Método CTransInPlaceFilter. GetMediaType (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2347e0466a7df848e0f0b2bccec325eedfefc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775566"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="9adbb-103">Método CTransInPlaceFilter. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="9adbb-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="9adbb-104">O `GetMediaType` método recupera um tipo de mídia preferencial para o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="9adbb-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9adbb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9adbb-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="9adbb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9adbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9adbb-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="9adbb-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="9adbb-108">Valor de índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="9adbb-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="9adbb-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="9adbb-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="9adbb-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9adbb-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9adbb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9adbb-111">Return value</span></span>

<span data-ttu-id="9adbb-112">Retorna E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="9adbb-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="9adbb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9adbb-113">Remarks</span></span>

<span data-ttu-id="9adbb-114">Esse método substitui o método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="9adbb-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="9adbb-115">Na classe **CTransInPlaceFilter** , cada pino chama o PIN conectado oposto para enumerar os tipos de mídia preferenciais.</span><span class="sxs-lookup"><span data-stu-id="9adbb-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="9adbb-116">O pino de entrada chama o pino de entrada do filtro downstream e o pino de saída chama o pino de saída do filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="9adbb-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="9adbb-117">Portanto, o método do filtro `GetMediaType` nunca é chamado.</span><span class="sxs-lookup"><span data-stu-id="9adbb-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="9adbb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9adbb-118">Requirements</span></span>



| <span data-ttu-id="9adbb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9adbb-119">Requirement</span></span> | <span data-ttu-id="9adbb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9adbb-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9adbb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9adbb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9adbb-122"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9adbb-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9adbb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9adbb-123">Library</span></span><br/> | <dl> <span data-ttu-id="9adbb-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9adbb-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9adbb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9adbb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9adbb-126">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="9adbb-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




