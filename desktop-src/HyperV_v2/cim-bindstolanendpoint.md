---
description: Representa uma associação em que um \_ objeto CIM ServiceAccessPoint ou CIM é \_ dependente de um \_ objeto LANEndpoint CIM subjacente no mesmo sistema.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: Classe CIM_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811883"
---
# <a name="cim_bindstolanendpoint-class"></a><span data-ttu-id="83346-103">\_Classe CIM BindsToLANEndpoint</span><span class="sxs-lookup"><span data-stu-id="83346-103">CIM\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="83346-104">Representa uma associação em que um objeto [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ou CIM é dependente de um [**objeto \_ LANEndpoint CIM**](cim-lanendpoint.md) subjacente no mesmo sistema. [**\_**](cim-protocolendpoint.md)</span><span class="sxs-lookup"><span data-stu-id="83346-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object depends on an underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object on the same system.</span></span>

## <a name="syntax"></a><span data-ttu-id="83346-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83346-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a><span data-ttu-id="83346-106">Membros</span><span class="sxs-lookup"><span data-stu-id="83346-106">Members</span></span>

<span data-ttu-id="83346-107">A classe **CIM \_ BindsToLANEndpoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="83346-107">The **CIM\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="83346-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83346-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83346-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83346-109">Properties</span></span>

<span data-ttu-id="83346-110">A classe **CIM \_ BindsToLANEndpoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="83346-110">The **CIM\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83346-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="83346-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83346-112">Tipo de dados: **CIM \_ LANEndpoint**</span><span class="sxs-lookup"><span data-stu-id="83346-112">Data type: **CIM\_LANEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="83346-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83346-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83346-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="83346-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="83346-115">O objeto [**CIM \_ LANEndpoint**](cim-lanendpoint.md) subjacente.</span><span class="sxs-lookup"><span data-stu-id="83346-115">The underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="83346-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="83346-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83346-117">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="83346-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="83346-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83346-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83346-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="83346-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="83346-120">O objeto [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ou [**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md) que é dependente do [**\_ LANEndpoint do CIM**](cim-lanendpoint.md).</span><span class="sxs-lookup"><span data-stu-id="83346-120">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object that is dependent on the [**CIM\_LANEndpoint**](cim-lanendpoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="83346-121">**Conjunto de quadros**</span><span class="sxs-lookup"><span data-stu-id="83346-121">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83346-122">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83346-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83346-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83346-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83346-124">O método de enquadramento para o ponto de acesso do serviço de camada superior ou o EndPoint do protocolo.</span><span class="sxs-lookup"><span data-stu-id="83346-124">The framing method for the upper layer service access point or protocol endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="83346-125">O 802.3 bruto só é conhecido por ser usado com o protocolo IPX.</span><span class="sxs-lookup"><span data-stu-id="83346-125">Raw802.3 is only known to be used with the IPX protocol.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83346-126">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="83346-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="83346-127">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="83346-127">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.2"></span>

<span data-ttu-id="83346-128">**802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="83346-128">**802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

<span data-ttu-id="83346-129">**Snap** (3)</span><span class="sxs-lookup"><span data-stu-id="83346-129">**SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

<span data-ttu-id="83346-130">**802.3 bruto** (4)</span><span class="sxs-lookup"><span data-stu-id="83346-130">**Raw802.3** (4)</span></span>


<span data-ttu-id="83346-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="83346-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="83346-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83346-132">Requirements</span></span>



| <span data-ttu-id="83346-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="83346-133">Requirement</span></span> | <span data-ttu-id="83346-134">Valor</span><span class="sxs-lookup"><span data-stu-id="83346-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83346-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83346-135">Minimum supported client</span></span><br/> | <span data-ttu-id="83346-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="83346-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="83346-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83346-137">Minimum supported server</span></span><br/> | <span data-ttu-id="83346-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83346-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="83346-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="83346-139">Namespace</span></span><br/>                | <span data-ttu-id="83346-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="83346-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="83346-141">MOF</span><span class="sxs-lookup"><span data-stu-id="83346-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83346-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83346-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83346-143">DLL</span><span class="sxs-lookup"><span data-stu-id="83346-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83346-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83346-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="83346-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="83346-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83346-146">**\_BINDSTO CIM**</span><span class="sxs-lookup"><span data-stu-id="83346-146">**CIM\_BindsTo**</span></span>](cim-bindsto.md)
</dt> </dl>

 

