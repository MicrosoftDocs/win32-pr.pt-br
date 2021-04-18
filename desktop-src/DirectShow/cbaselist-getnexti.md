---
description: O método getpróximoi recupera o item na posição especificada e avança a posição.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Método CBaseList. GetNextI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758872"
---
# <a name="cbaselistgetnexti-method"></a><span data-ttu-id="3b687-103">Método CBaseList. getavançari</span><span class="sxs-lookup"><span data-stu-id="3b687-103">CBaseList.GetNextI method</span></span>

<span data-ttu-id="3b687-104">O `GetNextI` método recupera o item na posição especificada e avança a posição.</span><span class="sxs-lookup"><span data-stu-id="3b687-104">The `GetNextI` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b687-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b687-105">Syntax</span></span>


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="3b687-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b687-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b687-107">*RP* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="3b687-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3b687-108">Referência a um valor de posição.</span><span class="sxs-lookup"><span data-stu-id="3b687-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b687-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b687-109">Return value</span></span>

<span data-ttu-id="3b687-110">Retorna um ponteiro para o item.</span><span class="sxs-lookup"><span data-stu-id="3b687-110">Returns a pointer to the item.</span></span> <span data-ttu-id="3b687-111">Se o *RP* for **nulo**, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3b687-111">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b687-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b687-112">Remarks</span></span>

<span data-ttu-id="3b687-113">Esse método avança o indicador de posição para a próxima posição.</span><span class="sxs-lookup"><span data-stu-id="3b687-113">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="3b687-114">Se o indicador de posição passar do final da lista, o método o definirá como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3b687-114">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b687-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b687-115">Requirements</span></span>



| <span data-ttu-id="3b687-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b687-116">Requirement</span></span> | <span data-ttu-id="3b687-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3b687-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b687-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b687-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3b687-119"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b687-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3b687-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b687-120">Library</span></span><br/> | <dl> <span data-ttu-id="3b687-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3b687-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b687-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b687-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b687-123">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="3b687-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




