---
title: Propriedade HelpText IResultVerb (WdsSharedIDL. h)
description: Essa propriedade retorna um ponteiro para a cadeia de caracteres de ajuda localizada para o verbo.
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- Recursos de ambiente herdado do Windows da propriedade HelpText
- Propriedade HelpText recursos de ambiente do Windows herdados, interface IResultVerb
- Recursos do ambiente Windows herdado da interface IResultVerb, propriedade HelpText
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0615ea9cc62f3a5f207e7be2c2c4e80987239c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644533"
---
# <a name="iresultverbhelptext-property"></a><span data-ttu-id="a2b36-106">Propriedade IResultVerb:: HelpText</span><span class="sxs-lookup"><span data-stu-id="a2b36-106">IResultVerb::HelpText property</span></span>

> [!NOTE]
> <span data-ttu-id="a2b36-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a2b36-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a2b36-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a2b36-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a2b36-109">Essa propriedade retorna um ponteiro para a cadeia de caracteres de ajuda localizada para o verbo.</span><span class="sxs-lookup"><span data-stu-id="a2b36-109">This property returns a pointer to the localized help string for the verb.</span></span>

<span data-ttu-id="a2b36-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a2b36-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b36-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2b36-111">Syntax</span></span>


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="a2b36-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a2b36-112">Property value</span></span>

<span data-ttu-id="a2b36-113">O valor dessa propriedade é um ponteiro para a cadeia de caracteres de ajuda localizada para esse verbo.</span><span class="sxs-lookup"><span data-stu-id="a2b36-113">The value of this property is a pointer to the localized help string for this verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b36-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2b36-114">Requirements</span></span>



| <span data-ttu-id="a2b36-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2b36-115">Requirement</span></span> | <span data-ttu-id="a2b36-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a2b36-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b36-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2b36-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b36-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="a2b36-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a2b36-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2b36-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b36-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="a2b36-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a2b36-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a2b36-121">Redistributable</span></span><br/>          | <span data-ttu-id="a2b36-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="a2b36-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="a2b36-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2b36-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b36-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b36-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





