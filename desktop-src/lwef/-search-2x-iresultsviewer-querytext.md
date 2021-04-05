---
title: Propriedade IResultsViewer QueryText (WdsView. h)
description: Obtém ou define o texto da consulta atual.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Recursos do ambiente Windows herdado da propriedade QueryText
- Propriedade QueryText recursos de ambiente do Windows herdados, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade QueryText
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98450114ad64ec0209b14041b8f2516dc6884b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086256"
---
# <a name="iresultsviewerquerytext-property"></a><span data-ttu-id="6fdb2-106">Propriedade IResultsViewer:: QueryText</span><span class="sxs-lookup"><span data-stu-id="6fdb2-106">IResultsViewer::QueryText property</span></span>

> [!NOTE]
> <span data-ttu-id="6fdb2-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6fdb2-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6fdb2-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6fdb2-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6fdb2-109">Obtém ou define o texto da consulta atual.</span><span class="sxs-lookup"><span data-stu-id="6fdb2-109">Gets or sets the current query text.</span></span>

<span data-ttu-id="6fdb2-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6fdb2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdb2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fdb2-111">Syntax</span></span>


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a><span data-ttu-id="6fdb2-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6fdb2-112">Property value</span></span>

<span data-ttu-id="6fdb2-113">Define o texto da consulta atual.</span><span class="sxs-lookup"><span data-stu-id="6fdb2-113">Sets the current query text.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fdb2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fdb2-114">Requirements</span></span>



| <span data-ttu-id="6fdb2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fdb2-115">Requirement</span></span> | <span data-ttu-id="6fdb2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6fdb2-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdb2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fdb2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6fdb2-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="6fdb2-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6fdb2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fdb2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6fdb2-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="6fdb2-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="6fdb2-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6fdb2-121">Redistributable</span></span><br/>          | <span data-ttu-id="6fdb2-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="6fdb2-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="6fdb2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fdb2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fdb2-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fdb2-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





