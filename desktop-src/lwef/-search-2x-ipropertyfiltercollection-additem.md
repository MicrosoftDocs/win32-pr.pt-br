---
title: Propriedade AddItem IPropertyFilterCollection (WdsSharedIDL. h)
description: Adiciona um novo filtro à coleção.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- Recursos do ambiente Windows herdado da propriedade AddItem
- Propriedade AddItem recursos de ambiente do Windows herdados, interface IPropertyFilterCollection
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection, Propriedade AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009224"
---
# <a name="ipropertyfiltercollectionadditem-property"></a><span data-ttu-id="9cfa0-106">Propriedade IPropertyFilterCollection:: AddItem</span><span class="sxs-lookup"><span data-stu-id="9cfa0-106">IPropertyFilterCollection::AddItem property</span></span>

> [!NOTE]
> <span data-ttu-id="9cfa0-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9cfa0-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9cfa0-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9cfa0-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9cfa0-109">Adiciona um novo filtro à coleção.</span><span class="sxs-lookup"><span data-stu-id="9cfa0-109">Adds a new filter to the collection.</span></span>

<span data-ttu-id="9cfa0-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9cfa0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cfa0-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cfa0-111">Syntax</span></span>


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="9cfa0-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9cfa0-112">Property value</span></span>

<span data-ttu-id="9cfa0-113">Retorna um ponteiro para o endereço do novo filtro.</span><span class="sxs-lookup"><span data-stu-id="9cfa0-113">returns a pointer to the address for the new filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cfa0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cfa0-114">Requirements</span></span>



| <span data-ttu-id="9cfa0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cfa0-115">Requirement</span></span> | <span data-ttu-id="9cfa0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9cfa0-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cfa0-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cfa0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9cfa0-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="9cfa0-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9cfa0-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cfa0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9cfa0-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="9cfa0-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9cfa0-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9cfa0-121">Redistributable</span></span><br/>          | <span data-ttu-id="9cfa0-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="9cfa0-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9cfa0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cfa0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cfa0-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cfa0-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





