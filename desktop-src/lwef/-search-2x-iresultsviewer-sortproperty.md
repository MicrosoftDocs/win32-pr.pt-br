---
title: Propriedade SortProperty IResultsViewer (WdsView. h)
description: Essa propriedade irá definir ou retornar o IndexColumn da propriedade para classificar os resultados por.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Recursos de ambiente herdado do Windows da propriedade SortProperty
- Propriedade SortProperty recursos de ambiente herdados do Windows, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade SortProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824374"
---
# <a name="iresultsviewersortproperty-property"></a><span data-ttu-id="6d80e-106">Propriedade IResultsViewer:: SortProperty</span><span class="sxs-lookup"><span data-stu-id="6d80e-106">IResultsViewer::SortProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="6d80e-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6d80e-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6d80e-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6d80e-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6d80e-109">Essa propriedade irá definir ou retornar o IndexColumn da propriedade para classificar os resultados por.</span><span class="sxs-lookup"><span data-stu-id="6d80e-109">This property will set or return the IndexColumn of the property to sort results by.</span></span>

<span data-ttu-id="6d80e-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6d80e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d80e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d80e-111">Syntax</span></span>


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="6d80e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6d80e-112">Property value</span></span>

<span data-ttu-id="6d80e-113">Define a propriedade IndexColumn.</span><span class="sxs-lookup"><span data-stu-id="6d80e-113">Sets the IndexColumn property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d80e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d80e-114">Requirements</span></span>



| <span data-ttu-id="6d80e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d80e-115">Requirement</span></span> | <span data-ttu-id="6d80e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6d80e-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6d80e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d80e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d80e-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="6d80e-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6d80e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d80e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d80e-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="6d80e-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="6d80e-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6d80e-121">Redistributable</span></span><br/>          | <span data-ttu-id="6d80e-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="6d80e-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="6d80e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d80e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d80e-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d80e-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





