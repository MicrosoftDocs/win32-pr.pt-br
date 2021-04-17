---
description: O método RemoveHead remove o primeiro item da lista.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Método CGenericList. RemoveHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748629"
---
# <a name="cgenericlistremovehead-method"></a><span data-ttu-id="5f46c-103">Método CGenericList. RemoveHead</span><span class="sxs-lookup"><span data-stu-id="5f46c-103">CGenericList.RemoveHead method</span></span>

<span data-ttu-id="5f46c-104">O `RemoveHead` método remove o primeiro item da lista.</span><span class="sxs-lookup"><span data-stu-id="5f46c-104">The `RemoveHead` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f46c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f46c-105">Syntax</span></span>


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a><span data-ttu-id="5f46c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f46c-106">Parameters</span></span>

<span data-ttu-id="5f46c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5f46c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f46c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f46c-108">Return value</span></span>

<span data-ttu-id="5f46c-109">Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo) ou **NULL** se a lista estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="5f46c-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f46c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f46c-110">Remarks</span></span>

<span data-ttu-id="5f46c-111">Esse método exclui o nó da lista, mas não o item que o nó contém.</span><span class="sxs-lookup"><span data-stu-id="5f46c-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f46c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f46c-112">Requirements</span></span>



| <span data-ttu-id="5f46c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f46c-113">Requirement</span></span> | <span data-ttu-id="5f46c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5f46c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f46c-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f46c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5f46c-116"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f46c-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5f46c-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f46c-117">Library</span></span><br/> | <dl> <span data-ttu-id="5f46c-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5f46c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f46c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f46c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f46c-120">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="5f46c-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




