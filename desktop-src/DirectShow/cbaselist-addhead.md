---
description: O método AddHead insere outra lista na frente desta lista.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Método CBaseList. AddHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756827"
---
# <a name="cbaselistaddhead-method"></a><span data-ttu-id="7fcda-103">Método CBaseList. AddHead</span><span class="sxs-lookup"><span data-stu-id="7fcda-103">CBaseList.AddHead method</span></span>

<span data-ttu-id="7fcda-104">O `AddHead` método insere outra lista na frente desta lista.</span><span class="sxs-lookup"><span data-stu-id="7fcda-104">The `AddHead` method inserts another list at the front of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fcda-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fcda-105">Syntax</span></span>


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="7fcda-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fcda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fcda-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="7fcda-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="7fcda-108">Ponteiro para a lista de itens a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="7fcda-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fcda-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fcda-109">Return value</span></span>

<span data-ttu-id="7fcda-110">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7fcda-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fcda-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fcda-111">Remarks</span></span>

<span data-ttu-id="7fcda-112">Se o método falhar, alguns itens poderão ter sido adicionados à lista.</span><span class="sxs-lookup"><span data-stu-id="7fcda-112">If the method fails, some items might have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcda-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fcda-113">Requirements</span></span>



| <span data-ttu-id="7fcda-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fcda-114">Requirement</span></span> | <span data-ttu-id="7fcda-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7fcda-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcda-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fcda-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7fcda-117"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fcda-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7fcda-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fcda-118">Library</span></span><br/> | <dl> <span data-ttu-id="7fcda-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7fcda-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcda-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fcda-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcda-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="7fcda-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




