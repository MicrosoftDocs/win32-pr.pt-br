---
title: Propriedade IPropertyFilter IndexColumn (WdsSharedIDL. h)
description: Nome da coluna indexada da propriedade pela qual filtrar.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Recursos do ambiente Windows herdado da propriedade IndexColumn
- Propriedade IndexColumn recursos de ambiente do Windows herdados, interface IPropertyFilter
- Recursos do ambiente Windows herdado da interface IPropertyFilter, Propriedade IndexColumn
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009318"
---
# <a name="ipropertyfilterindexcolumn-property"></a><span data-ttu-id="29f73-106">Propriedade IPropertyFilter:: IndexColumn</span><span class="sxs-lookup"><span data-stu-id="29f73-106">IPropertyFilter::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="29f73-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="29f73-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="29f73-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="29f73-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="29f73-109">Nome da coluna indexada da propriedade pela qual filtrar.</span><span class="sxs-lookup"><span data-stu-id="29f73-109">Indexed column name of the property to filter by.</span></span>

<span data-ttu-id="29f73-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="29f73-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="29f73-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="29f73-111">Syntax</span></span>


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="29f73-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="29f73-112">Property value</span></span>

<span data-ttu-id="29f73-113">Define a propriedade da coluna.</span><span class="sxs-lookup"><span data-stu-id="29f73-113">Sets the Column property.</span></span>

## <a name="requirements"></a><span data-ttu-id="29f73-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29f73-114">Requirements</span></span>



| <span data-ttu-id="29f73-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29f73-115">Requirement</span></span> | <span data-ttu-id="29f73-116">Valor</span><span class="sxs-lookup"><span data-stu-id="29f73-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="29f73-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29f73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29f73-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="29f73-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="29f73-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29f73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29f73-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="29f73-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="29f73-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="29f73-121">Redistributable</span></span><br/>          | <span data-ttu-id="29f73-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="29f73-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="29f73-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29f73-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="29f73-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="29f73-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





