---
description: O método addcauda acrescenta outra lista ao final desta lista.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Método CBaseList. addcaudal (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758873"
---
# <a name="cbaselistaddtail-method"></a><span data-ttu-id="1fcfd-103">Método CBaseList. addcaudal</span><span class="sxs-lookup"><span data-stu-id="1fcfd-103">CBaseList.AddTail method</span></span>

<span data-ttu-id="1fcfd-104">O `AddTail` método acrescenta outra lista ao final desta lista.</span><span class="sxs-lookup"><span data-stu-id="1fcfd-104">The `AddTail` method appends another list to the end of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fcfd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fcfd-105">Syntax</span></span>


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="1fcfd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fcfd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fcfd-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="1fcfd-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="1fcfd-108">Ponteiro para a lista a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="1fcfd-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fcfd-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fcfd-109">Return value</span></span>

<span data-ttu-id="1fcfd-110">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1fcfd-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fcfd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fcfd-111">Remarks</span></span>

<span data-ttu-id="1fcfd-112">Se o método falhar, alguns itens poderão ter sido adicionados à lista.</span><span class="sxs-lookup"><span data-stu-id="1fcfd-112">If the method fails, some items may have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcfd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fcfd-113">Requirements</span></span>



| <span data-ttu-id="1fcfd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcfd-114">Requirement</span></span> | <span data-ttu-id="1fcfd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1fcfd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcfd-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fcfd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1fcfd-117"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fcfd-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1fcfd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fcfd-118">Library</span></span><br/> | <dl> <span data-ttu-id="1fcfd-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1fcfd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fcfd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fcfd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcfd-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="1fcfd-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




