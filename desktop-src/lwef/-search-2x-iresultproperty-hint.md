---
title: Propriedade de dica IResultProperty (WdsSharedIDL. h)
description: Valor especial usado para auxiliar a recuperação de dados.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Propriedades de dica recursos de ambiente do Windows herdados
- Propriedade Hint recursos de ambiente herdados do Windows, interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, Propriedade Hint
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105807147"
---
# <a name="iresultpropertyhint-property"></a><span data-ttu-id="bcb9c-106">Propriedade IResultProperty:: Hint</span><span class="sxs-lookup"><span data-stu-id="bcb9c-106">IResultProperty::Hint property</span></span>

> [!NOTE]
> <span data-ttu-id="bcb9c-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bcb9c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="bcb9c-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="bcb9c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="bcb9c-109">Valor especial usado para auxiliar a recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="bcb9c-109">Special value used to aid data retrieval.</span></span>

<span data-ttu-id="bcb9c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="bcb9c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb9c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcb9c-111">Syntax</span></span>


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a><span data-ttu-id="bcb9c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bcb9c-112">Property value</span></span>

<span data-ttu-id="bcb9c-113">Retorna um ponteiro para a dica.</span><span class="sxs-lookup"><span data-stu-id="bcb9c-113">returns a pointer to the hint.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb9c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcb9c-114">Requirements</span></span>



| <span data-ttu-id="bcb9c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb9c-115">Requirement</span></span> | <span data-ttu-id="bcb9c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb9c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb9c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcb9c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb9c-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="bcb9c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bcb9c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcb9c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb9c-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="bcb9c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bcb9c-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="bcb9c-121">Redistributable</span></span><br/>          | <span data-ttu-id="bcb9c-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="bcb9c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="bcb9c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bcb9c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcb9c-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9c-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





