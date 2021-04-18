---
description: 'O método CheckMediaType determina se o PIN aceita um tipo de mídia específico. Esse método substitui o método CBasePin:: CheckMediaType.'
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Método CRendererInputPin. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749831"
---
# <a name="crendererinputpincheckmediatype-method"></a><span data-ttu-id="03fd5-104">Método CRendererInputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="03fd5-104">CRendererInputPin.CheckMediaType method</span></span>

<span data-ttu-id="03fd5-105">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="03fd5-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="03fd5-106">Esse método substitui o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="03fd5-106">This method overrides the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="03fd5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03fd5-107">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="03fd5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03fd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03fd5-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="03fd5-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="03fd5-110">Ponteiro para um objeto de tipo de mídia que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="03fd5-110">Pointer to a media type object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03fd5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03fd5-111">Return value</span></span>

<span data-ttu-id="03fd5-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03fd5-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03fd5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03fd5-113">Requirements</span></span>



| <span data-ttu-id="03fd5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="03fd5-114">Requirement</span></span> | <span data-ttu-id="03fd5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="03fd5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03fd5-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03fd5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="03fd5-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03fd5-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03fd5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03fd5-118">Library</span></span><br/> | <dl> <span data-ttu-id="03fd5-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="03fd5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03fd5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="03fd5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03fd5-121">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="03fd5-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




