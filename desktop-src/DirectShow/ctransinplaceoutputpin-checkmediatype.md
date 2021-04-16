---
description: O método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Método CTransInPlaceOutputPin. CheckMediaType (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0a422851bc7e09075076decc39d57b85d1052ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757632"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="d3586-103">Método CTransInPlaceOutputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="d3586-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="d3586-104">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="d3586-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3586-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3586-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d3586-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3586-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3586-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="d3586-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d3586-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="d3586-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3586-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3586-109">Return value</span></span>

<span data-ttu-id="d3586-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3586-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d3586-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3586-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d3586-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d3586-112">Return code</span></span>                                                                                                | <span data-ttu-id="d3586-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3586-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="d3586-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d3586-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="d3586-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="d3586-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="d3586-116"><dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt></span><span class="sxs-lookup"><span data-stu-id="d3586-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="d3586-117">Tipo de mídia não aceito.</span><span class="sxs-lookup"><span data-stu-id="d3586-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3586-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3586-118">Remarks</span></span>

<span data-ttu-id="d3586-119">Esse método substitui o método [**CTransformOutputPin:: CheckMediaType**](ctransformoutputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="d3586-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="d3586-120">Se o filtro já estiver sendo transmitido e estiver usando dois alocadores, esse método rejeitará qualquer alteração de formato.</span><span class="sxs-lookup"><span data-stu-id="d3586-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="d3586-121">Caso contrário, esse método chama o método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d3586-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="d3586-122">Se o pino de entrada estiver conectado, ele também chamará o método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de saída upstream.</span><span class="sxs-lookup"><span data-stu-id="d3586-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3586-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3586-123">Requirements</span></span>



| <span data-ttu-id="d3586-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3586-124">Requirement</span></span> | <span data-ttu-id="d3586-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d3586-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3586-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3586-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d3586-127"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3586-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3586-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3586-128">Library</span></span><br/> | <dl> <span data-ttu-id="d3586-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d3586-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3586-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3586-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3586-131">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="d3586-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




