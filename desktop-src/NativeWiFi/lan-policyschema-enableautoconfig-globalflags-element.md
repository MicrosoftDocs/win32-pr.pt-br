---
description: Especifica se os computadores usam o serviço de configuração automática interno para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1 X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: Elemento enableAutoConfig (globalFlags) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662588"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a><span data-ttu-id="7478c-103">Elemento enableAutoConfig (globalFlags) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="7478c-103">enableAutoConfig (globalFlags) Element (LAN_policy)</span></span>

<span data-ttu-id="7478c-104">O elemento **enableAutoConfig** (globalFlags) especifica se os computadores usam o serviço de configuração automática interno para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="7478c-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span>

<span data-ttu-id="7478c-105">Quando **enableAutoConfig** tem um valor de false, os computadores não devem usar o serviço de configuração automática interno para gerenciar conexões que exigem autenticação de camada 2.</span><span class="sxs-lookup"><span data-stu-id="7478c-105">When **enableAutoConfig** has a value of FALSE, machines must not use built-in automatic configuration service to manage connections that require layer 2 authentication.</span></span> <span data-ttu-id="7478c-106">Em vez disso, a rede especificada no elemento [**ProfileList**](lan-policyschema-profilelist-lanpolicy-element.md) é a única rede disponível para conexão.</span><span class="sxs-lookup"><span data-stu-id="7478c-106">Instead, the network specified in the [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) element is the only network available for connection.</span></span> <span data-ttu-id="7478c-107">O serviço de configuração automática responderá apenas às solicitações para habilitar o serviço.</span><span class="sxs-lookup"><span data-stu-id="7478c-107">The automatic configuration service will only respond to requests to enable the service.</span></span>

<span data-ttu-id="7478c-108">Quando **enableAutoConfig** tem um valor de true, os computadores podem usar o serviço de configuração automática interno para se conectar a redes com fio que exigem autenticação de camada 2.</span><span class="sxs-lookup"><span data-stu-id="7478c-108">When **enableAutoConfig** has a value of TRUE, machines may use the built-in automatic configuration service to connect to wired networks that require layer 2 authentication.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="7478c-109">O elemento **enableAutoConfig** é definido pelo elemento [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7478c-109">The **enableAutoConfig** element is defined by the [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7478c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7478c-110">Requirements</span></span>



| <span data-ttu-id="7478c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7478c-111">Requirement</span></span> | <span data-ttu-id="7478c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7478c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7478c-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7478c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7478c-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7478c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7478c-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7478c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7478c-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7478c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7478c-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="7478c-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="7478c-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="7478c-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7478c-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="7478c-119">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="7478c-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="7478c-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7478c-121">**globalFlags (LANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="7478c-121">**globalFlags (LANPolicy)**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




