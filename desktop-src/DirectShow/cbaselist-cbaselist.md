---
description: '\*Método de construtor de Construtor CBaseList. CBaseList (TCHAR, int).'
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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099634"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="1d055-103">Construtor CBaseList. CBaseList (TCHAR \* , int)</span><span class="sxs-lookup"><span data-stu-id="1d055-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="1d055-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="1d055-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d055-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d055-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="1d055-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d055-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d055-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1d055-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1d055-108">Ponteiro para o nome da lista.</span><span class="sxs-lookup"><span data-stu-id="1d055-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="1d055-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="1d055-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="1d055-110">Tamanho do cache do nó.</span><span class="sxs-lookup"><span data-stu-id="1d055-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d055-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d055-111">Remarks</span></span>

<span data-ttu-id="1d055-112">Para eficiência, a `CBaseList` classe mantém um cache de nós de lista.</span><span class="sxs-lookup"><span data-stu-id="1d055-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="1d055-113">Se você souber aproximadamente quantos itens a lista manterá, use esta versão do construtor.</span><span class="sxs-lookup"><span data-stu-id="1d055-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d055-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d055-114">Requirements</span></span>



| <span data-ttu-id="1d055-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d055-115">Requirement</span></span> | <span data-ttu-id="1d055-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1d055-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d055-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d055-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1d055-118"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d055-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1d055-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d055-119">Library</span></span><br/> | <dl> <span data-ttu-id="1d055-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1d055-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d055-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1d055-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d055-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="1d055-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




