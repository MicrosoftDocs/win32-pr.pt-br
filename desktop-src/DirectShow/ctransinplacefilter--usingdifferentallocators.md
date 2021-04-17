---
description: O método UsingDifferentAllocators determina se os Pins de entrada e de saída estão usando alocadores diferentes.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Método CTransInPlaceFilter. UsingDifferentAllocators (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752682"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a><span data-ttu-id="0388e-103">Método CTransInPlaceFilter. UsingDifferentAllocators</span><span class="sxs-lookup"><span data-stu-id="0388e-103">CTransInPlaceFilter.UsingDifferentAllocators method</span></span>

<span data-ttu-id="0388e-104">O `UsingDifferentAllocators` método determina se os Pins de entrada e de saída estão usando alocadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="0388e-104">The `UsingDifferentAllocators` method determines whether the input and output pins are using different allocators.</span></span>

## <a name="syntax"></a><span data-ttu-id="0388e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0388e-105">Syntax</span></span>


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a><span data-ttu-id="0388e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0388e-106">Parameters</span></span>

<span data-ttu-id="0388e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0388e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0388e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0388e-108">Return value</span></span>

<span data-ttu-id="0388e-109">Retornará **true** se os Pins de entrada e saída estiverem usando alocadores diferentes ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0388e-109">Returns **TRUE** if the input and output pins are using different allocators, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0388e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0388e-110">Requirements</span></span>



| <span data-ttu-id="0388e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0388e-111">Requirement</span></span> | <span data-ttu-id="0388e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0388e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0388e-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0388e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="0388e-114"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0388e-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0388e-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0388e-115">Library</span></span><br/> | <dl> <span data-ttu-id="0388e-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0388e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0388e-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="0388e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0388e-118">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="0388e-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




