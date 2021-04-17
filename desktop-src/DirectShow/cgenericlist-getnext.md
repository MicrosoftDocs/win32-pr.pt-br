---
description: O método GetNext recupera o item na posição especificada e avança a posição.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Método CGenericList. GetNext (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749249"
---
# <a name="cgenericlistgetnext-method"></a><span data-ttu-id="f8981-103">Método CGenericList. GetNext</span><span class="sxs-lookup"><span data-stu-id="f8981-103">CGenericList.GetNext method</span></span>

<span data-ttu-id="f8981-104">O `GetNext` método recupera o item na posição especificada e avança a posição.</span><span class="sxs-lookup"><span data-stu-id="f8981-104">The `GetNext` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8981-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8981-105">Syntax</span></span>


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="f8981-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8981-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8981-107">*RP* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="f8981-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f8981-108">Referência a um valor de posição.</span><span class="sxs-lookup"><span data-stu-id="f8981-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8981-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8981-109">Return value</span></span>

<span data-ttu-id="f8981-110">Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="f8981-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8981-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8981-111">Remarks</span></span>

<span data-ttu-id="f8981-112">Esse método avança o indicador de posição para a próxima posição.</span><span class="sxs-lookup"><span data-stu-id="f8981-112">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="f8981-113">Se o indicador de posição passar do final da lista, o método o definirá como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f8981-113">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

<span data-ttu-id="f8981-114">Se o *RP* for **nulo**, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f8981-114">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8981-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8981-115">Requirements</span></span>



| <span data-ttu-id="f8981-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8981-116">Requirement</span></span> | <span data-ttu-id="f8981-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f8981-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8981-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8981-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f8981-119"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8981-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f8981-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8981-120">Library</span></span><br/> | <dl> <span data-ttu-id="f8981-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f8981-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8981-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8981-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8981-123">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="f8981-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




