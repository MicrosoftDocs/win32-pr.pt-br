---
description: Método CBaseRenderer. GetPin – o método GetPin recupera um PIN.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Método CBaseRenderer. GetPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119884"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="ce92d-103">Método CBaseRenderer. GetPin</span><span class="sxs-lookup"><span data-stu-id="ce92d-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="ce92d-104">O `GetPin` método recupera um PIN.</span><span class="sxs-lookup"><span data-stu-id="ce92d-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce92d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce92d-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="ce92d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce92d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce92d-107">*n*</span><span class="sxs-lookup"><span data-stu-id="ce92d-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="ce92d-108">Número do PIN especificado.</span><span class="sxs-lookup"><span data-stu-id="ce92d-108">Number of the specified pin.</span></span> <span data-ttu-id="ce92d-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ce92d-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce92d-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ce92d-110">Return value</span></span>

<span data-ttu-id="ce92d-111">Retorna o ponteiro [**\_ pInputPin CBaseRenderer:: m**](cbaserenderer-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="ce92d-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce92d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce92d-112">Remarks</span></span>

<span data-ttu-id="ce92d-113">Esse método implementa o método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) , que é puro virtual na classe **CBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="ce92d-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="ce92d-114">O filtro dá suporte a exatamente um PIN (o PIN de entrada).</span><span class="sxs-lookup"><span data-stu-id="ce92d-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="ce92d-115">Na primeira vez que esse método é chamado, ele cria o PIN como um novo objeto [**CRendererInputPin**](crendererinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="ce92d-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce92d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce92d-116">Requirements</span></span>



| <span data-ttu-id="ce92d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce92d-117">Requirement</span></span> | <span data-ttu-id="ce92d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ce92d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce92d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce92d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ce92d-120"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce92d-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce92d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce92d-121">Library</span></span><br/> | <dl> <span data-ttu-id="ce92d-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ce92d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce92d-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ce92d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce92d-124">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="ce92d-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




