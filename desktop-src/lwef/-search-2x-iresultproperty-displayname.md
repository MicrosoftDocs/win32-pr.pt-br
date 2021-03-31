---
title: Propriedade DisplayName IResultProperty (WdsSharedIDL. h)
description: Nome de exibição localizado da propriedade.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Propriedade DisplayName recursos de ambiente do Windows herdados
- Propriedade DisplayName recursos de ambiente do Windows herdados, interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, Propriedade DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085847"
---
# <a name="iresultpropertydisplayname-property"></a><span data-ttu-id="2814c-106">IResultProperty::D Propriedade isplayname</span><span class="sxs-lookup"><span data-stu-id="2814c-106">IResultProperty::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="2814c-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2814c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2814c-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2814c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="2814c-109">Nome de exibição localizado da propriedade.</span><span class="sxs-lookup"><span data-stu-id="2814c-109">Localized display name of the property.</span></span>

<span data-ttu-id="2814c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2814c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2814c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2814c-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="2814c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2814c-112">Property value</span></span>

<span data-ttu-id="2814c-113">Retorna um ponteiro para o nome de exibição localizado.</span><span class="sxs-lookup"><span data-stu-id="2814c-113">returns a pointer to the localized display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="2814c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2814c-114">Requirements</span></span>



| <span data-ttu-id="2814c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2814c-115">Requirement</span></span> | <span data-ttu-id="2814c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2814c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2814c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2814c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2814c-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="2814c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2814c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2814c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2814c-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="2814c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2814c-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2814c-121">Redistributable</span></span><br/>          | <span data-ttu-id="2814c-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="2814c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="2814c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2814c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2814c-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2814c-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





