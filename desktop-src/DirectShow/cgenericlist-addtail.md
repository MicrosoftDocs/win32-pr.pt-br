---
description: O método addcauda acrescenta um item ao final da lista.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Método CGenericList. addcauda (Wxlist. h)-parâmetro pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105755350"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a><span data-ttu-id="273a6-103">Método CGenericList. addcauda (Wxlist. h)-parâmetro pObj</span><span class="sxs-lookup"><span data-stu-id="273a6-103">CGenericList.AddTail method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="273a6-104">O `AddTail` método anexa um item ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="273a6-104">The `AddTail` method appends an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="273a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="273a6-105">Syntax</span></span>


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="273a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="273a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="273a6-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="273a6-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="273a6-108">Ponteiro para um objeto do tipo **Object** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="273a6-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="273a6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="273a6-109">Return value</span></span>

<span data-ttu-id="273a6-110">Retorna um valor de posição para a nova posição de cauda.</span><span class="sxs-lookup"><span data-stu-id="273a6-110">Returns a POSITION value for the new tail position.</span></span> <span data-ttu-id="273a6-111">Se o método falhar, ele retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="273a6-111">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="273a6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="273a6-112">Requirements</span></span>

| <span data-ttu-id="273a6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="273a6-113">Requirement</span></span> | <span data-ttu-id="273a6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="273a6-114">Value</span></span> |
|-|-|
| <span data-ttu-id="273a6-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="273a6-115">Header</span></span> | <span data-ttu-id="273a6-116">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="273a6-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="273a6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="273a6-117">Library</span></span>| <span data-ttu-id="273a6-118">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="273a6-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="273a6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="273a6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273a6-120">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="273a6-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




