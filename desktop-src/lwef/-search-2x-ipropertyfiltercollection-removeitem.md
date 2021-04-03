---
title: Propriedade RemoveItem IPropertyFilterCollection (WdsSharedIDL. h)
description: Remove um filtro específico para a coleção.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- Recursos de ambiente herdado do Windows da propriedade RemoveItem
- Propriedade RemoveItem recursos de ambiente do Windows herdados, interface IPropertyFilterCollection
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection, Propriedade RemoveItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644856"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a><span data-ttu-id="2dcef-106">Propriedade IPropertyFilterCollection:: RemoveItem</span><span class="sxs-lookup"><span data-stu-id="2dcef-106">IPropertyFilterCollection::RemoveItem property</span></span>

> [!NOTE]
> <span data-ttu-id="2dcef-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2dcef-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2dcef-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2dcef-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="2dcef-109">Remove um filtro específico para a coleção.</span><span class="sxs-lookup"><span data-stu-id="2dcef-109">Removes a specific filter to the collection.</span></span>

<span data-ttu-id="2dcef-110">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="2dcef-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dcef-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dcef-111">Syntax</span></span>


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a><span data-ttu-id="2dcef-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2dcef-112">Property value</span></span>

<span data-ttu-id="2dcef-113">Aceita um ponteiro para o índice do filtro a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2dcef-113">Accepts a pointer to the index for the filter to be removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dcef-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dcef-114">Requirements</span></span>



| <span data-ttu-id="2dcef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dcef-115">Requirement</span></span> | <span data-ttu-id="2dcef-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2dcef-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dcef-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dcef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2dcef-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="2dcef-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2dcef-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dcef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2dcef-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="2dcef-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2dcef-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2dcef-121">Redistributable</span></span><br/>          | <span data-ttu-id="2dcef-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="2dcef-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="2dcef-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2dcef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dcef-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dcef-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





