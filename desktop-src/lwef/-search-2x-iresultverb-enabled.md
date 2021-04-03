---
title: Propriedade habilitada para IResultVerb (WdsSharedIDL. h)
description: Essa propriedade retornará TRUE se o verbo estiver habilitado.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Propriedade habilitada recursos de ambiente do Windows herdado
- Propriedade habilitada recursos de ambiente Windows herdados, interface IResultVerb
- Recursos do ambiente Windows herdado da interface IResultVerb, Propriedade Enabled
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8570e7bbb06843467080dd0dd748391234f259d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918721"
---
# <a name="iresultverbenabled-property"></a><span data-ttu-id="6b834-106">Propriedade IResultVerb:: Enabled</span><span class="sxs-lookup"><span data-stu-id="6b834-106">IResultVerb::Enabled property</span></span>

> [!NOTE]
> <span data-ttu-id="6b834-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6b834-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6b834-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6b834-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6b834-109">Essa propriedade retornará TRUE se o verbo estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="6b834-109">This property returns TRUE if the verb is enabled.</span></span>

<span data-ttu-id="6b834-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6b834-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b834-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b834-111">Syntax</span></span>


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a><span data-ttu-id="6b834-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6b834-112">Property value</span></span>

<span data-ttu-id="6b834-113">Essa propriedade retornará true se o verbo estiver habilitado ou false se não.</span><span class="sxs-lookup"><span data-stu-id="6b834-113">This property returns True if the verb is enabled or False if not.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b834-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b834-114">Requirements</span></span>



| <span data-ttu-id="6b834-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b834-115">Requirement</span></span> | <span data-ttu-id="6b834-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6b834-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b834-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b834-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6b834-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="6b834-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6b834-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b834-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6b834-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="6b834-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b834-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6b834-121">Redistributable</span></span><br/>          | <span data-ttu-id="6b834-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="6b834-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="6b834-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b834-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b834-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b834-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





