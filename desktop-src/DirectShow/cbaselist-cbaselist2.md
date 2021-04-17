---
description: Método de construtor.
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
ms.openlocfilehash: 3afc0a4acf54e186e122f676ac14e9e80aaeafdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747410"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="3777b-103">Construtor CBaseList. CBaseList</span><span class="sxs-lookup"><span data-stu-id="3777b-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="3777b-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="3777b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3777b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3777b-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="3777b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3777b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3777b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3777b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3777b-108">Ponteiro para o nome da lista.</span><span class="sxs-lookup"><span data-stu-id="3777b-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3777b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3777b-109">Remarks</span></span>

<span data-ttu-id="3777b-110">Para eficiência, a `CBaseList` classe mantém um cache de nós de lista.</span><span class="sxs-lookup"><span data-stu-id="3777b-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="3777b-111">Esta versão do construtor usa um tamanho de cache padrão.</span><span class="sxs-lookup"><span data-stu-id="3777b-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="3777b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3777b-112">Requirements</span></span>



| <span data-ttu-id="3777b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3777b-113">Requirement</span></span> | <span data-ttu-id="3777b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3777b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3777b-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3777b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3777b-116"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3777b-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3777b-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3777b-117">Library</span></span><br/> | <dl> <span data-ttu-id="3777b-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3777b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3777b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3777b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3777b-120">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="3777b-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




