---
description: O método addantesi insere um item antes da posição especificada.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Método CBaseList. addantesi (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778643"
---
# <a name="cbaselistaddbeforei-method"></a><span data-ttu-id="4e162-103">Método CBaseList. addantesi</span><span class="sxs-lookup"><span data-stu-id="4e162-103">CBaseList.AddBeforeI method</span></span>

<span data-ttu-id="4e162-104">O `AddBeforeI` método insere um item antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="4e162-104">The `AddBeforeI` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e162-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e162-105">Syntax</span></span>


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="4e162-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e162-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e162-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="4e162-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="4e162-108">Posição antes da qual adicionar o item.</span><span class="sxs-lookup"><span data-stu-id="4e162-108">Position before which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="4e162-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="4e162-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="4e162-110">Ponteiro para o item.</span><span class="sxs-lookup"><span data-stu-id="4e162-110">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e162-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e162-111">Return value</span></span>

<span data-ttu-id="4e162-112">Retorna o indicador de posição do item inserido.</span><span class="sxs-lookup"><span data-stu-id="4e162-112">Returns the position indicator for the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e162-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e162-113">Remarks</span></span>

<span data-ttu-id="4e162-114">Se o *PDV* for **nulo**, esse método adicionará o item à parte final da lista (equivalente a chamar o método [**CBaseList:: addcaudai**](cbaselist-addtaili.md) ).</span><span class="sxs-lookup"><span data-stu-id="4e162-114">If *pos* is **NULL**, this method adds the item to the tail of the list (equivalent to calling the [**CBaseList::AddTailI**](cbaselist-addtaili.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e162-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e162-115">Requirements</span></span>



| <span data-ttu-id="4e162-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e162-116">Requirement</span></span> | <span data-ttu-id="4e162-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4e162-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e162-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e162-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4e162-119"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e162-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4e162-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e162-120">Library</span></span><br/> | <dl> <span data-ttu-id="4e162-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4e162-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e162-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e162-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e162-123">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="4e162-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




