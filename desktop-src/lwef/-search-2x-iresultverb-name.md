---
title: Propriedade nome do IResultVerb (WdsSharedIDL. h)
description: Essa propriedade retorna um ponteiro para o nome do cononical para o verbo, como Print, Open etc.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Propriedade de nome recursos de ambiente do Windows herdados
- Propriedade de nome recursos de ambiente do Windows herdados, interface IResultVerb
- Recursos do ambiente Windows herdado da interface IResultVerb, Propriedade Name
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918044"
---
# <a name="iresultverbname-property"></a><span data-ttu-id="5d307-106">Propriedade IResultVerb:: Name</span><span class="sxs-lookup"><span data-stu-id="5d307-106">IResultVerb::Name property</span></span>

> [!NOTE]
> <span data-ttu-id="5d307-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5d307-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="5d307-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5d307-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="5d307-109">Essa propriedade retorna um ponteiro para o nome do cononical para o verbo, como Print, Open etc.</span><span class="sxs-lookup"><span data-stu-id="5d307-109">This property returns a pointer to the cononical name for the verb such as print, open, etc.</span></span>

<span data-ttu-id="5d307-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5d307-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d307-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d307-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="5d307-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5d307-112">Property value</span></span>

<span data-ttu-id="5d307-113">Name é um ponteiro para o nome do cononical para o verbo.</span><span class="sxs-lookup"><span data-stu-id="5d307-113">name is a pointer to the cononical name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d307-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d307-114">Requirements</span></span>



| <span data-ttu-id="5d307-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d307-115">Requirement</span></span> | <span data-ttu-id="5d307-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5d307-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d307-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d307-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5d307-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="5d307-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5d307-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d307-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5d307-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="5d307-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d307-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5d307-121">Redistributable</span></span><br/>          | <span data-ttu-id="5d307-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="5d307-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="5d307-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d307-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d307-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d307-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





