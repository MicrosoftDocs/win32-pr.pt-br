---
title: Tipo complexo IdentityPrivacyParameters
description: Contém informações sobre o uso de identidade anônima durante a autenticação PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104084291"
---
# <a name="identityprivacyparameters-complex-type"></a><span data-ttu-id="7f139-103">Tipo complexo IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="7f139-103">IdentityPrivacyParameters Complex Type</span></span>

<span data-ttu-id="7f139-104">O tipo complexo **IdentityPrivacyParameters** contém informações sobre o uso de identidade anônima durante a autenticação PEAP.</span><span class="sxs-lookup"><span data-stu-id="7f139-104">The **IdentityPrivacyParameters** complex type contains information about anonymous identity usage during PEAP authentication.</span></span>


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| <span data-ttu-id="7f139-105">Elemento</span><span class="sxs-lookup"><span data-stu-id="7f139-105">Element</span></span>                                                                                                               | <span data-ttu-id="7f139-106">Type</span><span class="sxs-lookup"><span data-stu-id="7f139-106">Type</span></span>    | <span data-ttu-id="7f139-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f139-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f139-108">**EnableIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="7f139-108">**EnableIdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | <span data-ttu-id="7f139-109">booleano</span><span class="sxs-lookup"><span data-stu-id="7f139-109">boolean</span></span> | <span data-ttu-id="7f139-110">Indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada.</span><span class="sxs-lookup"><span data-stu-id="7f139-110">Indicates whether a user's true identity or an anonymous identity is sent.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="7f139-111">**AnonymousUserName**</span><span class="sxs-lookup"><span data-stu-id="7f139-111">**AnonymousUserName**</span></span>](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | <span data-ttu-id="7f139-112">string</span><span class="sxs-lookup"><span data-stu-id="7f139-112">string</span></span>  | <span data-ttu-id="7f139-113">contém uma identidade anônima usada no lugar da identificação verdadeira de um usuário.</span><span class="sxs-lookup"><span data-stu-id="7f139-113">contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="7f139-114">Ele é enviado durante a 1ª fase da autenticação PEAP quando a **identidade** é enviada como texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="7f139-114">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span> <span data-ttu-id="7f139-115">O uso de identidade anônima é determinado pelo elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7f139-115">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7f139-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f139-116">Remarks</span></span>

<span data-ttu-id="7f139-117">O elemento IdentityPrivacyParameters é opcional.</span><span class="sxs-lookup"><span data-stu-id="7f139-117">The IdentityPrivacyParameters element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f139-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f139-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f139-119">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="7f139-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7f139-120">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="7f139-120">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="7f139-121">Tipos complexos mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="7f139-121">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




