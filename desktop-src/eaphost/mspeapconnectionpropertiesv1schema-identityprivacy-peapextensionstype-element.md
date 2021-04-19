---
title: Elemento IdentityPrivacy (PeapExtensionsType) (v1)
description: Indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada. | Elemento IdentityPrivacy (PeapExtensionsType)
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 748cf3ae8d5a4da4f8885332a72326bced45b398
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389070"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="ed051-105">Elemento IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="ed051-105">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="ed051-106">O elemento **IdentityPrivacy (PeapExtensionsType)** indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada.</span><span class="sxs-lookup"><span data-stu-id="ed051-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="ed051-107">O elemento é definido pelo elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ed051-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed051-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed051-108">Remarks</span></span>

<span data-ttu-id="ed051-109">O elemento **IdentityPrivacy** é opcional.</span><span class="sxs-lookup"><span data-stu-id="ed051-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed051-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed051-110">Requirements</span></span>



| <span data-ttu-id="ed051-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed051-111">Requirement</span></span> | <span data-ttu-id="ed051-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ed051-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ed051-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed051-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ed051-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ed051-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ed051-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed051-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ed051-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ed051-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed051-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed051-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed051-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="ed051-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ed051-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="ed051-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="ed051-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="ed051-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ed051-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="ed051-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="ed051-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ed051-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ed051-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="ed051-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ed051-124">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ed051-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ed051-125">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ed051-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ed051-126">**IdentityPrivacy(PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="ed051-126">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





