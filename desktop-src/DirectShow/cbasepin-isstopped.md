---
description: O método IsStopped determina se o filtro que contém esse PIN é interrompido.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Método CBasePin. IsStopped (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751505"
---
# <a name="cbasepinisstopped-method"></a><span data-ttu-id="47819-103">Método CBasePin. IsStopped</span><span class="sxs-lookup"><span data-stu-id="47819-103">CBasePin.IsStopped method</span></span>

<span data-ttu-id="47819-104">O `IsStopped` método determina se o filtro que contém este pin é interrompido.</span><span class="sxs-lookup"><span data-stu-id="47819-104">The `IsStopped` method determines whether the filter containing this pin is stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="47819-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47819-105">Syntax</span></span>


```C++
BOOL IsStopped();
```



## <a name="parameters"></a><span data-ttu-id="47819-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47819-106">Parameters</span></span>

<span data-ttu-id="47819-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="47819-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47819-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47819-108">Return value</span></span>

<span data-ttu-id="47819-109">Retornará **true** se o filtro for interrompido.</span><span class="sxs-lookup"><span data-stu-id="47819-109">Returns **TRUE** if the filter is stopped.</span></span> <span data-ttu-id="47819-110">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="47819-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="47819-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="47819-111">Remarks</span></span>

<span data-ttu-id="47819-112">Não chame esse método de dentro do método do construtor **CBasePin** , pois o filtro pode ainda não ter sido inicializado.</span><span class="sxs-lookup"><span data-stu-id="47819-112">Do not call this method from within in the **CBasePin** constructor method, because the filter might not be initialized yet.</span></span>

## <a name="requirements"></a><span data-ttu-id="47819-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47819-113">Requirements</span></span>



| <span data-ttu-id="47819-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="47819-114">Requirement</span></span> | <span data-ttu-id="47819-115">Valor</span><span class="sxs-lookup"><span data-stu-id="47819-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47819-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47819-116">Header</span></span><br/>  | <dl> <span data-ttu-id="47819-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47819-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="47819-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47819-118">Library</span></span><br/> | <dl> <span data-ttu-id="47819-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="47819-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47819-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="47819-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47819-121">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="47819-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




