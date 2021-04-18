---
description: O método MoveToTail divide a lista e acrescenta a parte de cabeçalho ao final de outra lista.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Método CBaseList. MoveToTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749636"
---
# <a name="cbaselistmovetotail-method"></a><span data-ttu-id="32016-103">Método CBaseList. MoveToTail</span><span class="sxs-lookup"><span data-stu-id="32016-103">CBaseList.MoveToTail method</span></span>

<span data-ttu-id="32016-104">O `MoveToTail` método divide a lista e acrescenta a parte de cabeçalho ao final de outra lista.</span><span class="sxs-lookup"><span data-stu-id="32016-104">The `MoveToTail` method splits the list and appends the head portion to the tail of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="32016-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32016-105">Syntax</span></span>


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="32016-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32016-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32016-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="32016-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="32016-108">Indicador de posição que marca a divisão na lista.</span><span class="sxs-lookup"><span data-stu-id="32016-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="32016-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="32016-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="32016-110">Ponteiro para outra lista.</span><span class="sxs-lookup"><span data-stu-id="32016-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32016-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32016-111">Return value</span></span>

<span data-ttu-id="32016-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="32016-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="32016-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="32016-113">Remarks</span></span>

<span data-ttu-id="32016-114">Esse método divide a lista após a posição especificada pelo parâmetro *pos* .</span><span class="sxs-lookup"><span data-stu-id="32016-114">This method splits the list after the position specified by the *pos* parameter.</span></span> <span data-ttu-id="32016-115">A parte final permanece na lista.</span><span class="sxs-lookup"><span data-stu-id="32016-115">The tail portion remains in the list.</span></span> <span data-ttu-id="32016-116">A parte de cabeçalho é anexada ao final da outra lista.</span><span class="sxs-lookup"><span data-stu-id="32016-116">The head portion is appended to the tail of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="32016-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32016-117">Requirements</span></span>



| <span data-ttu-id="32016-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32016-118">Requirement</span></span> | <span data-ttu-id="32016-119">Valor</span><span class="sxs-lookup"><span data-stu-id="32016-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32016-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32016-120">Header</span></span><br/>  | <dl> <span data-ttu-id="32016-121"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32016-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="32016-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32016-122">Library</span></span><br/> | <dl> <span data-ttu-id="32016-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="32016-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32016-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="32016-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32016-125">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="32016-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




