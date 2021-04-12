---
title: Propriedade UID IPropertyFilter (WdsSharedIDL. h)
description: UID da propriedade a ser filtrada.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- Propriedade UID recursos de ambiente herdados do Windows
- Propriedade UID recursos de ambiente herdados do Windows, interface IPropertyFilter
- Recursos do ambiente Windows herdado da interface IPropertyFilter, Propriedade UID
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295828"
---
# <a name="ipropertyfilteruid-property"></a><span data-ttu-id="6e82b-106">Propriedade IPropertyFilter:: UID</span><span class="sxs-lookup"><span data-stu-id="6e82b-106">IPropertyFilter::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="6e82b-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6e82b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6e82b-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6e82b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6e82b-109">UID da propriedade a ser filtrada.</span><span class="sxs-lookup"><span data-stu-id="6e82b-109">UID for the property to filter by.</span></span>

<span data-ttu-id="6e82b-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6e82b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e82b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e82b-111">Syntax</span></span>


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="6e82b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e82b-112">Property value</span></span>

<span data-ttu-id="6e82b-113">Define a propriedade UID.</span><span class="sxs-lookup"><span data-stu-id="6e82b-113">Sets the UID property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e82b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e82b-114">Requirements</span></span>



| <span data-ttu-id="6e82b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e82b-115">Requirement</span></span> | <span data-ttu-id="6e82b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6e82b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e82b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e82b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e82b-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="6e82b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6e82b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e82b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e82b-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="6e82b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6e82b-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6e82b-121">Redistributable</span></span><br/>          | <span data-ttu-id="6e82b-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="6e82b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="6e82b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e82b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e82b-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e82b-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





