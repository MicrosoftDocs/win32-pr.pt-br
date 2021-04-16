---
description: O método AddAfterI insere um item após a posição especificada.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Método CBaseList. addifi (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750707"
---
# <a name="cbaselistaddafteri-method"></a><span data-ttu-id="b5c22-103">Método CBaseList. addifi</span><span class="sxs-lookup"><span data-stu-id="b5c22-103">CBaseList.AddAfterI method</span></span>

<span data-ttu-id="b5c22-104">O `AddAfterI` método insere um item após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="b5c22-104">The `AddAfterI` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5c22-105">Syntax</span></span>


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="b5c22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5c22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c22-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="b5c22-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="b5c22-108">Posição após a qual adicionar o item.</span><span class="sxs-lookup"><span data-stu-id="b5c22-108">Position after which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="b5c22-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="b5c22-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="b5c22-110">Ponteiro para o item a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="b5c22-110">Pointer to the item to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c22-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5c22-111">Return value</span></span>

<span data-ttu-id="b5c22-112">Retorna o indicador de posição do item inserido.</span><span class="sxs-lookup"><span data-stu-id="b5c22-112">Returns the position indicator of the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5c22-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5c22-113">Remarks</span></span>

<span data-ttu-id="b5c22-114">Se o *PDV* for **nulo**, esse método adicionará o item ao cabeçalho da lista (equivalente a chamar o método [**CBaseList:: AddHeadI**](cbaselist-addheadi.md) ).</span><span class="sxs-lookup"><span data-stu-id="b5c22-114">If *pos* is **NULL**, this method adds the item to the head of the list (equivalent to calling the [**CBaseList::AddHeadI**](cbaselist-addheadi.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c22-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5c22-115">Requirements</span></span>



| <span data-ttu-id="b5c22-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5c22-116">Requirement</span></span> | <span data-ttu-id="b5c22-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b5c22-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c22-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5c22-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b5c22-119"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c22-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b5c22-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5c22-120">Library</span></span><br/> | <dl> <span data-ttu-id="b5c22-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c22-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c22-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5c22-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c22-123">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="b5c22-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




