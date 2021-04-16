---
description: Define uma rede permitida.
ms.assetid: 6dd90924-ded4-427d-a6cd-7742acf89c21
title: Elemento de rede (permitirlist)
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
ms.openlocfilehash: eb89a3037b7684c4e20e26ef3a2b0502be69251a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794445"
---
# <a name="network-allowlist-element"></a><span data-ttu-id="79c47-103">Elemento de rede (permitirlist)</span><span class="sxs-lookup"><span data-stu-id="79c47-103">network (allowList) Element</span></span>

<span data-ttu-id="79c47-104">O elemento de rede (permitir alist) define uma rede permitida.</span><span class="sxs-lookup"><span data-stu-id="79c47-104">The network (allowList) element defines an allowed network.</span></span> <span data-ttu-id="79c47-105">Um computador deve ter permissão para se conectar a uma rede permitida.</span><span class="sxs-lookup"><span data-stu-id="79c47-105">A machine must be allowed to connect to an allowed network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="79c47-106">O elemento **Network** é definido pelo elemento [**allowlist**](wlan-policyschema-allowlist-networkfilter-element.md) .</span><span class="sxs-lookup"><span data-stu-id="79c47-106">The **network** element is defined by the [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c47-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79c47-107">Requirements</span></span>



| <span data-ttu-id="79c47-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="79c47-108">Requirement</span></span> | <span data-ttu-id="79c47-109">Valor</span><span class="sxs-lookup"><span data-stu-id="79c47-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79c47-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79c47-110">Minimum supported client</span></span><br/> | <span data-ttu-id="79c47-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79c47-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="79c47-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79c47-112">Minimum supported server</span></span><br/> | <span data-ttu-id="79c47-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79c47-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79c47-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="79c47-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="79c47-115">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="79c47-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="79c47-116">**Lista**</span><span class="sxs-lookup"><span data-stu-id="79c47-116">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="79c47-117">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="79c47-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="79c47-118">**permitirlist (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="79c47-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> </dl>

 

 




