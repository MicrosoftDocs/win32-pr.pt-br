---
description: A \_ estrutura do filtro AMOVIESETUP contém informações para registrar um filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Estrutura de AMOVIESETUP_FILTER (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747425"
---
# <a name="amoviesetup_filter-structure"></a><span data-ttu-id="e856d-103">\_Estrutura do filtro AMOVIESETUP</span><span class="sxs-lookup"><span data-stu-id="e856d-103">AMOVIESETUP\_FILTER structure</span></span>

<span data-ttu-id="e856d-104">A estrutura do **\_ filtro AMOVIESETUP** contém informações para registrar um filtro.</span><span class="sxs-lookup"><span data-stu-id="e856d-104">The **AMOVIESETUP\_FILTER** structure contains information for registering a filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e856d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e856d-105">Syntax</span></span>


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a><span data-ttu-id="e856d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e856d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e856d-107">**clsID**</span><span class="sxs-lookup"><span data-stu-id="e856d-107">**clsID**</span></span>
</dt> <dd>

<span data-ttu-id="e856d-108">Identificador de classe do filtro.</span><span class="sxs-lookup"><span data-stu-id="e856d-108">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="e856d-109">**strName**</span><span class="sxs-lookup"><span data-stu-id="e856d-109">**strName**</span></span>
</dt> <dd>

<span data-ttu-id="e856d-110">Nome do filtro.</span><span class="sxs-lookup"><span data-stu-id="e856d-110">Name of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="e856d-111">**dwMerit**</span><span class="sxs-lookup"><span data-stu-id="e856d-111">**dwMerit**</span></span>
</dt> <dd>

<span data-ttu-id="e856d-112">Mérito de filtro.</span><span class="sxs-lookup"><span data-stu-id="e856d-112">Filter merit.</span></span> <span data-ttu-id="e856d-113">Usado pela interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) ao construir um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="e856d-113">Used by the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface when constructing a filter graph.</span></span> <span data-ttu-id="e856d-114">Para obter uma lista de valores de mérito, consulte [mérito](merit.md).</span><span class="sxs-lookup"><span data-stu-id="e856d-114">For a list of merit values, see [Merit](merit.md).</span></span>

</dd> <dt>

<span data-ttu-id="e856d-115">**nPins**</span><span class="sxs-lookup"><span data-stu-id="e856d-115">**nPins**</span></span>
</dt> <dd>

<span data-ttu-id="e856d-116">Número de elementos na matriz *lpPin* .</span><span class="sxs-lookup"><span data-stu-id="e856d-116">Number of elements in the *lpPin* array.</span></span> <span data-ttu-id="e856d-117">Se *lpPin* for **nulo**, defina esse membro como zero.</span><span class="sxs-lookup"><span data-stu-id="e856d-117">If *lpPin* is **NULL**, set this member to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e856d-118">**lpPin**</span><span class="sxs-lookup"><span data-stu-id="e856d-118">**lpPin**</span></span>
</dt> <dd>

<span data-ttu-id="e856d-119">Ponteiro para uma matriz de estruturas de [**\_ PIN AMOVIESETUP**](amoviesetup-pin.md) , de tamanho *nPins*.</span><span class="sxs-lookup"><span data-stu-id="e856d-119">Pointer to an array of [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structures, of size *nPins*.</span></span> <span data-ttu-id="e856d-120">Cada membro desta matriz descreve um PIN no filtro.</span><span class="sxs-lookup"><span data-stu-id="e856d-120">Each member of this array describes a pin on the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e856d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e856d-121">Remarks</span></span>

<span data-ttu-id="e856d-122">Para obter informações sobre como usar essa estrutura, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e856d-122">For information about using this structure, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="e856d-123">Use essa estrutura somente para filtros registrados na categoria de filtro padrão (CLSID \_ LegacyAmFilterCategory).</span><span class="sxs-lookup"><span data-stu-id="e856d-123">Use this structure only for filters that are registered in the default filter category (CLSID\_LegacyAmFilterCategory).</span></span> <span data-ttu-id="e856d-124">Para registrar um filtro em uma categoria diferente, use o método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , conforme descrito em [implementando DllRegisterServer](implementing-dllregisterserver.md).</span><span class="sxs-lookup"><span data-stu-id="e856d-124">To register a filter in a different category, use the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method, as described in [Implementing DllRegisterServer](implementing-dllregisterserver.md).</span></span>

> [!Note]  
> <span data-ttu-id="e856d-125">O arquivo de cabeçalho combase. h é fornecido com as [classes base do DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="e856d-125">The header file combase.h is provided with the [DirectShow Base Classes](directshow-base-classes.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e856d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e856d-126">Requirements</span></span>



| <span data-ttu-id="e856d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e856d-127">Requirement</span></span> | <span data-ttu-id="e856d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e856d-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e856d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e856d-129">Header</span></span><br/> | <dl> <span data-ttu-id="e856d-130"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e856d-130"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e856d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e856d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e856d-132">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e856d-132">DirectShow Structures</span></span>](directshow-structures.md)
</dt> </dl>

 

 




