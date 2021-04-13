---
title: Elemento AnonymousUserName (IdentityPrivacyParameters)
description: Contém uma identidade anônima usada no lugar da identificação verdadeira de um usuário. Ele é enviado durante a 1ª fase da autenticação PEAP quando a identidade é enviada como texto sem formatação.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Elemento AnonymousUserName EAPHost
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
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369759"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a><span data-ttu-id="d582c-105">Elemento AnonymousUserName (IdentityPrivacyParameters)</span><span class="sxs-lookup"><span data-stu-id="d582c-105">AnonymousUserName (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="d582c-106">O elemento **AnonymousUserName (IdentityPrivacyParameters)** contém uma identidade anônima usada no lugar da identificação verdadeira de um usuário.</span><span class="sxs-lookup"><span data-stu-id="d582c-106">The **AnonymousUserName (IdentityPrivacyParameters)** element contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="d582c-107">Ele é enviado durante a 1ª fase da autenticação PEAP quando a **identidade** é enviada como texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="d582c-107">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span>

<span data-ttu-id="d582c-108">O uso de identidade anônima é determinado pelo elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d582c-108">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

<span data-ttu-id="d582c-109">O elemento **AnonymousUserName** é definido pelo [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d582c-109">The **AnonymousUserName** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="d582c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d582c-110">Remarks</span></span>

<span data-ttu-id="d582c-111">O elemento **AnonymousUserName** é opcional.</span><span class="sxs-lookup"><span data-stu-id="d582c-111">The **AnonymousUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d582c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d582c-112">Requirements</span></span>



| <span data-ttu-id="d582c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d582c-113">Requirement</span></span> | <span data-ttu-id="d582c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d582c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d582c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d582c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d582c-116">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d582c-116">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d582c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d582c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d582c-118">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d582c-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d582c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d582c-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="d582c-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="d582c-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d582c-121">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="d582c-121">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="d582c-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="d582c-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d582c-123">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="d582c-123">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="d582c-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="d582c-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d582c-125">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="d582c-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d582c-126">Elementos do esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="d582c-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





