---
title: Elemento EapType (eaptlsconnectionpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema BaseEapConnectionProperties. Para o eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
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
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188003"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a><span data-ttu-id="4e6f7-105">Elemento EapType (eaptlsconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="4e6f7-105">EapType element (eaptlsconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="4e6f7-106">O elemento **EapType** é um tipo derivado do elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) do esquema [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="4e6f7-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="4e6f7-107">Esse elemento **EapType** derivado contém os seguintes elementos: [**CredentialName**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)e [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span><span class="sxs-lookup"><span data-stu-id="4e6f7-107">This derived **EapType** element contains the following elements: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md), and [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span></span>

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
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="4e6f7-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4e6f7-108">Child elements</span></span>



| <span data-ttu-id="4e6f7-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="4e6f7-109">Element</span></span>                                                                                                                               | <span data-ttu-id="4e6f7-110">Type</span><span class="sxs-lookup"><span data-stu-id="4e6f7-110">Type</span></span>                                                                                                              | <span data-ttu-id="4e6f7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e6f7-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e6f7-112">**extendedTLS: PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="4e6f7-112">**extendedTLS: PerformServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | <span data-ttu-id="4e6f7-113">Windows 7 e posterior: indica se a validação do servidor é executada.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="4e6f7-114">**extendedTLS: AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="4e6f7-114">**extendedTLS: AcceptServerName**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | <span data-ttu-id="4e6f7-115">Windows 7 e posterior: indica se o nome de um servidor é lido.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="4e6f7-116">**extendedTLS: TLSExtensions**</span><span class="sxs-lookup"><span data-stu-id="4e6f7-116">**extendedTLS: TLSExtensions**</span></span>](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | <span data-ttu-id="4e6f7-117">Windows 7 e posterior: permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-117">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4e6f7-118">**Credenciais**</span><span class="sxs-lookup"><span data-stu-id="4e6f7-118">**CredentialsSource**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [<span data-ttu-id="4e6f7-119">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="4e6f7-119">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | <span data-ttu-id="4e6f7-120">Contém informações sobre o local do certificado EAP-TLS (segurança de nível de transporte) EAP.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-120">Contains information about the location of the EAP Transport Level Security (EAP-TLS) certificate.</span></span> <br/> <span data-ttu-id="4e6f7-121">O elemento [**CredentialName**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-121">The [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="4e6f7-122">**DifferentUsername**</span><span class="sxs-lookup"><span data-stu-id="4e6f7-122">**DifferentUsername**</span></span>](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | <span data-ttu-id="4e6f7-123">booleano</span><span class="sxs-lookup"><span data-stu-id="4e6f7-123">boolean</span></span>                                                                                                           | <span data-ttu-id="4e6f7-124">Determina o nome de usuário que o EAP-TLS deve usar.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-124">Determines which user name EAP-TLS is to use.</span></span> <br/> <span data-ttu-id="4e6f7-125">Se o elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) for **true**, o EAP-TLS deverá usar um nome de usuário diferente do nome que aparece no certificado.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-125">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **TRUE**, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="4e6f7-126">Se o elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) for **false**, o EAP-TLS usará o nome de usuário que aparece no certificado.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-126">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **FALSE**, EAP-TLS uses the user name that appears on the certificate.</span></span><br/> <span data-ttu-id="4e6f7-127">O elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-127">The [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is optional.</span></span> <br/> |
| [<span data-ttu-id="4e6f7-128">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="4e6f7-128">**ServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [<span data-ttu-id="4e6f7-129">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="4e6f7-129">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | <span data-ttu-id="4e6f7-130">Contém informações sobre como executar a validação do servidor.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-130">Contains information about how to perform server validation.</span></span> <span data-ttu-id="4e6f7-131">O elemento [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="4e6f7-131">The [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="4e6f7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e6f7-132">Requirements</span></span>



| <span data-ttu-id="4e6f7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e6f7-133">Requirement</span></span> | <span data-ttu-id="4e6f7-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4e6f7-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4e6f7-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e6f7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4e6f7-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e6f7-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4e6f7-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e6f7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4e6f7-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e6f7-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e6f7-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e6f7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e6f7-140">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="4e6f7-140">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4e6f7-141">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4e6f7-141">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4e6f7-142">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4e6f7-142">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





