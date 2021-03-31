---
description: Especifica o SSID (identificador de conjunto de serviços) de uma rede sem fio.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Elemento NetworkName (networkitemtype)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829784"
---
# <a name="networkname-networkitemtype-element"></a><span data-ttu-id="8ce2b-103">Elemento NetworkName (networkitemtype)</span><span class="sxs-lookup"><span data-stu-id="8ce2b-103">networkName (networkItemType) Element</span></span>

<span data-ttu-id="8ce2b-104">O elemento NetworkName (networkitemtype) especifica o SSID (identificador de conjunto de serviços) de uma rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="8ce2b-104">The networkName (networkItemType) element specifies the service set identifier (SSID) of a wireless network.</span></span>

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

<span data-ttu-id="8ce2b-105">O elemento **NetworkName** é definido pelo tipo complexo [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8ce2b-105">The **networkName** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce2b-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ce2b-106">Requirements</span></span>



| <span data-ttu-id="8ce2b-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ce2b-107">Requirement</span></span> | <span data-ttu-id="8ce2b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="8ce2b-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ce2b-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ce2b-109">Minimum supported client</span></span><br/> | <span data-ttu-id="8ce2b-110">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ce2b-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ce2b-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ce2b-111">Minimum supported server</span></span><br/> | <span data-ttu-id="8ce2b-112">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ce2b-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ce2b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ce2b-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ce2b-114">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="8ce2b-114">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8ce2b-115">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="8ce2b-115">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="8ce2b-116">**Possíveis elementos pai imediatos na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="8ce2b-116">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8ce2b-117">**rede (permitirlist)**</span><span class="sxs-lookup"><span data-stu-id="8ce2b-117">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="8ce2b-118">**rede (bloquearlist)**</span><span class="sxs-lookup"><span data-stu-id="8ce2b-118">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




