---
title: Elemento EapType (eaptlsuserpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema baseeapuserpropertiesv1. Para o eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187755"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a><span data-ttu-id="445c6-105">Elemento EapType (eaptlsuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="445c6-105">EapType element (eaptlsuserpropertiesv1schema)</span></span>

<span data-ttu-id="445c6-106">O elemento **EapType** é um tipo derivado do elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) do esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="445c6-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="445c6-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="445c6-107">Child elements</span></span>



| <span data-ttu-id="445c6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="445c6-108">Element</span></span>                                                                   | <span data-ttu-id="445c6-109">Type</span><span class="sxs-lookup"><span data-stu-id="445c6-109">Type</span></span>      | <span data-ttu-id="445c6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="445c6-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="445c6-111">**Usu**</span><span class="sxs-lookup"><span data-stu-id="445c6-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="445c6-112">Captura o nome de usuário a ser enviado na resposta EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="445c6-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="445c6-113">Se o elemento [**username**](eaptlsuserpropertiesv1schema-username-element.md) estiver ausente, o EAP-TLS usará o nome no certificado referido no elemento [**usercert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="445c6-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="445c6-114">**Usercert**</span><span class="sxs-lookup"><span data-stu-id="445c6-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="445c6-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="445c6-115">hexBinary</span></span> | <span data-ttu-id="445c6-116">Refere-se ao hash SHA-1 do certificado que deve ser usado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="445c6-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="445c6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="445c6-117">Remarks</span></span>

<span data-ttu-id="445c6-118">O elemento **ProcessContents** permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="445c6-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="445c6-119">O elemento **ProcessContents** é opcional.</span><span class="sxs-lookup"><span data-stu-id="445c6-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="445c6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="445c6-120">Requirements</span></span>



| <span data-ttu-id="445c6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="445c6-121">Requirement</span></span> | <span data-ttu-id="445c6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="445c6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="445c6-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="445c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="445c6-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="445c6-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="445c6-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="445c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="445c6-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="445c6-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="445c6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="445c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445c6-128">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="445c6-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="445c6-129">Esquema eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="445c6-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





