---
description: Representa as configurações de agrupamento NIC do comutador.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Classe Msvm_VirtualEthernetSwitchNicTeamingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663605"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a><span data-ttu-id="c45c9-103">\_Classe Msvm VirtualEthernetSwitchNicTeamingSettingData</span><span class="sxs-lookup"><span data-stu-id="c45c9-103">Msvm\_VirtualEthernetSwitchNicTeamingSettingData class</span></span>

<span data-ttu-id="c45c9-104">Representa as configurações de agrupamento NIC do comutador.</span><span class="sxs-lookup"><span data-stu-id="c45c9-104">Represents the switch nic teaming settings.</span></span>

<span data-ttu-id="c45c9-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c45c9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c45c9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c45c9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a><span data-ttu-id="c45c9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c45c9-107">Members</span></span>

<span data-ttu-id="c45c9-108">A classe **Msvm \_ VirtualEthernetSwitchNicTeamingSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c45c9-108">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c45c9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c45c9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c45c9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c45c9-110">Properties</span></span>

<span data-ttu-id="c45c9-111">A classe **Msvm \_ VirtualEthernetSwitchNicTeamingSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c45c9-111">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c45c9-112">**LoadBalancingAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="c45c9-112">**LoadBalancingAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c45c9-113">Tipo de dados: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c45c9-113">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="c45c9-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c45c9-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c45c9-115">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c45c9-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c45c9-116">O algoritmo de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="c45c9-116">The load balancing algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="c45c9-117">**TeamingMode**</span><span class="sxs-lookup"><span data-stu-id="c45c9-117">**TeamingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c45c9-118">Tipo de dados: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c45c9-118">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="c45c9-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c45c9-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c45c9-120">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="c45c9-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c45c9-121">O modo de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="c45c9-121">The teaming mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c45c9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c45c9-122">Requirements</span></span>



| <span data-ttu-id="c45c9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c45c9-123">Requirement</span></span> | <span data-ttu-id="c45c9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c45c9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c45c9-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c45c9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c45c9-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c45c9-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c45c9-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c45c9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c45c9-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c45c9-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c45c9-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c45c9-129">Namespace</span></span><br/>                | <span data-ttu-id="c45c9-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c45c9-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c45c9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c45c9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c45c9-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c45c9-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c45c9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c45c9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c45c9-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c45c9-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c45c9-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c45c9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45c9-136">**Msvm \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="c45c9-136">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




