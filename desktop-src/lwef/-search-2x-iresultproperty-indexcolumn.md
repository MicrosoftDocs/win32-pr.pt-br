---
title: Propriedade IResultProperty IndexColumn (WdsSharedIDL. h)
description: Nome da coluna de propriedades no índice.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Recursos do ambiente Windows herdado da propriedade IndexColumn
- Propriedade IndexColumn recursos de ambiente do Windows herdados, interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, Propriedade IndexColumn
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824310"
---
# <a name="iresultpropertyindexcolumn-property"></a><span data-ttu-id="7f829-106">Propriedade IResultProperty:: IndexColumn</span><span class="sxs-lookup"><span data-stu-id="7f829-106">IResultProperty::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="7f829-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7f829-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7f829-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7f829-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7f829-109">Nome da coluna de propriedades no índice.</span><span class="sxs-lookup"><span data-stu-id="7f829-109">Properties column name in the index.</span></span>

<span data-ttu-id="7f829-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7f829-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f829-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f829-111">Syntax</span></span>


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="7f829-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7f829-112">Property value</span></span>

<span data-ttu-id="7f829-113">Retorna um ponteiro para o nome da coluna no índice.</span><span class="sxs-lookup"><span data-stu-id="7f829-113">returns a pointer to the column name in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f829-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f829-114">Requirements</span></span>



| <span data-ttu-id="7f829-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f829-115">Requirement</span></span> | <span data-ttu-id="7f829-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7f829-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f829-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f829-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7f829-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="7f829-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7f829-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f829-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7f829-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="7f829-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7f829-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7f829-121">Redistributable</span></span><br/>          | <span data-ttu-id="7f829-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="7f829-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="7f829-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f829-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f829-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f829-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





