---
description: Define uma rede bloqueada.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Elemento de rede (blocklist)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759064"
---
# <a name="network-blocklist-element"></a><span data-ttu-id="28b89-103">Elemento de rede (blocklist)</span><span class="sxs-lookup"><span data-stu-id="28b89-103">network (blockList) Element</span></span>

<span data-ttu-id="28b89-104">O elemento de rede (blocklist) define uma rede bloqueada.</span><span class="sxs-lookup"><span data-stu-id="28b89-104">The network (blockList) element defines a blocked network.</span></span> <span data-ttu-id="28b89-105">Um computador não pode se conectar a uma rede bloqueada.</span><span class="sxs-lookup"><span data-stu-id="28b89-105">A machine cannot connect to a blocked network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="28b89-106">O elemento **Network** é definido pelo elemento [**blocklist**](wlan-policyschema-blocklist-networkfilter-element.md) .</span><span class="sxs-lookup"><span data-stu-id="28b89-106">The **network** element is defined by the [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="28b89-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28b89-107">Requirements</span></span>



| <span data-ttu-id="28b89-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="28b89-108">Requirement</span></span> | <span data-ttu-id="28b89-109">Valor</span><span class="sxs-lookup"><span data-stu-id="28b89-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="28b89-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28b89-110">Minimum supported client</span></span><br/> | <span data-ttu-id="28b89-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28b89-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="28b89-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28b89-112">Minimum supported server</span></span><br/> | <span data-ttu-id="28b89-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28b89-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28b89-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="28b89-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="28b89-115">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="28b89-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="28b89-116">**Bloqueios**</span><span class="sxs-lookup"><span data-stu-id="28b89-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="28b89-117">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="28b89-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="28b89-118">**Blocklist (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="28b89-118">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




