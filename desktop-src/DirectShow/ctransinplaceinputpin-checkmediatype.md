---
description: Método CTransInPlaceInputPin. CheckMediaType – o método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Método CTransInPlaceInputPin. CheckMediaType (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5de3cec87d740db42824b0d7abf1ee4bfc6aeecb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094794"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="5ebea-103">Método CTransInPlaceInputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="5ebea-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="5ebea-104">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="5ebea-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ebea-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="5ebea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ebea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ebea-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="5ebea-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5ebea-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="5ebea-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ebea-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5ebea-109">Return value</span></span>

<span data-ttu-id="5ebea-110">Retornará S \_ OK se o tipo de mídia proposto for aceitável.</span><span class="sxs-lookup"><span data-stu-id="5ebea-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="5ebea-111">Caso contrário, retorna S \_ false ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="5ebea-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ebea-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ebea-112">Remarks</span></span>

<span data-ttu-id="5ebea-113">Esse método substitui o método [**CTransformInputPin:: CheckMediaType**](ctransforminputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="5ebea-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="5ebea-114">Ele chama o método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="5ebea-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="5ebea-115">Se o pino de saída estiver conectado, esse método também chamará o método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="5ebea-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ebea-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ebea-116">Requirements</span></span>



| <span data-ttu-id="5ebea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ebea-117">Requirement</span></span> | <span data-ttu-id="5ebea-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5ebea-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebea-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ebea-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5ebea-120"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ebea-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ebea-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ebea-121">Library</span></span><br/> | <dl> <span data-ttu-id="5ebea-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5ebea-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ebea-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5ebea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebea-124">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="5ebea-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




