---
title: Propriedade IResultType PropertyCount (WdsSharedIDL. h)
description: Essa propriedade contém o número de propriedades expostas pelo tipo.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- Recursos do ambiente Windows herdado da propriedade PropertyCount
- Propriedade PropertyCount recursos de ambiente do Windows herdados, interface IResultType
- Recursos do ambiente Windows herdado da interface IResultType, Propriedade PropertyCount
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1804c0abd249d93470cb2570f5bd58c600e8d3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499245"
---
# <a name="iresulttypepropertycount-property"></a><span data-ttu-id="51e0d-106">IResultType: Propriedade ropertyCount de:P</span><span class="sxs-lookup"><span data-stu-id="51e0d-106">IResultType::PropertyCount property</span></span>

> [!NOTE]
> <span data-ttu-id="51e0d-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="51e0d-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="51e0d-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="51e0d-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="51e0d-109">Essa propriedade contém o número de propriedades expostas pelo tipo.</span><span class="sxs-lookup"><span data-stu-id="51e0d-109">This property contains the number of properties exposed by the type.</span></span>

<span data-ttu-id="51e0d-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="51e0d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e0d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51e0d-111">Syntax</span></span>


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="51e0d-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="51e0d-112">Property value</span></span>

<span data-ttu-id="51e0d-113">Retorna o endereço do número de propriedades expostas.</span><span class="sxs-lookup"><span data-stu-id="51e0d-113">returns the address of the number of properties exposed.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e0d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51e0d-114">Requirements</span></span>



| <span data-ttu-id="51e0d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="51e0d-115">Requirement</span></span> | <span data-ttu-id="51e0d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="51e0d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e0d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51e0d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="51e0d-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="51e0d-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="51e0d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51e0d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="51e0d-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="51e0d-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="51e0d-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="51e0d-121">Redistributable</span></span><br/>          | <span data-ttu-id="51e0d-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="51e0d-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="51e0d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51e0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e0d-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e0d-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





