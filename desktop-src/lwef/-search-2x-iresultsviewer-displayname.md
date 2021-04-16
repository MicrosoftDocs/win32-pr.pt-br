---
title: Propriedade DisplayName IResultsViewer (WdsView. h)
description: Nome de exibição localizado do tipo.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- Propriedade DisplayName recursos de ambiente do Windows herdados
- Propriedade DisplayName recursos de ambiente do Windows herdados, interface IResultsViewer
- Recursos do ambiente Windows herdado da interface IResultsViewer, Propriedade DisplayName
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5ba65729fb238dbed57b71d893a9814c8ac8f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761061"
---
# <a name="iresultsviewerdisplayname-property"></a><span data-ttu-id="5a400-106">IResultsViewer::D Propriedade isplayname</span><span class="sxs-lookup"><span data-stu-id="5a400-106">IResultsViewer::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="5a400-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5a400-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="5a400-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5a400-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="5a400-109">Nome de exibição localizado do tipo.</span><span class="sxs-lookup"><span data-stu-id="5a400-109">Localized display name of the type.</span></span>

<span data-ttu-id="5a400-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5a400-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a400-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a400-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="5a400-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5a400-112">Property value</span></span>

<span data-ttu-id="5a400-113">Ponteiro para um valor que recebe o nome de exibição localizado para o tipo.</span><span class="sxs-lookup"><span data-stu-id="5a400-113">Pointer to a value that receives the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a400-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a400-114">Requirements</span></span>



| <span data-ttu-id="5a400-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a400-115">Requirement</span></span> | <span data-ttu-id="5a400-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5a400-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a400-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a400-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a400-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="5a400-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5a400-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a400-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a400-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="5a400-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="5a400-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5a400-121">Redistributable</span></span><br/>          | <span data-ttu-id="5a400-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="5a400-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="5a400-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a400-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a400-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a400-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





