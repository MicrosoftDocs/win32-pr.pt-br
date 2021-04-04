---
title: Propriedade IResultType PreceivedType (WdsSharedIDL. h)
description: Essa propriedade contém a cadeia de caracteres usada para identificar o tipo no índice.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Recursos do ambiente Windows herdado da propriedade PreceivedType
- Propriedade PreceivedType recursos de ambiente do Windows herdados, interface IResultType
- Recursos do ambiente Windows herdado da interface IResultType, Propriedade PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824308"
---
# <a name="iresulttypepreceivedtype-property"></a><span data-ttu-id="54f9e-106">IResultType::P Propriedade ReceivedType</span><span class="sxs-lookup"><span data-stu-id="54f9e-106">IResultType::PreceivedType property</span></span>

> [!NOTE]
> <span data-ttu-id="54f9e-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="54f9e-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="54f9e-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="54f9e-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="54f9e-109">Essa propriedade contém a cadeia de caracteres usada para identificar o tipo no índice.</span><span class="sxs-lookup"><span data-stu-id="54f9e-109">This property contains the string used to identify the type in the index.</span></span>

<span data-ttu-id="54f9e-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="54f9e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54f9e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54f9e-111">Syntax</span></span>


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="54f9e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="54f9e-112">Property value</span></span>

<span data-ttu-id="54f9e-113">Retorna o endereço da cadeia de caracteres identifyint o tipo no índice.</span><span class="sxs-lookup"><span data-stu-id="54f9e-113">returns the address of the string identifyint the type in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="54f9e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54f9e-114">Requirements</span></span>



| <span data-ttu-id="54f9e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="54f9e-115">Requirement</span></span> | <span data-ttu-id="54f9e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="54f9e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f9e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54f9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54f9e-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="54f9e-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="54f9e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54f9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54f9e-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="54f9e-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="54f9e-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="54f9e-121">Redistributable</span></span><br/>          | <span data-ttu-id="54f9e-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="54f9e-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="54f9e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54f9e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="54f9e-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="54f9e-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





