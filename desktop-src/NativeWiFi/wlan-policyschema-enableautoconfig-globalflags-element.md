---
description: Especifica se os computadores usam o serviço interno de configuração automática (autoconfiguração) para gerenciar conexões sem fio.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: Elemento enableAutoConfig (globalFlags) (LAN_policy) para WLAN
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
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188039"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a><span data-ttu-id="de86b-103">Elemento enableAutoConfig (globalFlags) (LAN_policy) para WLAN</span><span class="sxs-lookup"><span data-stu-id="de86b-103">enableAutoConfig (globalFlags) Element (LAN_policy) for WLAN</span></span> 

<span data-ttu-id="de86b-104">O elemento **enableAutoConfig** (globalFlags) especifica se os computadores usam o serviço interno de configuração automática (AutoConfig) para gerenciar conexões sem fio.</span><span class="sxs-lookup"><span data-stu-id="de86b-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <span data-ttu-id="de86b-105">Quando **enableAutoConfig** tem um valor de false, os computadores não devem usar o autoConfig para gerenciar conexões sem fio e o serviço de configuração automática responde apenas a solicitações para habilitar o serviço.</span><span class="sxs-lookup"><span data-stu-id="de86b-105">When **enableAutoConfig** has a value of FALSE, machines must not use AutoConfig to manage wireless connections, and the AutoConfig service only responds to requests to enable the service.</span></span> <span data-ttu-id="de86b-106">Quando **enableAutoConfig** tem um valor de true, os computadores podem usar o serviço de configuração automática.</span><span class="sxs-lookup"><span data-stu-id="de86b-106">When **enableAutoConfig** has a value of TRUE, machines may use the AutoConfig service.</span></span>

<span data-ttu-id="de86b-107">Esse elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="de86b-107">This element is mandatory.</span></span> <span data-ttu-id="de86b-108">Quando um perfil é criado pelo serviço de configuração automática, esse elemento terá o valor padrão de TRUE.</span><span class="sxs-lookup"><span data-stu-id="de86b-108">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="de86b-109">O elemento **enableAutoConfig** é definido pelo elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="de86b-109">The **enableAutoConfig** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="de86b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de86b-110">Requirements</span></span>



| <span data-ttu-id="de86b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="de86b-111">Requirement</span></span> | <span data-ttu-id="de86b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="de86b-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de86b-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de86b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="de86b-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de86b-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de86b-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de86b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="de86b-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de86b-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de86b-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="de86b-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="de86b-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="de86b-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="de86b-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="de86b-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="de86b-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="de86b-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="de86b-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="de86b-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




