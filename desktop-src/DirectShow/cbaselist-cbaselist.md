---
description: Método de construtor.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Construtor CBaseList. CBaseList (TCHAR *, INT) (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778641"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="dd8d8-103">Construtor CBaseList. CBaseList (TCHAR \* , int)</span><span class="sxs-lookup"><span data-stu-id="dd8d8-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="dd8d8-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd8d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd8d8-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="dd8d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd8d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd8d8-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="dd8d8-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="dd8d8-108">Ponteiro para o nome da lista.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="dd8d8-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="dd8d8-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="dd8d8-110">Tamanho do cache do nó.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd8d8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd8d8-111">Remarks</span></span>

<span data-ttu-id="dd8d8-112">Para eficiência, a `CBaseList` classe mantém um cache de nós de lista.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="dd8d8-113">Se você souber aproximadamente quantos itens a lista manterá, use esta versão do construtor.</span><span class="sxs-lookup"><span data-stu-id="dd8d8-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd8d8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd8d8-114">Requirements</span></span>



| <span data-ttu-id="dd8d8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd8d8-115">Requirement</span></span> | <span data-ttu-id="dd8d8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="dd8d8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd8d8-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd8d8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="dd8d8-118"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd8d8-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="dd8d8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd8d8-119">Library</span></span><br/> | <dl> <span data-ttu-id="dd8d8-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dd8d8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd8d8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd8d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd8d8-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="dd8d8-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




