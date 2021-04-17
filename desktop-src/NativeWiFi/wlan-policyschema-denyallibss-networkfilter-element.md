---
description: Especifica se o acesso a todas as redes ad hoc está bloqueado.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Elemento denyAllIBSS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789883"
---
# <a name="denyallibss-networkfilter-element"></a><span data-ttu-id="8e65a-103">Elemento denyAllIBSS (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="8e65a-103">denyAllIBSS (networkFilter) Element</span></span>

<span data-ttu-id="8e65a-104">O elemento denyAllIBSS (networkFilter) especifica se o acesso a todas as redes ad hoc está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="8e65a-104">The denyAllIBSS (networkFilter) element specifies if access to all ad-hoc networks is blocked.</span></span> <span data-ttu-id="8e65a-105">Quando **denyAllIBSS** tem um valor de true, os computadores não podem se conectar a uma rede ad hoc; caso contrário, os computadores podem se conectar a redes ad hoc.</span><span class="sxs-lookup"><span data-stu-id="8e65a-105">When **denyAllIBSS** has a value of TRUE, machines cannot connect to an ad-hoc network; otherwise, machines may connect to ad-hoc networks.</span></span>

<span data-ttu-id="8e65a-106">O valor padrão para esse elemento é FALSE.</span><span class="sxs-lookup"><span data-stu-id="8e65a-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="8e65a-107">Se **denyAllIBSS** não for especificado em um perfil, por padrão, os computadores poderão se conectar a redes ad-hoc.</span><span class="sxs-lookup"><span data-stu-id="8e65a-107">If **denyAllIBSS** is not specified in a profile, then by default machines may connect to ad-hoc networks.</span></span>

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

<span data-ttu-id="8e65a-108">O elemento **denyAllIBSS** é definido pelo elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8e65a-108">The **denyAllIBSS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e65a-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e65a-109">Requirements</span></span>



| <span data-ttu-id="8e65a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e65a-110">Requirement</span></span> | <span data-ttu-id="8e65a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="8e65a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8e65a-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e65a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8e65a-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e65a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8e65a-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e65a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8e65a-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e65a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e65a-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e65a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e65a-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="8e65a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8e65a-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="8e65a-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="8e65a-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="8e65a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8e65a-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="8e65a-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




