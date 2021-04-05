---
title: Propriedade UID IResultType (WdsSharedIDL. h)
description: Essa propriedade contém o identificador exclusivo para o tipo.
ms.assetid: 31c2ef7d-f5a7-441e-80ea-fd7e46fded07
keywords:
- Propriedade UID recursos de ambiente herdados do Windows
- Propriedade UID recursos de ambiente herdados do Windows, interface IResultType
- Recursos do ambiente Windows herdado da interface IResultType, Propriedade UID
topic_type:
- apiref
api_name:
- IResultType.UID
- IResultType.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbdd5a9b17da9cde04ac0b371a885b07415d0e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086430"
---
# <a name="iresulttypeuid-property"></a><span data-ttu-id="11f60-106">Propriedade IResultType:: UID</span><span class="sxs-lookup"><span data-stu-id="11f60-106">IResultType::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="11f60-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="11f60-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="11f60-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="11f60-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="11f60-109">Essa propriedade contém o identificador exclusivo para o tipo.</span><span class="sxs-lookup"><span data-stu-id="11f60-109">This property contains the unique identifier for the type.</span></span>

<span data-ttu-id="11f60-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="11f60-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f60-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11f60-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="11f60-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="11f60-112">Property value</span></span>

<span data-ttu-id="11f60-113">o endereço do local que contém a UID.</span><span class="sxs-lookup"><span data-stu-id="11f60-113">the address of the location containing the uid.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f60-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11f60-114">Requirements</span></span>



| <span data-ttu-id="11f60-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="11f60-115">Requirement</span></span> | <span data-ttu-id="11f60-116">Valor</span><span class="sxs-lookup"><span data-stu-id="11f60-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f60-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11f60-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11f60-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="11f60-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="11f60-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11f60-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11f60-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="11f60-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="11f60-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="11f60-121">Redistributable</span></span><br/>          | <span data-ttu-id="11f60-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="11f60-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="11f60-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11f60-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f60-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="11f60-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





