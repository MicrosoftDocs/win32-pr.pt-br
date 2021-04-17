---
description: Representa um serviço de comutador.
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: Classe CIM_SwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9abe6869c5b8ac61630091315e476ae232630717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769347"
---
# <a name="cim_switchservice-class"></a><span data-ttu-id="30f67-103">\_Classe CIM SwitchService</span><span class="sxs-lookup"><span data-stu-id="30f67-103">CIM\_SwitchService class</span></span>

<span data-ttu-id="30f67-104">Representa um serviço de comutador.</span><span class="sxs-lookup"><span data-stu-id="30f67-104">Represents a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f67-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30f67-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a><span data-ttu-id="30f67-106">Membros</span><span class="sxs-lookup"><span data-stu-id="30f67-106">Members</span></span>

<span data-ttu-id="30f67-107">A classe **CIM \_ SwitchService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="30f67-107">The **CIM\_SwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="30f67-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="30f67-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30f67-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="30f67-109">Properties</span></span>

<span data-ttu-id="30f67-110">A classe **CIM \_ SwitchService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="30f67-110">The **CIM\_SwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30f67-111">**BridgeAddress**</span><span class="sxs-lookup"><span data-stu-id="30f67-111">**BridgeAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30f67-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30f67-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30f67-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30f67-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30f67-114">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseBridgeAddress "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddressType**")</span><span class="sxs-lookup"><span data-stu-id="30f67-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseBridgeAddress"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddressType**")</span></span>
</dt> </dl>

<span data-ttu-id="30f67-115">O endereço do serviço de comutador, que é uma parte do identificador exclusivo do serviço.</span><span class="sxs-lookup"><span data-stu-id="30f67-115">The address of the switch service, which is a portion of the unique identifier of the service.</span></span>

</dd> <dt>

<span data-ttu-id="30f67-116">**BridgeAddressType**</span><span class="sxs-lookup"><span data-stu-id="30f67-116">**BridgeAddressType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30f67-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30f67-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30f67-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30f67-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30f67-119">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddress**")</span><span class="sxs-lookup"><span data-stu-id="30f67-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="30f67-120">O formato de endereçamento usado para a ponte e a propriedade **BridgeAddress** .</span><span class="sxs-lookup"><span data-stu-id="30f67-120">The addressing format used for the bridge and the **BridgeAddress** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="30f67-121">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="30f67-121">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="30f67-122">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="30f67-122">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="30f67-123">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="30f67-123">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

<span data-ttu-id="30f67-124">**Mac** (4)</span><span class="sxs-lookup"><span data-stu-id="30f67-124">**MAC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

<span data-ttu-id="30f67-125">**Prioridade de árvore de abrangência de Mac +** (5)</span><span class="sxs-lookup"><span data-stu-id="30f67-125">**MAC + Spanning Tree Priority** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="30f67-126">**Bridgetype**</span><span class="sxs-lookup"><span data-stu-id="30f67-126">**BridgeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30f67-127">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="30f67-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="30f67-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30f67-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30f67-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseType ")</span><span class="sxs-lookup"><span data-stu-id="30f67-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseType")</span></span>
</dt> </dl>

<span data-ttu-id="30f67-130">O tipo de serviço de alternância a ser executado.</span><span class="sxs-lookup"><span data-stu-id="30f67-130">The type of switching service to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="30f67-131">**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="30f67-131">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

<span data-ttu-id="30f67-132">**Somente transparente** (2)</span><span class="sxs-lookup"><span data-stu-id="30f67-132">**Transparent-only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

<span data-ttu-id="30f67-133">**Somente SourceRoute** (3)</span><span class="sxs-lookup"><span data-stu-id="30f67-133">**SourceRoute-only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

<span data-ttu-id="30f67-134">**Srt** (4)</span><span class="sxs-lookup"><span data-stu-id="30f67-134">**SRT** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="30f67-135">**NumPorts**</span><span class="sxs-lookup"><span data-stu-id="30f67-135">**NumPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30f67-136">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30f67-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30f67-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30f67-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30f67-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseNumPorts ")</span><span class="sxs-lookup"><span data-stu-id="30f67-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseNumPorts")</span></span>
</dt> </dl>

<span data-ttu-id="30f67-139">O número de portas de comutador controladas por esse serviço de comutação.</span><span class="sxs-lookup"><span data-stu-id="30f67-139">The number of switch ports controlled by this switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30f67-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f67-140">Requirements</span></span>



| <span data-ttu-id="30f67-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f67-141">Requirement</span></span> | <span data-ttu-id="30f67-142">Valor</span><span class="sxs-lookup"><span data-stu-id="30f67-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30f67-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30f67-143">Minimum supported client</span></span><br/> | <span data-ttu-id="30f67-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="30f67-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="30f67-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30f67-145">Minimum supported server</span></span><br/> | <span data-ttu-id="30f67-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="30f67-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="30f67-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="30f67-147">Namespace</span></span><br/>                | <span data-ttu-id="30f67-148">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="30f67-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="30f67-149">MOF</span><span class="sxs-lookup"><span data-stu-id="30f67-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30f67-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30f67-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30f67-151">DLL</span><span class="sxs-lookup"><span data-stu-id="30f67-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30f67-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30f67-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30f67-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="30f67-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f67-154">**\_FORWARDINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="30f67-154">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

