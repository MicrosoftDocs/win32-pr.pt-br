---
description: Especifica se o acesso a todas as redes de infraestrutura está bloqueado.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Elemento denyAllESS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164396"
---
# <a name="denyalless-networkfilter-element"></a><span data-ttu-id="c1d30-103">Elemento denyAllESS (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="c1d30-103">denyAllESS (networkFilter) Element</span></span>

<span data-ttu-id="c1d30-104">O elemento denyAllESS (networkFilter) especifica se o acesso a todas as redes de infraestrutura está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c1d30-104">The denyAllESS (networkFilter) element specifies if access to all infrastructure networks is blocked.</span></span> <span data-ttu-id="c1d30-105">Quando **denyAllESS** tem um valor de true, os computadores não podem se conectar a uma rede de infraestrutura; caso contrário, os computadores podem se conectar a redes de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c1d30-105">When **denyAllESS** has a value of TRUE, machines cannot connect to an infrastructure network; otherwise, machines may connect to infrastructure networks.</span></span>

<span data-ttu-id="c1d30-106">O valor padrão para esse elemento é FALSE.</span><span class="sxs-lookup"><span data-stu-id="c1d30-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="c1d30-107">Se **denyAllESS** não for especificado em um perfil, por padrão, os computadores poderão se conectar a redes de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c1d30-107">If **denyAllESS** is not specified in a profile, then by default machines may connect to infrastructure networks.</span></span>

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

<span data-ttu-id="c1d30-108">O elemento **denyAllESS** é definido pelo elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d30-108">The **denyAllESS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d30-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1d30-109">Requirements</span></span>



| <span data-ttu-id="c1d30-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1d30-110">Requirement</span></span> | <span data-ttu-id="c1d30-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c1d30-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1d30-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1d30-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d30-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1d30-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1d30-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d30-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1d30-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1d30-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1d30-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="c1d30-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c1d30-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="c1d30-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="c1d30-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="c1d30-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c1d30-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="c1d30-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




