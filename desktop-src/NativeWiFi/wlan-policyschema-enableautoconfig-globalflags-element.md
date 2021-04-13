---
description: Especifica se os computadores usam o serviço interno de configuração automática (autoconfiguração) para gerenciar conexões sem fio.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
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
ms.openlocfilehash: c03e4c2afa9e8e98c07e1bc0cdec4099d3260aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501558"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a><span data-ttu-id="a1408-103">Elemento enableAutoConfig (globalFlags) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="a1408-103">enableAutoConfig (globalFlags) Element (LAN_policy)</span></span>

<span data-ttu-id="a1408-104">O elemento **enableAutoConfig** (globalFlags) especifica se os computadores usam o serviço interno de configuração automática (AutoConfig) para gerenciar conexões sem fio.</span><span class="sxs-lookup"><span data-stu-id="a1408-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <span data-ttu-id="a1408-105">Quando **enableAutoConfig** tem um valor de false, os computadores não devem usar o autoConfig para gerenciar conexões sem fio e o serviço de configuração automática responde apenas a solicitações para habilitar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a1408-105">When **enableAutoConfig** has a value of FALSE, machines must not use AutoConfig to manage wireless connections, and the AutoConfig service only responds to requests to enable the service.</span></span> <span data-ttu-id="a1408-106">Quando **enableAutoConfig** tem um valor de true, os computadores podem usar o serviço de configuração automática.</span><span class="sxs-lookup"><span data-stu-id="a1408-106">When **enableAutoConfig** has a value of TRUE, machines may use the AutoConfig service.</span></span>

<span data-ttu-id="a1408-107">Esse elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a1408-107">This element is mandatory.</span></span> <span data-ttu-id="a1408-108">Quando um perfil é criado pelo serviço de configuração automática, esse elemento terá o valor padrão de TRUE.</span><span class="sxs-lookup"><span data-stu-id="a1408-108">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="a1408-109">O elemento **enableAutoConfig** é definido pelo elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a1408-109">The **enableAutoConfig** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1408-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1408-110">Requirements</span></span>



| <span data-ttu-id="a1408-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1408-111">Requirement</span></span> | <span data-ttu-id="a1408-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a1408-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1408-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1408-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a1408-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1408-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1408-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1408-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a1408-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1408-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1408-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1408-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1408-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a1408-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a1408-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="a1408-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="a1408-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a1408-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a1408-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="a1408-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




