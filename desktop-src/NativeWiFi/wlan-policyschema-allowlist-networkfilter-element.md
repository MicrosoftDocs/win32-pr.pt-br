---
description: Especifica a lista de redes LAN sem fio às quais qualquer computador deve ter permissão para se conectar.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: Elemento allowlist (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761887"
---
# <a name="allowlist-networkfilter-element"></a><span data-ttu-id="6c48a-103">Elemento allowlist (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="6c48a-103">allowList (networkFilter) Element</span></span>

<span data-ttu-id="6c48a-104">O elemento allowlist (networkFilter) especifica a lista de redes LAN sem fio às quais qualquer computador deve ter permissão para se conectar.</span><span class="sxs-lookup"><span data-stu-id="6c48a-104">The allowList (networkFilter) element specifies the list of wireless LAN networks to which any machine must be allowed to connect.</span></span>

``` syntax
<xs:element name="allowList">
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
```

<span data-ttu-id="6c48a-105">O elemento **allowlist** é definido pelo elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6c48a-105">The **allowList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6c48a-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6c48a-106">Child elements</span></span>



| <span data-ttu-id="6c48a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c48a-107">Element</span></span>                                                        | <span data-ttu-id="6c48a-108">Type</span><span class="sxs-lookup"><span data-stu-id="6c48a-108">Type</span></span>                                                                     | <span data-ttu-id="6c48a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c48a-109">Description</span></span>                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="6c48a-110">**rede**</span><span class="sxs-lookup"><span data-stu-id="6c48a-110">**network**</span></span>](wlan-policyschema-network-allowlist-element.md) | [<span data-ttu-id="6c48a-111">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="6c48a-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="6c48a-112">A rede à qual o computador pode se conectar.</span><span class="sxs-lookup"><span data-stu-id="6c48a-112">The network to which the machine can connect.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6c48a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c48a-113">Requirements</span></span>



| <span data-ttu-id="6c48a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c48a-114">Requirement</span></span> | <span data-ttu-id="6c48a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6c48a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c48a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c48a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c48a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c48a-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c48a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c48a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c48a-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c48a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c48a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c48a-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c48a-121">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="6c48a-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6c48a-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="6c48a-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="6c48a-123">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="6c48a-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6c48a-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="6c48a-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




