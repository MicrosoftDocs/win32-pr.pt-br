---
description: O método addapós insere uma lista após a posição especificada.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Método CBaseList. AddAfter (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749848"
---
# <a name="cbaselistaddafter-method"></a><span data-ttu-id="99bc4-103">Método CBaseList. AddAfter</span><span class="sxs-lookup"><span data-stu-id="99bc4-103">CBaseList.AddAfter method</span></span>

<span data-ttu-id="99bc4-104">O `AddAfter` método insere uma lista após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="99bc4-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bc4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99bc4-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="99bc4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99bc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99bc4-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="99bc4-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="99bc4-108">Posição após a qual inserir a lista.</span><span class="sxs-lookup"><span data-stu-id="99bc4-108">Position after which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="99bc4-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="99bc4-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="99bc4-110">Ponteiro para a lista a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="99bc4-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99bc4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99bc4-111">Return value</span></span>

<span data-ttu-id="99bc4-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="99bc4-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bc4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="99bc4-113">Remarks</span></span>

<span data-ttu-id="99bc4-114">Os indicadores de posição existentes, incluindo aquele especificado no parâmetro *pos* , permanecem válidos.</span><span class="sxs-lookup"><span data-stu-id="99bc4-114">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="99bc4-115">Se o método falhar, alguns dos itens podem ter sido adicionados.</span><span class="sxs-lookup"><span data-stu-id="99bc4-115">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="99bc4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99bc4-116">Requirements</span></span>



| <span data-ttu-id="99bc4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="99bc4-117">Requirement</span></span> | <span data-ttu-id="99bc4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="99bc4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99bc4-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99bc4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="99bc4-120"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99bc4-120"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="99bc4-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99bc4-121">Library</span></span><br/> | <dl> <span data-ttu-id="99bc4-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="99bc4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99bc4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="99bc4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99bc4-124">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="99bc4-124">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




