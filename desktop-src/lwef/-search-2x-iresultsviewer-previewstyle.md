---
title: Propriedade PreviewStyle do IResultsViewer (WdsView. h)
description: Controla o modo de exibição do painel de visualização.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- Recursos de ambiente herdado do Windows da propriedade PreviewStyle
- Propriedade PreviewStyle recursos de ambiente herdados do Windows, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade PreviewStyle
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb3cb2cfd94d5cf1e93080259257bb27fa4f086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765334"
---
# <a name="iresultsviewerpreviewstyle-property"></a><span data-ttu-id="11f5b-106">IResultsViewer: Propriedade reviewstyle de:P</span><span class="sxs-lookup"><span data-stu-id="11f5b-106">IResultsViewer::PreviewStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="11f5b-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="11f5b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="11f5b-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="11f5b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="11f5b-109">Controla o modo de exibição do painel de visualização.</span><span class="sxs-lookup"><span data-stu-id="11f5b-109">Controls the preview pane's display mode.</span></span>

<span data-ttu-id="11f5b-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="11f5b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f5b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="11f5b-111">Syntax</span></span>


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="11f5b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="11f5b-112">Property value</span></span>

<span data-ttu-id="11f5b-113">Define a propriedade de estilo atual para o painel de visualização.</span><span class="sxs-lookup"><span data-stu-id="11f5b-113">Sets the current style property for the preview pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f5b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11f5b-114">Requirements</span></span>



| <span data-ttu-id="11f5b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="11f5b-115">Requirement</span></span> | <span data-ttu-id="11f5b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="11f5b-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="11f5b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11f5b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11f5b-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="11f5b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="11f5b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11f5b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11f5b-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="11f5b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="11f5b-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="11f5b-121">Redistributable</span></span><br/>          | <span data-ttu-id="11f5b-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="11f5b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="11f5b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11f5b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f5b-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="11f5b-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





