---
title: Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)
description: Indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada. | Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Elemento EnableIdentityPrivacy EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298403"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a><span data-ttu-id="d72e2-105">Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)</span><span class="sxs-lookup"><span data-stu-id="d72e2-105">EnableIdentityPrivacy (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="d72e2-106">O elemento **EnableIdentityPrivacy (IdentityPrivacyParameters)** indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada.</span><span class="sxs-lookup"><span data-stu-id="d72e2-106">The **EnableIdentityPrivacy (IdentityPrivacyParameters)** element Indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="d72e2-107">O elemento **EnableIdentityPrivacy** é definido pelo [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d72e2-107">The **EnableIdentityPrivacy** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="d72e2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d72e2-108">Remarks</span></span>

<span data-ttu-id="d72e2-109">O elemento **EnableIdentityPrivacy** é opcional.</span><span class="sxs-lookup"><span data-stu-id="d72e2-109">The **EnableIdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d72e2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d72e2-110">Requirements</span></span>



| <span data-ttu-id="d72e2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d72e2-111">Requirement</span></span> | <span data-ttu-id="d72e2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d72e2-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d72e2-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d72e2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d72e2-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d72e2-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d72e2-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d72e2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d72e2-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d72e2-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d72e2-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d72e2-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="d72e2-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="d72e2-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d72e2-119">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="d72e2-119">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="d72e2-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="d72e2-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d72e2-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="d72e2-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="d72e2-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d72e2-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="d72e2-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="d72e2-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d72e2-124">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="d72e2-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d72e2-125">Elementos do esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="d72e2-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





