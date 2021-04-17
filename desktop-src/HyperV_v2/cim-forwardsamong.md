---
description: Representa uma associação na qual os pontos de extremidade de protocolo dependem de um serviço de encaminhamento para encaminhar dados.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: Classe CIM_ForwardsAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b584f6472d8fbe3eb738d87652b796d9bb617f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768762"
---
# <a name="cim_forwardsamong-class"></a><span data-ttu-id="faad5-103">\_Classe CIM ForwardsAmong</span><span class="sxs-lookup"><span data-stu-id="faad5-103">CIM\_ForwardsAmong class</span></span>

<span data-ttu-id="faad5-104">Representa uma associação na qual os pontos de extremidade de protocolo dependem de um serviço de encaminhamento para encaminhar dados.</span><span class="sxs-lookup"><span data-stu-id="faad5-104">Represents an association in which protocol endpoints depend on a forwarding service to forward data.</span></span>

## <a name="syntax"></a><span data-ttu-id="faad5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="faad5-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="faad5-106">Membros</span><span class="sxs-lookup"><span data-stu-id="faad5-106">Members</span></span>

<span data-ttu-id="faad5-107">A classe **CIM \_ ForwardsAmong** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="faad5-107">The **CIM\_ForwardsAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="faad5-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="faad5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="faad5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="faad5-109">Properties</span></span>

<span data-ttu-id="faad5-110">A classe **CIM \_ ForwardsAmong** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="faad5-110">The **CIM\_ForwardsAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="faad5-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="faad5-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faad5-112">Tipo de dados: **CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="faad5-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="faad5-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="faad5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="faad5-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="faad5-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="faad5-115">Os pontos de extremidade de protocolo enviam e recebem os dados encaminhados.</span><span class="sxs-lookup"><span data-stu-id="faad5-115">The protocol endpoints send and receive the forwarded data.</span></span>

</dd> <dt>

<span data-ttu-id="faad5-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="faad5-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faad5-117">Tipo de dados: **CIM \_ ForwardingService**</span><span class="sxs-lookup"><span data-stu-id="faad5-117">Data type: **CIM\_ForwardingService**</span></span>
</dt> <dt>

<span data-ttu-id="faad5-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="faad5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="faad5-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="faad5-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="faad5-120">O serviço de encaminhamento que encaminha os dados.</span><span class="sxs-lookup"><span data-stu-id="faad5-120">The forwarding service that forwards the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="faad5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faad5-121">Requirements</span></span>



| <span data-ttu-id="faad5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="faad5-122">Requirement</span></span> | <span data-ttu-id="faad5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="faad5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faad5-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faad5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="faad5-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="faad5-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="faad5-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faad5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="faad5-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="faad5-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="faad5-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="faad5-128">Namespace</span></span><br/>                | <span data-ttu-id="faad5-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="faad5-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="faad5-130">MOF</span><span class="sxs-lookup"><span data-stu-id="faad5-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faad5-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faad5-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="faad5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="faad5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faad5-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="faad5-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="faad5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="faad5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faad5-135">**\_SERVICESAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="faad5-135">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> </dl>

 

