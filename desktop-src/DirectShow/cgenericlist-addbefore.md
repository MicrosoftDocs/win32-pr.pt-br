---
description: O método addantes insere um item antes da posição especificada. Esse método usa os parâmetros ' p ' e ' pObj '.
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Método CGenericList. AddBefore (Wxlist. h)-p, pObj parâmetros
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103930778"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="5914a-104">Método CGenericList. AddBefore (Wxlist. h)-p, pObj parâmetros</span><span class="sxs-lookup"><span data-stu-id="5914a-104">CGenericList.AddBefore method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="5914a-105">O `AddBefore` método insere um item antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="5914a-105">The `AddBefore` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="5914a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5914a-106">Syntax</span></span>


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="5914a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5914a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5914a-108">*DTI*</span><span class="sxs-lookup"><span data-stu-id="5914a-108">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="5914a-109">Posição antes da qual inserir a lista.</span><span class="sxs-lookup"><span data-stu-id="5914a-109">Position before which to insert the list.</span></span> <span data-ttu-id="5914a-110">Se *p* for **NULL**, esse método adicionará o item à parte final da lista.</span><span class="sxs-lookup"><span data-stu-id="5914a-110">If *p* is **NULL**, this method adds the item to the tail of the list.</span></span>

</dd> <dt>

<span data-ttu-id="5914a-111">*pObj*</span><span class="sxs-lookup"><span data-stu-id="5914a-111">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="5914a-112">Ponteiro para um objeto do tipo **Object** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="5914a-112">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5914a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5914a-113">Return value</span></span>

<span data-ttu-id="5914a-114">Retorna o indicador de posição do item inserido.</span><span class="sxs-lookup"><span data-stu-id="5914a-114">Returns the position indicator for the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="5914a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5914a-115">Requirements</span></span>

| <span data-ttu-id="5914a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5914a-116">Requirement</span></span> | <span data-ttu-id="5914a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5914a-117">Value</span></span> |
|-|-|
| <span data-ttu-id="5914a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5914a-118">Header</span></span> | <span data-ttu-id="5914a-119">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="5914a-119">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="5914a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5914a-120">Library</span></span>| <span data-ttu-id="5914a-121">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="5914a-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5914a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5914a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5914a-123">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="5914a-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




