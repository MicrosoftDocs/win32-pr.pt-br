---
description: Define a lista de redes permitidas e negadas para computadores.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Elemento networkFilter (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782966"
---
# <a name="networkfilter-wlanpolicy-element"></a><span data-ttu-id="f279a-103">Elemento networkFilter (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="f279a-103">networkFilter (WLANPolicy) Element</span></span>

<span data-ttu-id="f279a-104">O elemento networkFilter (WLANPolicy) define a lista de redes permitidas e negadas para computadores.</span><span class="sxs-lookup"><span data-stu-id="f279a-104">The networkFilter (WLANPolicy) element defines the list of allowed and denied networks for machines.</span></span>

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="network"
                            type="networkItemType"
                            maxOccurs="unbounded"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="blockList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="network"
                            type="networkItemType"
                            maxOccurs="unbounded"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
                type="boolean"
                minOccurs="0"
             />
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

<span data-ttu-id="f279a-105">O elemento **networkFilter** é definido pelo elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f279a-105">The **networkFilter** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f279a-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f279a-106">Child elements</span></span>



| <span data-ttu-id="f279a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f279a-107">Element</span></span>                                                                    | <span data-ttu-id="f279a-108">Type</span><span class="sxs-lookup"><span data-stu-id="f279a-108">Type</span></span>                                                                     | <span data-ttu-id="f279a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f279a-109">Description</span></span>                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f279a-110">**Lista**</span><span class="sxs-lookup"><span data-stu-id="f279a-110">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="f279a-111">A lista de redes LAN sem fio às quais qualquer computador deve ter permissão para se conectar.</span><span class="sxs-lookup"><span data-stu-id="f279a-111">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/> |
| [<span data-ttu-id="f279a-112">**Bloqueios**</span><span class="sxs-lookup"><span data-stu-id="f279a-112">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="f279a-113">A lista de redes LAN sem fio às quais um computador não deve se conectar.</span><span class="sxs-lookup"><span data-stu-id="f279a-113">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>              |
| [<span data-ttu-id="f279a-114">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="f279a-114">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)   | <span data-ttu-id="f279a-115">booleano</span><span class="sxs-lookup"><span data-stu-id="f279a-115">boolean</span></span>                                                                  | <span data-ttu-id="f279a-116">Especifica se o acesso a todas as redes de infraestrutura está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f279a-116">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                     |
| [<span data-ttu-id="f279a-117">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="f279a-117">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md) | <span data-ttu-id="f279a-118">booleano</span><span class="sxs-lookup"><span data-stu-id="f279a-118">boolean</span></span>                                                                  | <span data-ttu-id="f279a-119">Especifica se o acesso a todas as redes ad hoc está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f279a-119">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                             |
| [<span data-ttu-id="f279a-120">**rede**</span><span class="sxs-lookup"><span data-stu-id="f279a-120">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)             | [<span data-ttu-id="f279a-121">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="f279a-121">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="f279a-122">Uma rede permitida.</span><span class="sxs-lookup"><span data-stu-id="f279a-122">An allowed network.</span></span> <br/>                                                                |
| [<span data-ttu-id="f279a-123">**rede**</span><span class="sxs-lookup"><span data-stu-id="f279a-123">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)             | [<span data-ttu-id="f279a-124">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="f279a-124">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="f279a-125">Uma rede bloqueada.</span><span class="sxs-lookup"><span data-stu-id="f279a-125">A blocked network.</span></span> <br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="f279a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f279a-126">Requirements</span></span>



| <span data-ttu-id="f279a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f279a-127">Requirement</span></span> | <span data-ttu-id="f279a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f279a-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f279a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f279a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f279a-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f279a-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f279a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f279a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f279a-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f279a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f279a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f279a-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f279a-134">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="f279a-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f279a-135">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="f279a-135">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="f279a-136">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="f279a-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f279a-137">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="f279a-137">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




