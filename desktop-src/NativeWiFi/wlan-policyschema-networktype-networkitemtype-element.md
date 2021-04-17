---
description: Especifica um tipo de rede.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Elemento NetworkType (networkitemtype)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757236"
---
# <a name="networktype-networkitemtype-element"></a><span data-ttu-id="90e79-103">Elemento NetworkType (networkitemtype)</span><span class="sxs-lookup"><span data-stu-id="90e79-103">networkType (networkItemType) Element</span></span>

<span data-ttu-id="90e79-104">O elemento NetworkType (networkitemtype) especifica um tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="90e79-104">The networkType (networkItemType) element specifies a network type.</span></span> <span data-ttu-id="90e79-105">Há dois tipos de redes: redes de infraestrutura (ESS) e redes ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="90e79-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

<span data-ttu-id="90e79-106">O elemento **NetworkType** é definido pelo tipo complexo [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="90e79-106">The **networkType** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="90e79-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90e79-107">Requirements</span></span>



| <span data-ttu-id="90e79-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="90e79-108">Requirement</span></span> | <span data-ttu-id="90e79-109">Valor</span><span class="sxs-lookup"><span data-stu-id="90e79-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="90e79-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90e79-110">Minimum supported client</span></span><br/> | <span data-ttu-id="90e79-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90e79-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="90e79-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90e79-112">Minimum supported server</span></span><br/> | <span data-ttu-id="90e79-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90e79-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90e79-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="90e79-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="90e79-115">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="90e79-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="90e79-116">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="90e79-116">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="90e79-117">**Possíveis elementos pai imediatos na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="90e79-117">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="90e79-118">**rede (permitirlist)**</span><span class="sxs-lookup"><span data-stu-id="90e79-118">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="90e79-119">**rede (bloquearlist)**</span><span class="sxs-lookup"><span data-stu-id="90e79-119">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




