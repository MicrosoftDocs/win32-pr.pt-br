---
description: O método AddHead adiciona um item à frente da lista.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Método CGenericList. AddHead (Wxlist. h)-pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104012194"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a><span data-ttu-id="c708a-103">Método CGenericList. AddHead (Wxlist. h)-pObj</span><span class="sxs-lookup"><span data-stu-id="c708a-103">CGenericList.AddHead method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="c708a-104">O `AddHead` método adiciona um item à frente da lista.</span><span class="sxs-lookup"><span data-stu-id="c708a-104">The `AddHead` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c708a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c708a-105">Syntax</span></span>


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="c708a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c708a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c708a-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="c708a-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="c708a-108">Ponteiro para um objeto do tipo **Object** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="c708a-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c708a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c708a-109">Return value</span></span>

<span data-ttu-id="c708a-110">Retorna um valor de posição que indica a nova posição de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c708a-110">Returns a POSITION value indicating the new head position.</span></span> <span data-ttu-id="c708a-111">Se o método falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c708a-111">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c708a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c708a-112">Requirements</span></span>

| <span data-ttu-id="c708a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c708a-113">Requirement</span></span> | <span data-ttu-id="c708a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c708a-114">Value</span></span> |
|-|-|
| <span data-ttu-id="c708a-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c708a-115">Header</span></span> | <span data-ttu-id="c708a-116">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="c708a-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="c708a-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c708a-117">Library</span></span>| <span data-ttu-id="c708a-118">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="c708a-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c708a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c708a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c708a-120">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="c708a-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




