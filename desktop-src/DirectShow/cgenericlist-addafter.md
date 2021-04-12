---
description: O método addapós insere um item após a posição especificada e usa os parâmetros ' p ' e ' pObj '.
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Método CGenericList. AddAfter (Wxlist. h)-p, pObj parâmetros
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104298880"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="8ef01-103">Método CGenericList. AddAfter (Wxlist. h)-p, pObj parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ef01-103">CGenericList.AddAfter method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="8ef01-104">O `AddAfter` método insere um item após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="8ef01-104">The `AddAfter` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ef01-105">Syntax</span></span>


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="8ef01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ef01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ef01-107">*DTI*</span><span class="sxs-lookup"><span data-stu-id="8ef01-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef01-108">Posição após a qual adicionar o item.</span><span class="sxs-lookup"><span data-stu-id="8ef01-108">Position after which to add the item.</span></span> <span data-ttu-id="8ef01-109">Se *p* for **NULL**, o método adicionará o item ao cabeçalho da lista.</span><span class="sxs-lookup"><span data-stu-id="8ef01-109">If *p* is **NULL**, the method adds the item to the head of the list.</span></span>

</dd> <dt>

<span data-ttu-id="8ef01-110">*pObj*</span><span class="sxs-lookup"><span data-stu-id="8ef01-110">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef01-111">Ponteiro para um objeto do tipo **Object** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="8ef01-111">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ef01-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ef01-112">Return value</span></span>

<span data-ttu-id="8ef01-113">Retorna o indicador de posição do item inserido.</span><span class="sxs-lookup"><span data-stu-id="8ef01-113">Returns the position indicator of the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef01-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ef01-114">Requirements</span></span>

| <span data-ttu-id="8ef01-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ef01-115">Requirement</span></span> | <span data-ttu-id="8ef01-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8ef01-116">Value</span></span> |
|-|-|
| <span data-ttu-id="8ef01-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ef01-117">Header</span></span> | <span data-ttu-id="8ef01-118">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="8ef01-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="8ef01-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ef01-119">Library</span></span>| <span data-ttu-id="8ef01-120">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="8ef01-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="8ef01-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ef01-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef01-122">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="8ef01-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




