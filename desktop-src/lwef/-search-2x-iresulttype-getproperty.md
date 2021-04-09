---
title: Propriedade GetProperty IResultType (WdsSharedIDL. h)
description: Esta propriedade contém informações de propriedade especificadas.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- Propriedade GetProperty recursos de ambiente herdado do Windows
- Propriedade GetProperty recursos de ambiente herdados do Windows, interface IResultType
- Recursos do ambiente Windows herdado da interface IResultType, Propriedade GetProperty
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd62517e7db9fdc15841c443ba9010903ddea697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824309"
---
# <a name="iresulttypegetproperty-property"></a><span data-ttu-id="7cbb1-106">Propriedade IResultType:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="7cbb1-106">IResultType::GetProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="7cbb1-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7cbb1-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7cbb1-109">Esta propriedade contém informações de propriedade especificadas.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-109">This property contains specified property information.</span></span>

<span data-ttu-id="7cbb1-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbb1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cbb1-111">Syntax</span></span>


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a><span data-ttu-id="7cbb1-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7cbb1-112">Property value</span></span>

<span data-ttu-id="7cbb1-113">Define o endereço das informações de propriedade especificadas.</span><span class="sxs-lookup"><span data-stu-id="7cbb1-113">Sets the address of the specified property information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cbb1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cbb1-114">Requirements</span></span>



| <span data-ttu-id="7cbb1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cbb1-115">Requirement</span></span> | <span data-ttu-id="7cbb1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7cbb1-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbb1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cbb1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7cbb1-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="7cbb1-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7cbb1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cbb1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7cbb1-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="7cbb1-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7cbb1-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7cbb1-121">Redistributable</span></span><br/>          | <span data-ttu-id="7cbb1-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="7cbb1-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="7cbb1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cbb1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cbb1-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cbb1-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





