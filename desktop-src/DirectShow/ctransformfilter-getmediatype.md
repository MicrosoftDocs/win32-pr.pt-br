---
description: Método CTransformFilter. GetMediaType – o método GetMediaType recupera um tipo de mídia preferencial para o pino de saída.
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
ms.openlocfilehash: 6415b8e3d8ae4e292b7e2592b123120927081ea8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095114"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="8a7a0-103">Método CTransformFilter. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="8a7a0-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="8a7a0-104">O `GetMediaType` método recupera um tipo de mídia preferencial para o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a7a0-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8a7a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a7a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a7a0-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="8a7a0-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="8a7a0-108">Valor de índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="8a7a0-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="8a7a0-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="8a7a0-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a7a0-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8a7a0-111">Return value</span></span>

<span data-ttu-id="8a7a0-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a7a0-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8a7a0-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8a7a0-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8a7a0-114">Return code</span></span>                                                                                            | <span data-ttu-id="8a7a0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a7a0-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8a7a0-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7a0-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="8a7a0-117">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="8a7a0-118"><dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7a0-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="8a7a0-119">Índice fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="8a7a0-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8a7a0-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="8a7a0-121">Índice menor que zero.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a7a0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a7a0-122">Remarks</span></span>

<span data-ttu-id="8a7a0-123">O método [**CTransformOutputPin:: GetMediaType**](ctransformoutputpin-getmediatype.md) do pino de saída chama esse método.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="8a7a0-124">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-124">The derived class must implement this method.</span></span> <span data-ttu-id="8a7a0-125">Para obter mais informações, consulte [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="8a7a0-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a7a0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a7a0-126">Requirements</span></span>



| <span data-ttu-id="8a7a0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a7a0-127">Requirement</span></span> | <span data-ttu-id="8a7a0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8a7a0-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7a0-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a7a0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8a7a0-130"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a7a0-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8a7a0-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a7a0-131">Library</span></span><br/> | <dl> <span data-ttu-id="8a7a0-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8a7a0-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a7a0-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8a7a0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7a0-134">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




