---
title: Elemento IdentityPrivacy (PeapExtensionsType)
description: Indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada. | Elemento IdentityPrivacy (PeapExtensionsType)
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Elemento IdentityPrivacy EAPHost
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
ms.openlocfilehash: 2701352ee0e192dfd2d33fc2647b9ec6df96dd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506391"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="1e7f4-105">O elemento IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="1e7f4-105">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="1e7f4-106">O elemento **IdentityPrivacy (PeapExtensionsType)** indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="1e7f4-107">O elemento **IdentityPrivacy** é definido pelo elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1e7f4-107">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e7f4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e7f4-108">Remarks</span></span>

<span data-ttu-id="1e7f4-109">O elemento **IdentityPrivacy** é opcional.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e7f4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e7f4-110">Requirements</span></span>



| <span data-ttu-id="1e7f4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e7f4-111">Requirement</span></span> | <span data-ttu-id="1e7f4-112">Valor</span><span class="sxs-lookup"><span data-stu-id="1e7f4-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1e7f4-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e7f4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1e7f4-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1e7f4-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1e7f4-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e7f4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1e7f4-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="1e7f4-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e7f4-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e7f4-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e7f4-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="1e7f4-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1e7f4-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="1e7f4-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="1e7f4-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="1e7f4-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1e7f4-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="1e7f4-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="1e7f4-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1e7f4-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="1e7f4-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="1e7f4-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1e7f4-124">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="1e7f4-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="1e7f4-125">Elementos do esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="1e7f4-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





