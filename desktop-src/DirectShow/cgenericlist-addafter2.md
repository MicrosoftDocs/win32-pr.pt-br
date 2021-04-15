---
description: O método addapós insere uma lista após a posição especificada e usa os parâmetros ' pos ' e ' plist '.
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Método CGenericList. AddAfter (Wxlist. h)-Pos, parâmetros do plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506545"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="59717-103">Método CGenericList. AddAfter (Wxlist. h)-Pos, parâmetros do plist</span><span class="sxs-lookup"><span data-stu-id="59717-103">CGenericList.AddAfter method (Wxlist.h) - pos, plist parameters</span></span>

<span data-ttu-id="59717-104">O `AddAfter` método insere uma lista após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="59717-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="59717-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59717-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="59717-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59717-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="59717-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="59717-108">Posição para inserir a lista.</span><span class="sxs-lookup"><span data-stu-id="59717-108">Position to insert the list.</span></span> <span data-ttu-id="59717-109">A lista é inserida após esta posição.</span><span class="sxs-lookup"><span data-stu-id="59717-109">The list is inserted after this position.</span></span>

</dd> <dt>

<span data-ttu-id="59717-110">*pList*</span><span class="sxs-lookup"><span data-stu-id="59717-110">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="59717-111">Ponteiro para a lista a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="59717-111">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59717-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59717-112">Return value</span></span>

<span data-ttu-id="59717-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="59717-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="59717-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59717-114">Requirements</span></span>

| <span data-ttu-id="59717-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="59717-115">Requirement</span></span> | <span data-ttu-id="59717-116">Valor</span><span class="sxs-lookup"><span data-stu-id="59717-116">Value</span></span> |
|-|-|
| <span data-ttu-id="59717-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59717-117">Header</span></span> | <span data-ttu-id="59717-118">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="59717-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="59717-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59717-119">Library</span></span>| <span data-ttu-id="59717-120">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="59717-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="59717-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="59717-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59717-122">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="59717-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




