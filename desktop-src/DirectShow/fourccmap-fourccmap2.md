---
description: Um método de construtor que fornece o mapeamento entre os tipos DWORD de formato multimídia de estilo antigo e os subtipos GUID. Esse método usa o parâmetro ' FOURCC '.
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Construtor FOURCCMap:: FOURCCMap (FOURCC. h) – parâmetro FOURCC'
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
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105749603"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a><span data-ttu-id="dbdf2-104">Construtor FOURCCMap:: FOURCCMap (FOURCC. h) – parâmetro FOURCC</span><span class="sxs-lookup"><span data-stu-id="dbdf2-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - Fourcc parameter</span></span>

<span data-ttu-id="dbdf2-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="dbdf2-105">Constructor method.</span></span> <span data-ttu-id="dbdf2-106">O constuctor fornece o mapeamento entre os tipos **DWORD** de formato multimídia de estilo antigo e os subtipos de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="dbdf2-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbdf2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbdf2-107">Syntax</span></span>


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a><span data-ttu-id="dbdf2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbdf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbdf2-109">*FOURCC*</span><span class="sxs-lookup"><span data-stu-id="dbdf2-109">*Fourcc*</span></span> 
</dt> <dd>

<span data-ttu-id="dbdf2-110">**DWORD** que especifica o FOURCC.</span><span class="sxs-lookup"><span data-stu-id="dbdf2-110">**DWORD** that specifies the FOURCC.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbdf2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbdf2-111">Remarks</span></span>

<span data-ttu-id="dbdf2-112">Se esse objeto for construído com o código **FOURCC** , um **GUID** será criado para corresponder a ele.</span><span class="sxs-lookup"><span data-stu-id="dbdf2-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="dbdf2-113">Se esse objeto for criado com um **GUID** existente, o valor **FOURCC** do objeto será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="dbdf2-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="dbdf2-114">Depois disso, o valor **FOURCC** pode ser definido ou recuperado usando as funções de membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="dbdf2-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbdf2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbdf2-115">Requirements</span></span>

| <span data-ttu-id="dbdf2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbdf2-116">Requirement</span></span> | <span data-ttu-id="dbdf2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dbdf2-117">Value</span></span> |
|-|-|
| <span data-ttu-id="dbdf2-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbdf2-118">Header</span></span>  | <span data-ttu-id="dbdf2-119">FourCC. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="dbdf2-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="dbdf2-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbdf2-120">Library</span></span> | <span data-ttu-id="dbdf2-121">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="dbdf2-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="dbdf2-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbdf2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbdf2-123">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="dbdf2-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




