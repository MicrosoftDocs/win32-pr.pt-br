---
title: Propriedade IPropertyFilter LogicOperator (WdsSharedIDL. h)
description: Operador lógico a ser usado ao aplicar um filtro.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Recursos do ambiente Windows herdado da propriedade LogicOperator
- Propriedade LogicOperator recursos de ambiente do Windows herdados, interface IPropertyFilter
- Recursos do ambiente Windows herdado da interface IPropertyFilter, Propriedade LogicOperator
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c514ae6231a9d83063b4a294680bdd3949c91102
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455965"
---
# <a name="ipropertyfilterlogicoperator-property"></a><span data-ttu-id="70c65-106">Propriedade IPropertyFilter:: LogicOperator</span><span class="sxs-lookup"><span data-stu-id="70c65-106">IPropertyFilter::LogicOperator property</span></span>

> [!NOTE]
> <span data-ttu-id="70c65-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70c65-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="70c65-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="70c65-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="70c65-109">Operador lógico a ser usado ao aplicar um filtro.</span><span class="sxs-lookup"><span data-stu-id="70c65-109">Logic Operator to use when applying a filter.</span></span>

<span data-ttu-id="70c65-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="70c65-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c65-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="70c65-111">Syntax</span></span>


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a><span data-ttu-id="70c65-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="70c65-112">Property value</span></span>

<span data-ttu-id="70c65-113">Define o tipo de operador lógico.</span><span class="sxs-lookup"><span data-stu-id="70c65-113">Sets the logic operator type.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c65-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70c65-114">Requirements</span></span>



| <span data-ttu-id="70c65-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c65-115">Requirement</span></span> | <span data-ttu-id="70c65-116">Valor</span><span class="sxs-lookup"><span data-stu-id="70c65-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="70c65-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70c65-117">Minimum supported client</span></span><br/> | <span data-ttu-id="70c65-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="70c65-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="70c65-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70c65-119">Minimum supported server</span></span><br/> | <span data-ttu-id="70c65-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="70c65-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="70c65-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="70c65-121">Redistributable</span></span><br/>          | <span data-ttu-id="70c65-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="70c65-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="70c65-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70c65-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c65-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c65-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





