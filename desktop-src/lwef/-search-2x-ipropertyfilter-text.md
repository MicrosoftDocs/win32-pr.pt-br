---
title: Propriedade Text de IPropertyFilter (WdsSharedIDL. h)
description: Texto do filtro.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- Propriedade de texto recursos de ambiente herdados do Windows
- Propriedade de texto recursos de ambiente herdados do Windows, interface IPropertyFilter
- Recursos de ambiente do Windows herdados da interface IPropertyFilter, propriedade Text
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b30614f63cbcd766ca843f1b793632502f8e114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499553"
---
# <a name="ipropertyfiltertext-property"></a><span data-ttu-id="57a80-106">Propriedade IPropertyFilter:: Text</span><span class="sxs-lookup"><span data-stu-id="57a80-106">IPropertyFilter::Text property</span></span>

> [!NOTE]
> <span data-ttu-id="57a80-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="57a80-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="57a80-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="57a80-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="57a80-109">Texto do filtro.</span><span class="sxs-lookup"><span data-stu-id="57a80-109">Text of the filter.</span></span>

<span data-ttu-id="57a80-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="57a80-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a80-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="57a80-111">Syntax</span></span>


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="57a80-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="57a80-112">Property value</span></span>

<span data-ttu-id="57a80-113">Define o texto do filtro.</span><span class="sxs-lookup"><span data-stu-id="57a80-113">Sets the filter text.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a80-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a80-114">Requirements</span></span>



| <span data-ttu-id="57a80-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a80-115">Requirement</span></span> | <span data-ttu-id="57a80-116">Valor</span><span class="sxs-lookup"><span data-stu-id="57a80-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a80-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57a80-117">Minimum supported client</span></span><br/> | <span data-ttu-id="57a80-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="57a80-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="57a80-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57a80-119">Minimum supported server</span></span><br/> | <span data-ttu-id="57a80-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="57a80-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="57a80-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="57a80-121">Redistributable</span></span><br/>          | <span data-ttu-id="57a80-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="57a80-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="57a80-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57a80-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a80-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="57a80-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





