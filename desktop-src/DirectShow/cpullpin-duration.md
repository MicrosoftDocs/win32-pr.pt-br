---
description: O método Duration recupera a duração do fluxo.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Método CPullPin. Duration (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770082"
---
# <a name="cpullpinduration-method"></a><span data-ttu-id="4a022-103">Método CPullPin. Duration</span><span class="sxs-lookup"><span data-stu-id="4a022-103">CPullPin.Duration method</span></span>

<span data-ttu-id="4a022-104">O `Duration` método recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="4a022-104">The `Duration` method retrieves the duration of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a022-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a022-105">Syntax</span></span>


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a><span data-ttu-id="4a022-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a022-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a022-107">*ptDuration*</span><span class="sxs-lookup"><span data-stu-id="4a022-107">*ptDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="4a022-108">Ponteiro para uma variável que recebe a duração, em bytes multiplicado por 10 milhões.</span><span class="sxs-lookup"><span data-stu-id="4a022-108">Pointer to a variable that receives the duration, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a022-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a022-109">Return value</span></span>

<span data-ttu-id="4a022-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4a022-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a022-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a022-111">Remarks</span></span>

<span data-ttu-id="4a022-112">A duração é indeterminada até que o método [**CPullPin:: Connect**](cpullpin-connect.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="4a022-112">The duration is indeterminate until the [**CPullPin::Connect**](cpullpin-connect.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a022-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a022-113">Requirements</span></span>



| <span data-ttu-id="4a022-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a022-114">Requirement</span></span> | <span data-ttu-id="4a022-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4a022-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a022-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a022-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4a022-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a022-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="4a022-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a022-118">Library</span></span><br/> | <dl> <span data-ttu-id="4a022-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4a022-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a022-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a022-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a022-121">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="4a022-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




