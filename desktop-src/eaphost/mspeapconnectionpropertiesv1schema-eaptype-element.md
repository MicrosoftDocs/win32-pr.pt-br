---
title: Elemento EapType (mspeapconnectionpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema BaseEapConnectionProperties. Para o mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187751"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a><span data-ttu-id="7cda6-105">Elemento EapType (mspeapconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="7cda6-105">EapType element (mspeapconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="7cda6-106">O elemento **EapType** é um tipo derivado do elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) do esquema [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="7cda6-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="7cda6-107">Esse elemento **EapType** derivado contém os seguintes elementos: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) e [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span><span class="sxs-lookup"><span data-stu-id="7cda6-107">This derived **EapType** element contains the following elements: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) and [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="7cda6-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7cda6-108">Child elements</span></span>



| <span data-ttu-id="7cda6-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="7cda6-109">Element</span></span>                                                                                                     | <span data-ttu-id="7cda6-110">Type</span><span class="sxs-lookup"><span data-stu-id="7cda6-110">Type</span></span>                                                                                                            | <span data-ttu-id="7cda6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cda6-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cda6-112">**EAP**</span><span class="sxs-lookup"><span data-stu-id="7cda6-112">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | <span data-ttu-id="7cda6-113">Descreve o método interno e a configuração do método.</span><span class="sxs-lookup"><span data-stu-id="7cda6-113">Describes the inner method and the method configuration.</span></span> <span data-ttu-id="7cda6-114">Se o elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) for true, o elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="7cda6-114">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present.</span></span> <span data-ttu-id="7cda6-115">Se o elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) for false, o elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) deverá estar ausente.</span><span class="sxs-lookup"><span data-stu-id="7cda6-115">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is FALSE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be absent.</span></span><br/>           |
| [<span data-ttu-id="7cda6-116">**EnableQuarantineChecks**</span><span class="sxs-lookup"><span data-stu-id="7cda6-116">**EnableQuarantineChecks**</span></span>](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | <span data-ttu-id="7cda6-117">booleano</span><span class="sxs-lookup"><span data-stu-id="7cda6-117">boolean</span></span>                                                                                                         | <span data-ttu-id="7cda6-118">Indica se as verificações de NAP (proteção de acesso à rede) devem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="7cda6-118">Indicates whether to perform Network Access Protection (NAP) checks.</span></span> <span data-ttu-id="7cda6-119">Se o elemento [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) for true, o PEAP executará verificações de NAP; Se FALSE, o PEAP não executará verificações de NAP.</span><span class="sxs-lookup"><span data-stu-id="7cda6-119">If the [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is TRUE, then PEAP will perform NAP checks; if FALSE PEAP will not perform NAP checks.</span></span> <span data-ttu-id="7cda6-120">O elemento [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="7cda6-120">The [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is optional.</span></span><br/>                                                                                |
| [<span data-ttu-id="7cda6-121">**FastReconnect**</span><span class="sxs-lookup"><span data-stu-id="7cda6-121">**FastReconnect**</span></span>](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | <span data-ttu-id="7cda6-122">booleano</span><span class="sxs-lookup"><span data-stu-id="7cda6-122">boolean</span></span>                                                                                                         | <span data-ttu-id="7cda6-123">Indica se uma reconexão rápida deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="7cda6-123">Indicates whether to perform a fast reconnect.</span></span> <span data-ttu-id="7cda6-124">Se o elemento [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) for true, o PEAP tentará executar uma reconexão rápida; Se for FALSE, o PEAP executará a autenticação completa.</span><span class="sxs-lookup"><span data-stu-id="7cda6-124">If the [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="7cda6-125">O elemento [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="7cda6-125">The [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="7cda6-126">**IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="7cda6-126">**IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [<span data-ttu-id="7cda6-127">**IdentityPrivacyParameters**</span><span class="sxs-lookup"><span data-stu-id="7cda6-127">**IdentityPrivacyParameters**</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | <span data-ttu-id="7cda6-128">Windows 7 ou posterior: indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada.</span><span class="sxs-lookup"><span data-stu-id="7cda6-128">Windows 7 or later: Indicates whether a user's true identity or an anonymous identity is sent.</span></span> <span data-ttu-id="7cda6-129">O elemento [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="7cda6-129">The [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="7cda6-130">**InnerEapOptional**</span><span class="sxs-lookup"><span data-stu-id="7cda6-130">**InnerEapOptional**</span></span>](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | <span data-ttu-id="7cda6-131">booleano</span><span class="sxs-lookup"><span data-stu-id="7cda6-131">boolean</span></span>                                                                                                         | <span data-ttu-id="7cda6-132">Indica se o acesso de convidado deve ser realizado.</span><span class="sxs-lookup"><span data-stu-id="7cda6-132">Indicates whether to perform GUEST access.</span></span> <span data-ttu-id="7cda6-133">Se o elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) for true, o elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) deverá estar presente e descreverá o método interno e sua configuração; Se for FALSE, o PEAP executará o acesso de convidado.</span><span class="sxs-lookup"><span data-stu-id="7cda6-133">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and its configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="7cda6-134">O elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="7cda6-134">The [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is optional.</span></span><br/>            |
| [<span data-ttu-id="7cda6-135">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="7cda6-135">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [<span data-ttu-id="7cda6-136">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="7cda6-136">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | <span data-ttu-id="7cda6-137">O elemento [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="7cda6-137">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <span data-ttu-id="7cda6-138">O elemento [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="7cda6-138">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="7cda6-139">**RequireCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="7cda6-139">**RequireCryptoBinding**</span></span>](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | <span data-ttu-id="7cda6-140">booleano</span><span class="sxs-lookup"><span data-stu-id="7cda6-140">boolean</span></span>                                                                                                         | <span data-ttu-id="7cda6-141">Indica se é para autenticar com servidores que dão suporte a cryptobinding.</span><span class="sxs-lookup"><span data-stu-id="7cda6-141">Indicates whether to authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="7cda6-142">Se o elemento [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) for true, o PEAP será autenticado com servidores que não dão suporte a cryptobinding; Se for FALSE, o PEAP será autenticado somente com servidores que dão suporte a cryptobinding.</span><span class="sxs-lookup"><span data-stu-id="7cda6-142">If the [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="7cda6-143">O elemento [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="7cda6-143">The [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="7cda6-144">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="7cda6-144">**ServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [<span data-ttu-id="7cda6-145">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="7cda6-145">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | <span data-ttu-id="7cda6-146">Contém informações sobre como executar a validação do servidor.</span><span class="sxs-lookup"><span data-stu-id="7cda6-146">Contains information about how to perform server validation.</span></span> <span data-ttu-id="7cda6-147">O elemento [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="7cda6-147">The [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="7cda6-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cda6-148">Requirements</span></span>



| <span data-ttu-id="7cda6-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cda6-149">Requirement</span></span> | <span data-ttu-id="7cda6-150">Valor</span><span class="sxs-lookup"><span data-stu-id="7cda6-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7cda6-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cda6-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7cda6-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7cda6-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7cda6-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cda6-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7cda6-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7cda6-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cda6-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cda6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cda6-156">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="7cda6-156">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7cda6-157">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7cda6-157">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="7cda6-158">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7cda6-158">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





