---
title: Elemento EapType (mschapv2connectionpropertiesv1schema)
description: É um tipo derivado do elemento EapType do esquema baseeapconnectionpropertiesv1. Esse é o elemento superior que aparece dentro do elemento config do esquema EapHostConfig.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187759"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a><span data-ttu-id="3ba29-105">Elemento EapType (mschapv2connectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="3ba29-105">EapType Element (mschapv2connectionpropertiesv1schema)</span></span>

<span data-ttu-id="3ba29-106">O elemento **EapType** é um tipo derivado do elemento [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) do esquema [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="3ba29-106">The **EapType** element is a derived type of the [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span> <span data-ttu-id="3ba29-107">Esse é o elemento superior que aparece dentro do elemento config do esquema [EapHostConfig](eaphostconfigschema-elements.md)</span><span class="sxs-lookup"><span data-stu-id="3ba29-107">This is the top element that appears inside the Config element of the [EapHostConfig](eaphostconfigschema-elements.md) schema</span></span>

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
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
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

## <a name="child-elements"></a><span data-ttu-id="3ba29-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3ba29-108">Child elements</span></span>



| <span data-ttu-id="3ba29-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="3ba29-109">Element</span></span>                                                                                                       | <span data-ttu-id="3ba29-110">Type</span><span class="sxs-lookup"><span data-stu-id="3ba29-110">Type</span></span>    | <span data-ttu-id="3ba29-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ba29-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ba29-112">**UseWinLogonCredentials**</span><span class="sxs-lookup"><span data-stu-id="3ba29-112">**UseWinLogonCredentials**</span></span>](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | <span data-ttu-id="3ba29-113">booleano</span><span class="sxs-lookup"><span data-stu-id="3ba29-113">boolean</span></span> | <span data-ttu-id="3ba29-114">Controla o uso das credenciais Winlogin.</span><span class="sxs-lookup"><span data-stu-id="3ba29-114">Controls use of the winlogin credentials.</span></span> <span data-ttu-id="3ba29-115">Se for TRUE, o EAP MS-CHAPv2 obterá as credenciais do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="3ba29-115">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="3ba29-116">Se for FALSE, o EAP MS-CHAPv2 obterá as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="3ba29-116">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <br/> <span data-ttu-id="3ba29-117">O elemento [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="3ba29-117">The [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3ba29-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ba29-118">Remarks</span></span>

<span data-ttu-id="3ba29-119">O elemento **ProcessContents** permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="3ba29-119">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="3ba29-120">O elemento **ProcessContents** é opcional.</span><span class="sxs-lookup"><span data-stu-id="3ba29-120">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba29-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba29-121">Requirements</span></span>



| <span data-ttu-id="3ba29-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba29-122">Requirement</span></span> | <span data-ttu-id="3ba29-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3ba29-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ba29-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba29-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba29-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ba29-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ba29-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba29-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba29-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ba29-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ba29-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ba29-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba29-129">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="3ba29-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3ba29-130">Esquema mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3ba29-130">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





