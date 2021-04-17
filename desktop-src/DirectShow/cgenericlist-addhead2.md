---
description: O método AddHead adiciona uma lista à frente da lista.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Método CGenericList. AddHead (Wxlist. h)-parâmetro pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105754539"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a><span data-ttu-id="e00ec-103">Método CGenericList. AddHead (Wxlist. h)-parâmetro pList</span><span class="sxs-lookup"><span data-stu-id="e00ec-103">CGenericList.AddHead method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="e00ec-104">O `AddHead` método adiciona uma lista à frente da lista.</span><span class="sxs-lookup"><span data-stu-id="e00ec-104">The `AddHead` method adds a list to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e00ec-105">Syntax</span></span>


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="e00ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e00ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00ec-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="e00ec-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="e00ec-108">Ponteiro para a lista de itens a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="e00ec-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00ec-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e00ec-109">Return value</span></span>

<span data-ttu-id="e00ec-110">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e00ec-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00ec-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e00ec-111">Requirements</span></span>

| <span data-ttu-id="e00ec-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e00ec-112">Requirement</span></span> | <span data-ttu-id="e00ec-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e00ec-113">Value</span></span> |
|-|-|
| <span data-ttu-id="e00ec-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e00ec-114">Header</span></span> | <span data-ttu-id="e00ec-115">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="e00ec-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="e00ec-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e00ec-116">Library</span></span>| <span data-ttu-id="e00ec-117">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="e00ec-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e00ec-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e00ec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00ec-119">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="e00ec-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




