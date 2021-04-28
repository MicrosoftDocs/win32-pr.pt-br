---
description: Construtor de CBaseList. CBaseList-método de construtor.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Construtor CBaseList. CBaseList (Wxlist. h)
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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096323"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="a706f-103">Construtor CBaseList. CBaseList</span><span class="sxs-lookup"><span data-stu-id="a706f-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="a706f-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="a706f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a706f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a706f-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="a706f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a706f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a706f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="a706f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a706f-108">Ponteiro para o nome da lista.</span><span class="sxs-lookup"><span data-stu-id="a706f-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a706f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a706f-109">Remarks</span></span>

<span data-ttu-id="a706f-110">Para eficiência, a `CBaseList` classe mantém um cache de nós de lista.</span><span class="sxs-lookup"><span data-stu-id="a706f-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="a706f-111">Esta versão do construtor usa um tamanho de cache padrão.</span><span class="sxs-lookup"><span data-stu-id="a706f-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="a706f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a706f-112">Requirements</span></span>



| <span data-ttu-id="a706f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a706f-113">Requirement</span></span> | <span data-ttu-id="a706f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a706f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a706f-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a706f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a706f-116"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a706f-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a706f-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a706f-117">Library</span></span><br/> | <dl> <span data-ttu-id="a706f-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a706f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a706f-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a706f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a706f-120">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="a706f-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




