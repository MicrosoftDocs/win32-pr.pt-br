---
title: Elemento EapType (mspeapuserpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema baseeapuserpropertiesv1. Para o mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
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
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187835"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a><span data-ttu-id="3da54-105">Elemento EapType (mspeapuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="3da54-105">EapType Element (mspeapuserpropertiesv1schema)</span></span>

<span data-ttu-id="3da54-106">O elemento **EapType** é um tipo derivado do elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) do esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="3da54-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType
        "
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
                        maxOccurs="unbounded"
                        ref="Eap"
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

## <a name="child-elements"></a><span data-ttu-id="3da54-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3da54-107">Child elements</span></span>



| <span data-ttu-id="3da54-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3da54-108">Element</span></span>                                                                               | <span data-ttu-id="3da54-109">Type</span><span class="sxs-lookup"><span data-stu-id="3da54-109">Type</span></span>                                                                                      | <span data-ttu-id="3da54-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3da54-110">Description</span></span>                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3da54-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="3da54-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | <span data-ttu-id="3da54-112">O elemento [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) identifica o método interno e as credenciais a serem usadas com esse método.</span><span class="sxs-lookup"><span data-stu-id="3da54-112">The [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) element identifies the inner method and the credentials to be used with that method.</span></span> <span data-ttu-id="3da54-113">Quando a configuração de PEAP estiver configurada para acesso de convidado PEAP, esse elemento estará ausente.</span><span class="sxs-lookup"><span data-stu-id="3da54-113">When PEAP configuration is configured for PEAP guest access, this element is absent.</span></span><br/>                                  |
| [<span data-ttu-id="3da54-114">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="3da54-114">**PeapExtensions**</span></span>](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [<span data-ttu-id="3da54-115">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="3da54-115">**PeapExtensionsType**</span></span>](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | <span data-ttu-id="3da54-116">O elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="3da54-116">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <br/> <span data-ttu-id="3da54-117">O elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="3da54-117">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3da54-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3da54-118">Requirements</span></span>



| <span data-ttu-id="3da54-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da54-119">Requirement</span></span> | <span data-ttu-id="3da54-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3da54-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3da54-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3da54-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3da54-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3da54-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3da54-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3da54-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3da54-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3da54-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3da54-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3da54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da54-126">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="3da54-126">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3da54-127">Esquema mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3da54-127">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





