---
description: Método CBasePin. GetMediaType – o método GetMediaType recupera um tipo de mídia preferencial, por valor de índice.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Método CBasePin. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099364"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="1ee8a-103">Método CBasePin. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="1ee8a-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="1ee8a-104">O `GetMediaType` método recupera um tipo de mídia preferencial, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ee8a-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="1ee8a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ee8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee8a-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="1ee8a-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee8a-108">Valor de índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="1ee8a-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="1ee8a-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee8a-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee8a-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1ee8a-111">Return value</span></span>

<span data-ttu-id="1ee8a-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ee8a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1ee8a-113">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="1ee8a-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1ee8a-114">Return code</span></span>                                                                                            | <span data-ttu-id="1ee8a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ee8a-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1ee8a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8a-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="1ee8a-117">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="1ee8a-118"><dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8a-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="1ee8a-119">Índice fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="1ee8a-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8a-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="1ee8a-121">Índice menor que zero.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="1ee8a-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8a-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="1ee8a-123">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="1ee8a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ee8a-124">Remarks</span></span>

<span data-ttu-id="1ee8a-125">A partir da lista de tipos de mídia preferenciais do PIN, esse método retorna o tipo com um valor de índice de *iPosition*.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="1ee8a-126">A classe [**CEnumMediaTypes**](cenummediatypes.md) chama esse método para enumerar os tipos de mídia preferenciais.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="1ee8a-127">A classe base retorna E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="1ee8a-128">Substitua esse método em sua classe derivada.</span><span class="sxs-lookup"><span data-stu-id="1ee8a-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee8a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ee8a-129">Requirements</span></span>



| <span data-ttu-id="1ee8a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee8a-130">Requirement</span></span> | <span data-ttu-id="1ee8a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1ee8a-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee8a-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ee8a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="1ee8a-133"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8a-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1ee8a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ee8a-134">Library</span></span><br/> | <dl> <span data-ttu-id="1ee8a-135"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee8a-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee8a-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1ee8a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee8a-137">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="1ee8a-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




