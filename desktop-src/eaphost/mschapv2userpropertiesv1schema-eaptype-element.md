---
title: Elemento EapType (mschapv2userpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema baseeapuserpropertiesv1. Para o mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187747"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a><span data-ttu-id="827fc-105">Elemento EapType (mschapv2userpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="827fc-105">EapType element (mschapv2userpropertiesv1schema)</span></span>

<span data-ttu-id="827fc-106">O elemento **EapType** é um tipo derivado do elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) do esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="827fc-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="827fc-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="827fc-107">Child elements</span></span>



| <span data-ttu-id="827fc-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="827fc-108">Element</span></span>                                                                           | <span data-ttu-id="827fc-109">Type</span><span class="sxs-lookup"><span data-stu-id="827fc-109">Type</span></span>   | <span data-ttu-id="827fc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="827fc-110">Description</span></span>                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="827fc-111">**Usu**</span><span class="sxs-lookup"><span data-stu-id="827fc-111">**Username**</span></span>](mschapv2userpropertiesv1schema-username-element.md)               |        | <span data-ttu-id="827fc-112">Identifica o usuário que está sendo autenticado.</span><span class="sxs-lookup"><span data-stu-id="827fc-112">Identifies the user being authenticated.</span></span> <span data-ttu-id="827fc-113">Se esse elemento não estiver presente, o nome de usuário será obtido do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="827fc-113">If this element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="827fc-114">O elemento [**username**](mschapv2userpropertiesv1schema-username-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="827fc-114">The [**Username**](mschapv2userpropertiesv1schema-username-element.md) element is optional.</span></span><br/>                                        |
| [<span data-ttu-id="827fc-115">**LogonDomain**</span><span class="sxs-lookup"><span data-stu-id="827fc-115">**LogonDomain**</span></span>](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | <span data-ttu-id="827fc-116">string</span><span class="sxs-lookup"><span data-stu-id="827fc-116">string</span></span> | <span data-ttu-id="827fc-117">Identifica o domínio do usuário ou computador que está sendo autenticado.</span><span class="sxs-lookup"><span data-stu-id="827fc-117">Identifies the domain of the user or machine being authenticated.</span></span> <span data-ttu-id="827fc-118">Se esse elemento não estiver presente, o domínio do Winlogon será usado.</span><span class="sxs-lookup"><span data-stu-id="827fc-118">If this element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="827fc-119">O elemento [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="827fc-119">The [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) element is optional.</span></span><br/>        |
| [<span data-ttu-id="827fc-120">**Senha**</span><span class="sxs-lookup"><span data-stu-id="827fc-120">**Password**</span></span>](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | <span data-ttu-id="827fc-121">string</span><span class="sxs-lookup"><span data-stu-id="827fc-121">string</span></span> | <span data-ttu-id="827fc-122">Identifica a senha do usuário ou computador que está sendo autenticado.</span><span class="sxs-lookup"><span data-stu-id="827fc-122">Identifies the password of the user or machine being authenticated.</span></span> <span data-ttu-id="827fc-123">Se esse elemento não estiver presente, o hash de senha será obtido do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="827fc-123">If this element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="827fc-124">O elemento [**password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="827fc-124">The [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="827fc-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="827fc-125">Remarks</span></span>

<span data-ttu-id="827fc-126">O elemento **ProcessContents** permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="827fc-126">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="827fc-127">O elemento **ProcessContents** é opcional.</span><span class="sxs-lookup"><span data-stu-id="827fc-127">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="827fc-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="827fc-128">Requirements</span></span>



| <span data-ttu-id="827fc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="827fc-129">Requirement</span></span> | <span data-ttu-id="827fc-130">Valor</span><span class="sxs-lookup"><span data-stu-id="827fc-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="827fc-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="827fc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="827fc-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="827fc-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="827fc-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="827fc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="827fc-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="827fc-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="827fc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="827fc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="827fc-136">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="827fc-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="827fc-137">Esquema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="827fc-137">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





