---
title: Propriedade DisplayName IResultVerb (WdsSharedIDL. h)
description: Essa propriedade retorna um ponteiro para o nome de exibição localizado para o verbo.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Propriedade DisplayName recursos de ambiente do Windows herdados
- Propriedade DisplayName recursos de ambiente do Windows herdados, interface IResultVerb
- Recursos do ambiente Windows herdado da interface IResultVerb, Propriedade DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009221"
---
# <a name="iresultverbdisplayname-property"></a><span data-ttu-id="1d5f4-106">IResultVerb::D Propriedade isplayname</span><span class="sxs-lookup"><span data-stu-id="1d5f4-106">IResultVerb::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="1d5f4-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="1d5f4-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="1d5f4-109">Essa propriedade retorna um ponteiro para o nome de exibição localizado para o verbo.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-109">This property returns a pointer to the localized display name for the verb.</span></span>

<span data-ttu-id="1d5f4-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5f4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d5f4-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a><span data-ttu-id="1d5f4-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1d5f4-112">Property value</span></span>

<span data-ttu-id="1d5f4-113">Essa propriedade retorna um ponteiro para o nome de exibição localizado para o verbo.</span><span class="sxs-lookup"><span data-stu-id="1d5f4-113">This property returns a pointer to the localized display name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5f4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d5f4-114">Requirements</span></span>



| <span data-ttu-id="1d5f4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d5f4-115">Requirement</span></span> | <span data-ttu-id="1d5f4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1d5f4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5f4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d5f4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d5f4-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="1d5f4-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1d5f4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d5f4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d5f4-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="1d5f4-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1d5f4-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="1d5f4-121">Redistributable</span></span><br/>          | <span data-ttu-id="1d5f4-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="1d5f4-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="1d5f4-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d5f4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d5f4-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d5f4-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





