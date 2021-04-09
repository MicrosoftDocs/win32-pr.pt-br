---
description: Especifica a lista de redes LAN sem fio às quais um computador não deve se conectar.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Elemento blocklist (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920660"
---
# <a name="blocklist-networkfilter-element"></a><span data-ttu-id="52e62-103">Elemento blocklist (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="52e62-103">blockList (networkFilter) Element</span></span>

<span data-ttu-id="52e62-104">O elemento blocklist (networkFilter) especifica a lista de redes LAN sem fio às quais um computador não deve se conectar.</span><span class="sxs-lookup"><span data-stu-id="52e62-104">The blockList (networkFilter) element specifies the list of wireless LAN networks to which a machine must not connect.</span></span>

``` syntax
<xs:element name="blockList">
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

<span data-ttu-id="52e62-105">O elemento **blocklist** é definido pelo elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="52e62-105">The **blockList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="52e62-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="52e62-106">Child elements</span></span>



| <span data-ttu-id="52e62-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="52e62-107">Element</span></span>                                                        | <span data-ttu-id="52e62-108">Type</span><span class="sxs-lookup"><span data-stu-id="52e62-108">Type</span></span>                                                                     | <span data-ttu-id="52e62-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="52e62-109">Description</span></span>                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="52e62-110">**rede**</span><span class="sxs-lookup"><span data-stu-id="52e62-110">**network**</span></span>](wlan-policyschema-network-blocklist-element.md) | [<span data-ttu-id="52e62-111">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="52e62-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="52e62-112">A rede bloqueada.</span><span class="sxs-lookup"><span data-stu-id="52e62-112">The blocked network.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="52e62-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52e62-113">Requirements</span></span>



| <span data-ttu-id="52e62-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52e62-114">Requirement</span></span> | <span data-ttu-id="52e62-115">Valor</span><span class="sxs-lookup"><span data-stu-id="52e62-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52e62-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52e62-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52e62-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52e62-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52e62-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52e62-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52e62-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52e62-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52e62-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="52e62-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="52e62-121">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="52e62-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="52e62-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="52e62-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="52e62-123">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="52e62-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="52e62-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="52e62-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




