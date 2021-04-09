---
title: Propriedade UID IResultProperty (WdsSharedIDL. h)
description: Identificador exclusivo da propriedade.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- Propriedade UID recursos de ambiente herdados do Windows
- Propriedade UID recursos de ambiente herdados do Windows, interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, Propriedade UID
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009223"
---
# <a name="iresultpropertyuid-property"></a><span data-ttu-id="e97c6-106">Propriedade IResultProperty:: UID</span><span class="sxs-lookup"><span data-stu-id="e97c6-106">IResultProperty::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="e97c6-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e97c6-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e97c6-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e97c6-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e97c6-109">Identificador exclusivo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e97c6-109">Unique identifier for the property.</span></span>

<span data-ttu-id="e97c6-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e97c6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e97c6-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e97c6-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="e97c6-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e97c6-112">Property value</span></span>

<span data-ttu-id="e97c6-113">Retorna um ponteiro para o identificador de propriedade exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e97c6-113">returns a pointer to the unique property identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="e97c6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e97c6-114">Requirements</span></span>



| <span data-ttu-id="e97c6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e97c6-115">Requirement</span></span> | <span data-ttu-id="e97c6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e97c6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e97c6-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e97c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e97c6-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="e97c6-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e97c6-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e97c6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e97c6-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="e97c6-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e97c6-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e97c6-121">Redistributable</span></span><br/>          | <span data-ttu-id="e97c6-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="e97c6-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="e97c6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e97c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e97c6-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e97c6-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





