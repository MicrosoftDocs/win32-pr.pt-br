---
title: Elemento IdentityPrivacy (PeapExtensionsType) (v1)
description: O elemento IdentityPrivacy (PeapExtensionsType) indica se a identidade verdadeira de um usuário é enviada no esquema mspeapconnectionpropertiesv1.
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
ms.openlocfilehash: 7195ce43fb3f1a1f1710fe7aee3f5f74e18f3786
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989211"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="a3a5f-104">Elemento IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="a3a5f-104">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="a3a5f-105">O **elemento IdentityPrivacy (PeapExtensionsType)** indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada.</span><span class="sxs-lookup"><span data-stu-id="a3a5f-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="a3a5f-106">O elemento é definido pelo [**elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="a3a5f-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3a5f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3a5f-107">Remarks</span></span>

<span data-ttu-id="a3a5f-108">O **elemento IdentityPrivacy** é opcional.</span><span class="sxs-lookup"><span data-stu-id="a3a5f-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a5f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3a5f-109">Requirements</span></span>



| <span data-ttu-id="a3a5f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3a5f-110">Requirement</span></span> | <span data-ttu-id="a3a5f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a3a5f-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a3a5f-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3a5f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a5f-113">Somente aplicativos \[ da área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a3a5f-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a3a5f-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3a5f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a5f-115">Somente aplicativos da área de trabalho do Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="a3a5f-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3a5f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3a5f-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3a5f-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a3a5f-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a3a5f-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="a3a5f-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="a3a5f-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a3a5f-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a3a5f-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="a3a5f-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="a3a5f-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a3a5f-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="a3a5f-122">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="a3a5f-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a3a5f-123">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a3a5f-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="a3a5f-124">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a3a5f-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a3a5f-125">**IdentityPrivacy(PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="a3a5f-125">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





