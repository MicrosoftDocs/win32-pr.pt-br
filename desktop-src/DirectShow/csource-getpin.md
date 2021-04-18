---
description: 'O método GetPin recupera um PIN. Esse método implementa o método puramente virtual CBaseFilter:: GetPin.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Método CSource. GetPin (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757019"
---
# <a name="csourcegetpin-method"></a><span data-ttu-id="f62d0-104">Método CSource. GetPin</span><span class="sxs-lookup"><span data-stu-id="f62d0-104">CSource.GetPin method</span></span>

<span data-ttu-id="f62d0-105">O `GetPin` método recupera um PIN.</span><span class="sxs-lookup"><span data-stu-id="f62d0-105">The `GetPin` method retrieves a pin.</span></span> <span data-ttu-id="f62d0-106">Esse método implementa o método puramente virtual [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="f62d0-106">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f62d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f62d0-107">Syntax</span></span>


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="f62d0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f62d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f62d0-109">*n*</span><span class="sxs-lookup"><span data-stu-id="f62d0-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="f62d0-110">Número do PIN especificado.</span><span class="sxs-lookup"><span data-stu-id="f62d0-110">Number of the specified pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f62d0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f62d0-111">Return value</span></span>

<span data-ttu-id="f62d0-112">Retorna o ponteiro para o objeto [**CBasePin**](cbasepin.md) que implementa o PIN ou **NULL** se o índice estiver fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="f62d0-112">Returns the pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the index is out of range.</span></span>

## <a name="requirements"></a><span data-ttu-id="f62d0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f62d0-113">Requirements</span></span>



| <span data-ttu-id="f62d0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f62d0-114">Requirement</span></span> | <span data-ttu-id="f62d0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f62d0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f62d0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f62d0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f62d0-117"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f62d0-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f62d0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f62d0-118">Library</span></span><br/> | <dl> <span data-ttu-id="f62d0-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f62d0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f62d0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f62d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f62d0-121">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="f62d0-121">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




