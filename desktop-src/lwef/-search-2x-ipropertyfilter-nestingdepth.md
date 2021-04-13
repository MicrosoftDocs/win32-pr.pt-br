---
title: Propriedade IPropertyFilter NestingDepth (WdsSharedIDL. h)
description: Profundidade de filtros em um conjunto aninhado de parênteses.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Recursos do ambiente Windows herdado da propriedade NestingDepth
- Propriedade NestingDepth recursos de ambiente do Windows herdados, interface IPropertyFilter
- Recursos do ambiente Windows herdado da interface IPropertyFilter, Propriedade NestingDepth
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369589"
---
# <a name="ipropertyfilternestingdepth-property"></a><span data-ttu-id="7dc29-106">Propriedade IPropertyFilter:: NestingDepth</span><span class="sxs-lookup"><span data-stu-id="7dc29-106">IPropertyFilter::NestingDepth property</span></span>

> [!NOTE]
> <span data-ttu-id="7dc29-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7dc29-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7dc29-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7dc29-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7dc29-109">Profundidade de filtros em um conjunto aninhado de parênteses.</span><span class="sxs-lookup"><span data-stu-id="7dc29-109">Filters depth within a nested set of parentheses.</span></span>

<span data-ttu-id="7dc29-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7dc29-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc29-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dc29-111">Syntax</span></span>


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a><span data-ttu-id="7dc29-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7dc29-112">Property value</span></span>

<span data-ttu-id="7dc29-113">Define o número que indica a profundidade de parênteses aninhados.</span><span class="sxs-lookup"><span data-stu-id="7dc29-113">Sets the number indicating the depth of nested parentheses.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc29-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dc29-114">Requirements</span></span>



| <span data-ttu-id="7dc29-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dc29-115">Requirement</span></span> | <span data-ttu-id="7dc29-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7dc29-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc29-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dc29-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc29-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="7dc29-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7dc29-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dc29-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc29-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="7dc29-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7dc29-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7dc29-121">Redistributable</span></span><br/>          | <span data-ttu-id="7dc29-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="7dc29-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="7dc29-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7dc29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc29-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc29-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





