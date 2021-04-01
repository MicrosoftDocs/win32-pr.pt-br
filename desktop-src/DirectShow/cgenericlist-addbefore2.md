---
description: O método addantes insere uma lista antes da posição especificada. Esse método usa os parâmetros ' pos ' e ' pList '.
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Método CGenericList. AddBefore (Wxlist. h)-Pos, parâmetros do pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103664130"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="dd314-104">Método CGenericList. AddBefore (Wxlist. h)-Pos, parâmetros do pList</span><span class="sxs-lookup"><span data-stu-id="dd314-104">CGenericList.AddBefore method (Wxlist.h) - pos, pList parameters</span></span>

<span data-ttu-id="dd314-105">O `AddBefore` método insere uma lista antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="dd314-105">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd314-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd314-106">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="dd314-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd314-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd314-108">*pos*</span><span class="sxs-lookup"><span data-stu-id="dd314-108">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="dd314-109">Posição para inserir a lista.</span><span class="sxs-lookup"><span data-stu-id="dd314-109">Position to insert the list.</span></span> <span data-ttu-id="dd314-110">A lista é inserida antes dessa posição.</span><span class="sxs-lookup"><span data-stu-id="dd314-110">The list is inserted before this position.</span></span>

</dd> <dt>

<span data-ttu-id="dd314-111">*pList*</span><span class="sxs-lookup"><span data-stu-id="dd314-111">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="dd314-112">Ponteiro para a lista a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="dd314-112">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd314-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd314-113">Return value</span></span>

<span data-ttu-id="dd314-114">Retornará **true** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dd314-114">Returns **TRUE** if successful.</span></span> <span data-ttu-id="dd314-115">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="dd314-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd314-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd314-116">Requirements</span></span>

| <span data-ttu-id="dd314-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd314-117">Requirement</span></span> | <span data-ttu-id="dd314-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dd314-118">Value</span></span> |
|-|-|
| <span data-ttu-id="dd314-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd314-119">Header</span></span> | <span data-ttu-id="dd314-120">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="dd314-120">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="dd314-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd314-121">Library</span></span>| <span data-ttu-id="dd314-122">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="dd314-122">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="dd314-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd314-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd314-124">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="dd314-124">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




