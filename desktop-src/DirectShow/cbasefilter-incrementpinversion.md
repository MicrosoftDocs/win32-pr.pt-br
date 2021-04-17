---
description: O método IncremementPinVersion incrementa o número de versão no conjunto de Pins.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Método CBaseFilter. IncrementPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749265"
---
# <a name="cbasefilterincrementpinversion-method"></a><span data-ttu-id="dee54-103">Método CBaseFilter. IncrementPinVersion</span><span class="sxs-lookup"><span data-stu-id="dee54-103">CBaseFilter.IncrementPinVersion method</span></span>

<span data-ttu-id="dee54-104">O `IncremementPinVersion` método incrementa o número de versão no conjunto de Pins.</span><span class="sxs-lookup"><span data-stu-id="dee54-104">The `IncremementPinVersion` method increments the version number on the set of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dee54-105">Syntax</span></span>


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="dee54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dee54-106">Parameters</span></span>

<span data-ttu-id="dee54-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dee54-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dee54-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dee54-108">Return value</span></span>

<span data-ttu-id="dee54-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dee54-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dee54-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dee54-110">Remarks</span></span>

<span data-ttu-id="dee54-111">Esse método incrementa a variável de membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="dee54-111">This method increments the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span> <span data-ttu-id="dee54-112">Se o filtro cria ou destrói Pins dinamicamente, chame esse método sempre que os Pins forem alterados.</span><span class="sxs-lookup"><span data-stu-id="dee54-112">If the filter dynamically creates or destroys pins, call this method whenever the pins change.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee54-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dee54-113">Requirements</span></span>



| <span data-ttu-id="dee54-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee54-114">Requirement</span></span> | <span data-ttu-id="dee54-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dee54-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee54-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dee54-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dee54-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dee54-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dee54-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dee54-118">Library</span></span><br/> | <dl> <span data-ttu-id="dee54-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dee54-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee54-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="dee54-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee54-121">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="dee54-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="dee54-122">**CBaseFilter::GetPinVersion**</span><span class="sxs-lookup"><span data-stu-id="dee54-122">**CBaseFilter::GetPinVersion**</span></span>](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




