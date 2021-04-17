---
description: O método CRendererInputPin é um método de construtor.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Construtor CRendererInputPin. CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757021"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a><span data-ttu-id="61881-103">Construtor CRendererInputPin. CRendererInputPin</span><span class="sxs-lookup"><span data-stu-id="61881-103">CRendererInputPin.CRendererInputPin constructor</span></span>

<span data-ttu-id="61881-104">O `CRendererInputPin` método é um método de construtor.</span><span class="sxs-lookup"><span data-stu-id="61881-104">The `CRendererInputPin` method is a constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61881-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61881-105">Syntax</span></span>


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a><span data-ttu-id="61881-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61881-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61881-107">*pRenderer*</span><span class="sxs-lookup"><span data-stu-id="61881-107">*pRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="61881-108">Ponteiro para o objeto [**CBaseRenderer**](cbaserenderer.md) que implementa o filtro.</span><span class="sxs-lookup"><span data-stu-id="61881-108">Pointer to the [**CBaseRenderer**](cbaserenderer.md) object that implements the filter.</span></span>

</dd> <dt>

<span data-ttu-id="61881-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="61881-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="61881-110">Ponteiro para uma variável que recebe um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61881-110">Pointer to a variable that receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="61881-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="61881-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="61881-112">Ponteiro para uma cadeia de caracteres largos contendo o identificador de PIN.</span><span class="sxs-lookup"><span data-stu-id="61881-112">Pointer to a wide-character string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61881-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61881-113">Requirements</span></span>



| <span data-ttu-id="61881-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61881-114">Requirement</span></span> | <span data-ttu-id="61881-115">Valor</span><span class="sxs-lookup"><span data-stu-id="61881-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61881-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61881-116">Header</span></span><br/>  | <dl> <span data-ttu-id="61881-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61881-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61881-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61881-118">Library</span></span><br/> | <dl> <span data-ttu-id="61881-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="61881-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61881-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="61881-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61881-121">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="61881-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




