---
description: Um método de construtor que fornece o mapeamento entre os tipos DWORD de formato multimídia de estilo antigo e os subtipos GUID. Esse método não usa parâmetros.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Construtor FOURCCMap:: FOURCCMap (FOURCC. h) – sem parâmetros'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105760747"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a><span data-ttu-id="ccb35-104">Construtor FOURCCMap:: FOURCCMap (FOURCC. h) – sem parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccb35-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - No parameters</span></span>

<span data-ttu-id="ccb35-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="ccb35-105">Constructor method.</span></span> <span data-ttu-id="ccb35-106">O constuctor fornece o mapeamento entre os tipos **DWORD** de formato multimídia de estilo antigo e os subtipos de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="ccb35-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb35-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccb35-107">Syntax</span></span>


```C++
FOURCCMap();
```



## <a name="parameters"></a><span data-ttu-id="ccb35-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccb35-108">Parameters</span></span>

<span data-ttu-id="ccb35-109">Este construtor não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ccb35-109">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccb35-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccb35-110">Remarks</span></span>

<span data-ttu-id="ccb35-111">Se esse objeto for construído com o código **FOURCC** , um **GUID** será criado para corresponder a ele.</span><span class="sxs-lookup"><span data-stu-id="ccb35-111">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="ccb35-112">Se esse objeto for criado com um **GUID** existente, o valor **FOURCC** do objeto será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="ccb35-112">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="ccb35-113">Depois disso, o valor **FOURCC** pode ser definido ou recuperado usando as funções de membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ccb35-113">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb35-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb35-114">Requirements</span></span>


| <span data-ttu-id="ccb35-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb35-115">Requirement</span></span> | <span data-ttu-id="ccb35-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ccb35-116">Value</span></span> |
|-|-|
| <span data-ttu-id="ccb35-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccb35-117">Header</span></span>  | <span data-ttu-id="ccb35-118">FourCC. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="ccb35-118">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="ccb35-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ccb35-119">Library</span></span> | <span data-ttu-id="ccb35-120">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="ccb35-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



## <a name="see-also"></a><span data-ttu-id="ccb35-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccb35-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb35-122">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="ccb35-122">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




