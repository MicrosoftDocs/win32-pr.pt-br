---
description: O método RemoveTail remove o último item da lista.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Método CGenericList. RemoveTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752896"
---
# <a name="cgenericlistremovetail-method"></a><span data-ttu-id="c4007-103">Método CGenericList. RemoveTail</span><span class="sxs-lookup"><span data-stu-id="c4007-103">CGenericList.RemoveTail method</span></span>

<span data-ttu-id="c4007-104">O `RemoveTail` método remove o último item da lista.</span><span class="sxs-lookup"><span data-stu-id="c4007-104">The `RemoveTail` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4007-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4007-105">Syntax</span></span>


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a><span data-ttu-id="c4007-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4007-106">Parameters</span></span>

<span data-ttu-id="c4007-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c4007-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4007-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4007-108">Return value</span></span>

<span data-ttu-id="c4007-109">Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo) ou **NULL** se a lista estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="c4007-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4007-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4007-110">Remarks</span></span>

<span data-ttu-id="c4007-111">Esse método exclui o nó da lista, mas não o item contido no nó.</span><span class="sxs-lookup"><span data-stu-id="c4007-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4007-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4007-112">Requirements</span></span>



| <span data-ttu-id="c4007-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4007-113">Requirement</span></span> | <span data-ttu-id="c4007-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c4007-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4007-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4007-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c4007-116"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4007-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c4007-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4007-117">Library</span></span><br/> | <dl> <span data-ttu-id="c4007-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c4007-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4007-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4007-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4007-120">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="c4007-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




