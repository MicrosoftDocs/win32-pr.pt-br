---
description: O método MoveToHead divide a lista e insere a parte final no cabeçalho de outra lista.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Método CBaseList. MoveToHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778640"
---
# <a name="cbaselistmovetohead-method"></a><span data-ttu-id="ebb16-103">Método CBaseList. MoveToHead</span><span class="sxs-lookup"><span data-stu-id="ebb16-103">CBaseList.MoveToHead method</span></span>

<span data-ttu-id="ebb16-104">O `MoveToHead` método divide a lista e insere a parte final no cabeçalho de outra lista.</span><span class="sxs-lookup"><span data-stu-id="ebb16-104">The `MoveToHead` method splits the list and inserts the tail portion at the head of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb16-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebb16-105">Syntax</span></span>


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="ebb16-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebb16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb16-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="ebb16-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="ebb16-108">Indicador de posição que marca a divisão na lista.</span><span class="sxs-lookup"><span data-stu-id="ebb16-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="ebb16-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="ebb16-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="ebb16-110">Ponteiro para outra lista.</span><span class="sxs-lookup"><span data-stu-id="ebb16-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebb16-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebb16-111">Return value</span></span>

<span data-ttu-id="ebb16-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ebb16-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebb16-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebb16-113">Remarks</span></span>

<span data-ttu-id="ebb16-114">Esse método divide a lista antes da posição especificada pelo parâmetro *pos* .</span><span class="sxs-lookup"><span data-stu-id="ebb16-114">This method splits the list before the position specified by the *pos* parameter.</span></span> <span data-ttu-id="ebb16-115">A parte de cabeçalho permanece na lista.</span><span class="sxs-lookup"><span data-stu-id="ebb16-115">The head portion remains in the list.</span></span> <span data-ttu-id="ebb16-116">A parte final é inserida no cabeçalho da outra lista.</span><span class="sxs-lookup"><span data-stu-id="ebb16-116">The tail portion is inserted at the head of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb16-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb16-117">Requirements</span></span>



| <span data-ttu-id="ebb16-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb16-118">Requirement</span></span> | <span data-ttu-id="ebb16-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ebb16-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb16-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebb16-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ebb16-121"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebb16-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ebb16-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebb16-122">Library</span></span><br/> | <dl> <span data-ttu-id="ebb16-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ebb16-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebb16-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebb16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb16-125">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="ebb16-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




