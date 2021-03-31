---
title: Propriedade Count de IPropertyFilterCollection (WdsSharedIDL. h)
description: Número de filtros na coleção.
ms.assetid: 9d656f06-eb1d-4cc6-9096-252f0fc65ae2
keywords:
- Propriedade de contagem recursos de ambiente do Windows herdados
- Propriedade de contagem recursos de ambiente do Windows herdados, interface IPropertyFilterCollection
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.Count
- IPropertyFilterCollection.get_Count
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258a2ca8089cecb8e2e15fbe7e9e92ce1ed3468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644536"
---
# <a name="ipropertyfiltercollectioncount-property"></a><span data-ttu-id="362e4-106">Propriedade IPropertyFilterCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="362e4-106">IPropertyFilterCollection::Count property</span></span>

> [!NOTE]
> <span data-ttu-id="362e4-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="362e4-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="362e4-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="362e4-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="362e4-109">Número de filtros na coleção.</span><span class="sxs-lookup"><span data-stu-id="362e4-109">Number of filters in the collection.</span></span>

<span data-ttu-id="362e4-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="362e4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="362e4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="362e4-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="362e4-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="362e4-112">Property value</span></span>

<span data-ttu-id="362e4-113">Retorna um ponteiro para o número de filtros na coleção.</span><span class="sxs-lookup"><span data-stu-id="362e4-113">returns a pointer to the number of filters in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="362e4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="362e4-114">Requirements</span></span>



| <span data-ttu-id="362e4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="362e4-115">Requirement</span></span> | <span data-ttu-id="362e4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="362e4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="362e4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="362e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="362e4-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="362e4-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="362e4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="362e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="362e4-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="362e4-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="362e4-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="362e4-121">Redistributable</span></span><br/>          | <span data-ttu-id="362e4-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="362e4-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="362e4-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="362e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="362e4-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="362e4-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





