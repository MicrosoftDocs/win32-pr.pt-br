---
description: Um método de construtor que fornece o mapeamento entre os tipos DWORD de formato multimídia de estilo antigo e os subtipos GUID. Esse método usa o parâmetro ' pGuid '.
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'Construtor FOURCCMap:: FOURCCMap (FOURCC. h)-parâmetro pGuid'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105757299"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a><span data-ttu-id="f395f-104">Construtor FOURCCMap:: FOURCCMap (FOURCC. h)-parâmetro pGuid</span><span class="sxs-lookup"><span data-stu-id="f395f-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - pguid parameter</span></span>

<span data-ttu-id="f395f-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="f395f-105">Constructor method.</span></span> <span data-ttu-id="f395f-106">O constuctor fornece o mapeamento entre os tipos **DWORD** de formato multimídia de estilo antigo e os subtipos de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="f395f-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f395f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f395f-107">Syntax</span></span>


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="f395f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f395f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f395f-109">*pguid*</span><span class="sxs-lookup"><span data-stu-id="f395f-109">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="f395f-110">Ponteiro para o identificador global exclusivo (**GUID**).</span><span class="sxs-lookup"><span data-stu-id="f395f-110">Pointer to the globally unique identifier (**GUID**).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f395f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f395f-111">Remarks</span></span>

<span data-ttu-id="f395f-112">Se esse objeto for construído com o código **FOURCC** , um **GUID** será criado para corresponder a ele.</span><span class="sxs-lookup"><span data-stu-id="f395f-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="f395f-113">Se esse objeto for criado com um **GUID** existente, o valor **FOURCC** do objeto será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="f395f-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="f395f-114">Depois disso, o valor **FOURCC** pode ser definido ou recuperado usando as funções de membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f395f-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="f395f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f395f-115">Requirements</span></span>

| <span data-ttu-id="f395f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f395f-116">Requirement</span></span> | <span data-ttu-id="f395f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f395f-117">Value</span></span> |
|-|-|
| <span data-ttu-id="f395f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f395f-118">Header</span></span>  | <span data-ttu-id="f395f-119">FourCC. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="f395f-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="f395f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f395f-120">Library</span></span> | <span data-ttu-id="f395f-121">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="f395f-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f395f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f395f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f395f-123">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="f395f-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




