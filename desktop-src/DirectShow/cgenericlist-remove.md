---
description: O método remove remove o item na posição especificada.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Método CGenericList. Remove (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752700"
---
# <a name="cgenericlistremove-method"></a><span data-ttu-id="e445c-103">Método CGenericList. Remove</span><span class="sxs-lookup"><span data-stu-id="e445c-103">CGenericList.Remove method</span></span>

<span data-ttu-id="e445c-104">O `Remove` método remove o item na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="e445c-104">The `Remove` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="e445c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e445c-105">Syntax</span></span>


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="e445c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e445c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e445c-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="e445c-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="e445c-108">Valor de posição indicando o item a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e445c-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e445c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e445c-109">Return value</span></span>

<span data-ttu-id="e445c-110">Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="e445c-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="e445c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e445c-111">Remarks</span></span>

<span data-ttu-id="e445c-112">Esse método exclui o nó da lista, mas não exclui o item contido nesse nó.</span><span class="sxs-lookup"><span data-stu-id="e445c-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="e445c-113">Se o *PDV* for **nulo**, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e445c-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e445c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e445c-114">Requirements</span></span>



| <span data-ttu-id="e445c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e445c-115">Requirement</span></span> | <span data-ttu-id="e445c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e445c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e445c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e445c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e445c-118"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e445c-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e445c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e445c-119">Library</span></span><br/> | <dl> <span data-ttu-id="e445c-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e445c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e445c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e445c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e445c-122">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="e445c-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




