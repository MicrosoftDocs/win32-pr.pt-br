---
title: Tipo complexo PeapExtensionsType
description: Contém aprimoramentos de esquema feitos no Windows 7. Futuros aprimoramentos de esquema serão tratados pelo PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- PeapExtensionsType tipo complexo EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644985"
---
# <a name="peapextensionstype-complex-type"></a><span data-ttu-id="4c4d7-105">Tipo complexo PeapExtensionsType</span><span class="sxs-lookup"><span data-stu-id="4c4d7-105">PeapExtensionsType Complex Type</span></span>

<span data-ttu-id="4c4d7-106">O tipo complexo **PeapExtensionsType** contém aprimoramentos de esquema feitos no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-106">The **PeapExtensionsType** complex type contains schema enhancements made in Windows 7.</span></span> <span data-ttu-id="4c4d7-107">Futuros aprimoramentos de esquema serão tratados pelo [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="4c4d7-107">Future schema enhancements will be handled by [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4c4d7-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4c4d7-108">Child elements</span></span>



| <span data-ttu-id="4c4d7-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="4c4d7-109">Element</span></span>                                                                                                                               | <span data-ttu-id="4c4d7-110">Type</span><span class="sxs-lookup"><span data-stu-id="4c4d7-110">Type</span></span> | <span data-ttu-id="4c4d7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c4d7-111">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c4d7-112">**extendedPeap:PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="4c4d7-112">**extendedPeap:PerformServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | <span data-ttu-id="4c4d7-113">Windows 7 e posterior: indica se a validação do servidor é executada.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                          |
| [<span data-ttu-id="4c4d7-114">**extendedPeap:AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="4c4d7-114">**extendedPeap:AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | <span data-ttu-id="4c4d7-115">Windows 7 e posterior: indica se o nome de um servidor é lido.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                            |
| [<span data-ttu-id="4c4d7-116">**extendedPeap:IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="4c4d7-116">**extendedPeap:IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | <span data-ttu-id="4c4d7-117">Windows 7 e posterior: indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-117">Windows 7 and later: indicates whether a user's true identity or an anonymous identity is sent.</span></span><br/> |
| [<span data-ttu-id="4c4d7-118">**extendedPeap:PeapExtensionsV2**</span><span class="sxs-lookup"><span data-stu-id="4c4d7-118">**extendedPeap:PeapExtensionsV2**</span></span>](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | <span data-ttu-id="4c4d7-119">Windows 7 e posterior: permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-119">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                 |



## <a name="remarks"></a><span data-ttu-id="4c4d7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c4d7-120">Remarks</span></span>

<span data-ttu-id="4c4d7-121">O elemento **PeapExtensionsType** é opcional.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-121">The **PeapExtensionsType** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4d7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c4d7-122">Requirements</span></span>



| <span data-ttu-id="4c4d7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4d7-123">Requirement</span></span> | <span data-ttu-id="4c4d7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4c4d7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4c4d7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4d7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4d7-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4c4d7-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4c4d7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4d7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4d7-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="4c4d7-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c4d7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c4d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4d7-130">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="4c4d7-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4c4d7-131">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4c4d7-131">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4c4d7-132">Tipos complexos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4c4d7-132">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





