---
description: O método RemoveTailI remove o último item da lista.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Método CBaseList. RemoveTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811761"
---
# <a name="cbaselistremovetaili-method"></a><span data-ttu-id="42091-103">Método CBaseList. RemoveTailI</span><span class="sxs-lookup"><span data-stu-id="42091-103">CBaseList.RemoveTailI method</span></span>

<span data-ttu-id="42091-104">O `RemoveTailI` método remove o último item da lista.</span><span class="sxs-lookup"><span data-stu-id="42091-104">The `RemoveTailI` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="42091-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42091-105">Syntax</span></span>


```C++
void* RemoveTailI();
```



## <a name="parameters"></a><span data-ttu-id="42091-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42091-106">Parameters</span></span>

<span data-ttu-id="42091-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="42091-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42091-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42091-108">Return value</span></span>

<span data-ttu-id="42091-109">Retorna um ponteiro para o item ou **NULL** se a lista estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="42091-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="42091-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="42091-110">Remarks</span></span>

<span data-ttu-id="42091-111">Esse método exclui o nó da lista, mas não o item contido no nó.</span><span class="sxs-lookup"><span data-stu-id="42091-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="42091-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42091-112">Requirements</span></span>



| <span data-ttu-id="42091-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="42091-113">Requirement</span></span> | <span data-ttu-id="42091-114">Valor</span><span class="sxs-lookup"><span data-stu-id="42091-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42091-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42091-115">Header</span></span><br/>  | <dl> <span data-ttu-id="42091-116"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42091-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="42091-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42091-117">Library</span></span><br/> | <dl> <span data-ttu-id="42091-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="42091-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42091-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="42091-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42091-120">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="42091-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




