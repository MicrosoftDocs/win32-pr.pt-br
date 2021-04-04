---
title: Propriedade IPropertyFilterCollection GetITem (WdsSharedIDL. h)
description: Retorna um filtro específico dentro da coleção.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Recursos do ambiente Windows herdado da propriedade GetITem
- Propriedade GetITem recursos de ambiente do Windows herdados, interface IPropertyFilterCollection
- Recursos do ambiente Windows herdado da interface IPropertyFilterCollection, Propriedade GetITem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918298"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a><span data-ttu-id="39057-106">Propriedade IPropertyFilterCollection:: GetITem</span><span class="sxs-lookup"><span data-stu-id="39057-106">IPropertyFilterCollection::GetITem property</span></span>

> [!NOTE]
> <span data-ttu-id="39057-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="39057-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="39057-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="39057-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="39057-109">Retorna um filtro específico dentro da coleção.</span><span class="sxs-lookup"><span data-stu-id="39057-109">Returns a specific filter within the collection.</span></span>

<span data-ttu-id="39057-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="39057-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="39057-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="39057-111">Syntax</span></span>


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="39057-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="39057-112">Property value</span></span>

<span data-ttu-id="39057-113">Define o endereço do filtro.</span><span class="sxs-lookup"><span data-stu-id="39057-113">Sets the address of the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="39057-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39057-114">Requirements</span></span>



| <span data-ttu-id="39057-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="39057-115">Requirement</span></span> | <span data-ttu-id="39057-116">Valor</span><span class="sxs-lookup"><span data-stu-id="39057-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="39057-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39057-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39057-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="39057-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="39057-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39057-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39057-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="39057-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39057-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="39057-121">Redistributable</span></span><br/>          | <span data-ttu-id="39057-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="39057-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="39057-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39057-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39057-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39057-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





