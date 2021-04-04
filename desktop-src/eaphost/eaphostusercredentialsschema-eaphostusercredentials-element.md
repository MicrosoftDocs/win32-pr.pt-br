---
title: Elemento EapHostUserCredentials
description: Contém o elemento EapMethod e as credenciais ou o elemento CredentialsBlob.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Elemento EapHostUserCredentials EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085953"
---
# <a name="eaphostusercredentials-element"></a><span data-ttu-id="67ffd-104">Elemento EapHostUserCredentials</span><span class="sxs-lookup"><span data-stu-id="67ffd-104">EapHostUserCredentials Element</span></span>

<span data-ttu-id="67ffd-105">O elemento **EapHostUserCredentials** contém o elemento [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) e [**as credenciais**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) ou o elemento [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="67ffd-105">The **EapHostUserCredentials** element contains the [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) element, and [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) or [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) element.</span></span>

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="67ffd-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="67ffd-106">Child elements</span></span>



| <span data-ttu-id="67ffd-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="67ffd-107">Element</span></span>                                                                                                | <span data-ttu-id="67ffd-108">Type</span><span class="sxs-lookup"><span data-stu-id="67ffd-108">Type</span></span>                                                                                                                | <span data-ttu-id="67ffd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="67ffd-109">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67ffd-110">**Credenciais**</span><span class="sxs-lookup"><span data-stu-id="67ffd-110">**Credentials**</span></span>](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [<span data-ttu-id="67ffd-111">**BaseEapMethodUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="67ffd-111">**BaseEapMethodUserCredentials**</span></span>](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | <span data-ttu-id="67ffd-112">É usado quando a configuração do método está no formato de texto XML em vez de em um BLOB binário.</span><span class="sxs-lookup"><span data-stu-id="67ffd-112">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>   |
| [<span data-ttu-id="67ffd-113">**CredentialsBlob**</span><span class="sxs-lookup"><span data-stu-id="67ffd-113">**CredentialsBlob**</span></span>](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | <span data-ttu-id="67ffd-114">hexBinary</span><span class="sxs-lookup"><span data-stu-id="67ffd-114">hexBinary</span></span>                                                                                                           | <span data-ttu-id="67ffd-115">É usado quando a configuração do método é um BLOB binário em vez de no formato de texto XML.</span><span class="sxs-lookup"><span data-stu-id="67ffd-115">Is used when the method configuration is a binary BLOB instead of in XML text format.</span></span><br/> |
| [<span data-ttu-id="67ffd-116">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="67ffd-116">**EapMethod**</span></span>](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [<span data-ttu-id="67ffd-117">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="67ffd-117">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                                                  | <span data-ttu-id="67ffd-118">Identifica o método que está sendo referenciado.</span><span class="sxs-lookup"><span data-stu-id="67ffd-118">Identifies the method being referred to.</span></span> <br/>                                             |



## <a name="remarks"></a><span data-ttu-id="67ffd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="67ffd-119">Remarks</span></span>

<span data-ttu-id="67ffd-120">As [**credenciais**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) e os elementos [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) não podem ser usados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="67ffd-120">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) elements cannot be both be used simultaneously.</span></span>

<span data-ttu-id="67ffd-121">Há um ponto de extensão para outros namespaces.</span><span class="sxs-lookup"><span data-stu-id="67ffd-121">There is an extension point for other namespaces.</span></span>

<span data-ttu-id="67ffd-122">O elemento **ProcessContents** permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="67ffd-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="67ffd-123">O elemento **ProcessContents** é opcional.</span><span class="sxs-lookup"><span data-stu-id="67ffd-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="67ffd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ffd-124">Requirements</span></span>



| <span data-ttu-id="67ffd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ffd-125">Requirement</span></span> | <span data-ttu-id="67ffd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="67ffd-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67ffd-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67ffd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="67ffd-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67ffd-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="67ffd-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67ffd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="67ffd-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67ffd-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67ffd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="67ffd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ffd-132">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="67ffd-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="67ffd-133">Esquema eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="67ffd-133">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





