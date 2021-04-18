---
description: O método addcaudai adiciona um item ao final da lista.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Método CBaseList. addcaudai (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751914"
---
# <a name="cbaselistaddtaili-method"></a><span data-ttu-id="90a49-103">Método CBaseList. addcaudai</span><span class="sxs-lookup"><span data-stu-id="90a49-103">CBaseList.AddTailI method</span></span>

<span data-ttu-id="90a49-104">O `AddTailI` método adiciona um item ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="90a49-104">The `AddTailI` method adds an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a49-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90a49-105">Syntax</span></span>


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="90a49-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90a49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90a49-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="90a49-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="90a49-108">Ponteiro para o item.</span><span class="sxs-lookup"><span data-stu-id="90a49-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90a49-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90a49-109">Return value</span></span>

<span data-ttu-id="90a49-110">Retorna um valor de posição para a nova posição de cauda.</span><span class="sxs-lookup"><span data-stu-id="90a49-110">Returns a POSITION value for the new tail position.</span></span>

## <a name="remarks"></a><span data-ttu-id="90a49-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="90a49-111">Remarks</span></span>

<span data-ttu-id="90a49-112">Se o método falhar, ele retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="90a49-112">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a49-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a49-113">Requirements</span></span>



| <span data-ttu-id="90a49-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="90a49-114">Requirement</span></span> | <span data-ttu-id="90a49-115">Valor</span><span class="sxs-lookup"><span data-stu-id="90a49-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90a49-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90a49-116">Header</span></span><br/>  | <dl> <span data-ttu-id="90a49-117"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90a49-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="90a49-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90a49-118">Library</span></span><br/> | <dl> <span data-ttu-id="90a49-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="90a49-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90a49-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="90a49-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a49-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="90a49-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




