---
description: O método removeri remove o item na posição especificada.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Método CBaseList. Removei (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771870"
---
# <a name="cbaselistremovei-method"></a><span data-ttu-id="438e8-103">Método CBaseList. Removei</span><span class="sxs-lookup"><span data-stu-id="438e8-103">CBaseList.RemoveI method</span></span>

<span data-ttu-id="438e8-104">O `RemoveI` método remove o item na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="438e8-104">The `RemoveI` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="438e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="438e8-105">Syntax</span></span>


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="438e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="438e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="438e8-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="438e8-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="438e8-108">Valor de posição indicando o item a ser removido.</span><span class="sxs-lookup"><span data-stu-id="438e8-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="438e8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="438e8-109">Return value</span></span>

<span data-ttu-id="438e8-110">Retorna um ponteiro para o item.</span><span class="sxs-lookup"><span data-stu-id="438e8-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="438e8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="438e8-111">Remarks</span></span>

<span data-ttu-id="438e8-112">Esse método exclui o nó da lista, mas não exclui o item contido nesse nó.</span><span class="sxs-lookup"><span data-stu-id="438e8-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="438e8-113">Se o *PDV* for **nulo**, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="438e8-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="438e8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="438e8-114">Requirements</span></span>



| <span data-ttu-id="438e8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="438e8-115">Requirement</span></span> | <span data-ttu-id="438e8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="438e8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="438e8-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="438e8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="438e8-118"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="438e8-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="438e8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="438e8-119">Library</span></span><br/> | <dl> <span data-ttu-id="438e8-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="438e8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="438e8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="438e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="438e8-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="438e8-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




