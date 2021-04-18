---
description: O método RemoveHeadI remove o primeiro item da lista.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Método CBaseList. RemoveHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787425"
---
# <a name="cbaselistremoveheadi-method"></a><span data-ttu-id="40e90-103">Método CBaseList. RemoveHeadI</span><span class="sxs-lookup"><span data-stu-id="40e90-103">CBaseList.RemoveHeadI method</span></span>

<span data-ttu-id="40e90-104">O `RemoveHeadI` método remove o primeiro item da lista.</span><span class="sxs-lookup"><span data-stu-id="40e90-104">The `RemoveHeadI` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e90-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40e90-105">Syntax</span></span>


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a><span data-ttu-id="40e90-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40e90-106">Parameters</span></span>

<span data-ttu-id="40e90-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="40e90-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40e90-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40e90-108">Return value</span></span>

<span data-ttu-id="40e90-109">Retorna um ponteiro para o item ou **NULL** se a lista estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="40e90-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="40e90-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="40e90-110">Remarks</span></span>

<span data-ttu-id="40e90-111">Esse método exclui o nó da lista, mas não o item que o nó contém.</span><span class="sxs-lookup"><span data-stu-id="40e90-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="40e90-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e90-112">Requirements</span></span>



| <span data-ttu-id="40e90-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="40e90-113">Requirement</span></span> | <span data-ttu-id="40e90-114">Valor</span><span class="sxs-lookup"><span data-stu-id="40e90-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40e90-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40e90-115">Header</span></span><br/>  | <dl> <span data-ttu-id="40e90-116"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40e90-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="40e90-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40e90-117">Library</span></span><br/> | <dl> <span data-ttu-id="40e90-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="40e90-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40e90-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="40e90-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e90-120">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="40e90-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




