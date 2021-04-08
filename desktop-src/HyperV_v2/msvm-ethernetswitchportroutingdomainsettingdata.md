---
description: Representa os dados de configuração de domínio de roteamento.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Classe Msvm_EthernetSwitchPortRoutingDomainSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837515"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a><span data-ttu-id="dd992-103">\_Classe Msvm EthernetSwitchPortRoutingDomainSettingData</span><span class="sxs-lookup"><span data-stu-id="dd992-103">Msvm\_EthernetSwitchPortRoutingDomainSettingData class</span></span>

<span data-ttu-id="dd992-104">Representa os dados de configuração de domínio de roteamento.</span><span class="sxs-lookup"><span data-stu-id="dd992-104">Represents the routing domain setting data.</span></span>

<span data-ttu-id="dd992-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dd992-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd992-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd992-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a><span data-ttu-id="dd992-107">Membros</span><span class="sxs-lookup"><span data-stu-id="dd992-107">Members</span></span>

<span data-ttu-id="dd992-108">A classe **Msvm \_ EthernetSwitchPortRoutingDomainSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dd992-108">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="dd992-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd992-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd992-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd992-110">Properties</span></span>

<span data-ttu-id="dd992-111">A classe **Msvm \_ EthernetSwitchPortRoutingDomainSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dd992-111">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd992-112">**IsolationIdList**</span><span class="sxs-lookup"><span data-stu-id="dd992-112">**IsolationIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd992-113">Tipo de dados: matriz **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd992-113">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="dd992-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dd992-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd992-115">Qualificadores: **WmiDataId** (3), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="dd992-115">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="dd992-116">As IDs de VirtualSubnetId ou VLAN para os domínios de roteamento.</span><span class="sxs-lookup"><span data-stu-id="dd992-116">The VirtualSubnetId or VLAN IDs for the routing domains.</span></span>

</dd> <dt>

<span data-ttu-id="dd992-117">**IsolationIdNameList**</span><span class="sxs-lookup"><span data-stu-id="dd992-117">**IsolationIdNameList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd992-118">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dd992-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd992-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dd992-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd992-120">Qualificadores: **WmiDataId** (4), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="dd992-120">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="dd992-121">A matriz de nome amigável VirtualSubnetId ou VLAN.</span><span class="sxs-lookup"><span data-stu-id="dd992-121">The VirtualSubnetId or VLAN friendly name array.</span></span>

</dd> <dt>

<span data-ttu-id="dd992-122">**RoutingDomainGuid**</span><span class="sxs-lookup"><span data-stu-id="dd992-122">**RoutingDomainGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd992-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dd992-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd992-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dd992-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd992-125">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="dd992-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="dd992-126">O GUID do domínio de roteamento.</span><span class="sxs-lookup"><span data-stu-id="dd992-126">The routing domain GUID.</span></span>

</dd> <dt>

<span data-ttu-id="dd992-127">**RoutingDomainName**</span><span class="sxs-lookup"><span data-stu-id="dd992-127">**RoutingDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd992-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dd992-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd992-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dd992-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd992-130">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="dd992-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="dd992-131">O nome amigável do domínio de roteamento.</span><span class="sxs-lookup"><span data-stu-id="dd992-131">The routing domain friendly name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd992-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd992-132">Requirements</span></span>



| <span data-ttu-id="dd992-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd992-133">Requirement</span></span> | <span data-ttu-id="dd992-134">Valor</span><span class="sxs-lookup"><span data-stu-id="dd992-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd992-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd992-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dd992-136">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dd992-136">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dd992-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd992-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dd992-138">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dd992-138">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dd992-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd992-139">Namespace</span></span><br/>                | <span data-ttu-id="dd992-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dd992-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd992-141">MOF</span><span class="sxs-lookup"><span data-stu-id="dd992-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd992-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd992-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd992-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dd992-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd992-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd992-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd992-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd992-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd992-146">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="dd992-146">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

