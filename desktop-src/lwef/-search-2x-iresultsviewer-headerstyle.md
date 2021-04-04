---
title: Propriedade IResultsViewer HeaderStyle (WdsView. h)
description: O estilo do cabeçalho exibido na exibição.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Recursos do ambiente Windows herdado da propriedade HeaderStyle
- Propriedade HeaderStyle recursos de ambiente do Windows herdados, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, propriedade HeaderStyle
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644673"
---
# <a name="iresultsviewerheaderstyle-property"></a><span data-ttu-id="5da3f-106">Propriedade IResultsViewer:: HeaderStyle</span><span class="sxs-lookup"><span data-stu-id="5da3f-106">IResultsViewer::HeaderStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="5da3f-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5da3f-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="5da3f-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5da3f-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="5da3f-109">O estilo do cabeçalho exibido na exibição.</span><span class="sxs-lookup"><span data-stu-id="5da3f-109">The style of header displayed in the view.</span></span>

<span data-ttu-id="5da3f-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5da3f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da3f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5da3f-111">Syntax</span></span>


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="5da3f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5da3f-112">Property value</span></span>

<span data-ttu-id="5da3f-113">Define o estilo do cabeçalho exibido.</span><span class="sxs-lookup"><span data-stu-id="5da3f-113">Sets the style of the header displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da3f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5da3f-114">Requirements</span></span>



| <span data-ttu-id="5da3f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5da3f-115">Requirement</span></span> | <span data-ttu-id="5da3f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5da3f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5da3f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5da3f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5da3f-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="5da3f-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5da3f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5da3f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5da3f-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="5da3f-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="5da3f-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5da3f-121">Redistributable</span></span><br/>          | <span data-ttu-id="5da3f-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="5da3f-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="5da3f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5da3f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5da3f-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="5da3f-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





