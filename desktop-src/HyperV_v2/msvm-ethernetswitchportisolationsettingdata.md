---
description: Representa os dados de configuração de isolamento.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Classe Msvm_EthernetSwitchPortIsolationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770404"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a><span data-ttu-id="57952-103">\_Classe Msvm EthernetSwitchPortIsolationSettingData</span><span class="sxs-lookup"><span data-stu-id="57952-103">Msvm\_EthernetSwitchPortIsolationSettingData class</span></span>

<span data-ttu-id="57952-104">Representa os dados de configuração de isolamento.</span><span class="sxs-lookup"><span data-stu-id="57952-104">Represents the Isolation setting data.</span></span>

<span data-ttu-id="57952-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="57952-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="57952-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57952-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="57952-107">Membros</span><span class="sxs-lookup"><span data-stu-id="57952-107">Members</span></span>

<span data-ttu-id="57952-108">A classe **Msvm \_ EthernetSwitchPortIsolationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="57952-108">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="57952-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57952-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57952-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57952-110">Properties</span></span>

<span data-ttu-id="57952-111">A classe **Msvm \_ EthernetSwitchPortIsolationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="57952-111">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57952-112">**AllowUntaggedTraffic**</span><span class="sxs-lookup"><span data-stu-id="57952-112">**AllowUntaggedTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57952-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="57952-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57952-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="57952-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="57952-115">Qualificadores: **WmiDataId** (2), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="57952-115">Qualifiers: **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="57952-116">Se a porta tem permissão para enviar/receber tráfego não marcado.</span><span class="sxs-lookup"><span data-stu-id="57952-116">Whether the port is allowed to send/receive untagged traffic.</span></span>

</dd> <dt>

<span data-ttu-id="57952-117">**Defaultisolaid**</span><span class="sxs-lookup"><span data-stu-id="57952-117">**DefaultIsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57952-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57952-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57952-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="57952-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="57952-120">Qualificadores: **WmiDataId** (3), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="57952-120">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="57952-121">O VirtualSubnetId ou a VLAN padrão que será definida em todos os tráfegos de envio/recebimento se **AllowedUntaggedTraffic** for **true**.</span><span class="sxs-lookup"><span data-stu-id="57952-121">The default VirtualSubnetId or VLAN that will be set on all send/receive traffic if **AllowedUntaggedTraffic** is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="57952-122">**EnableMultiTenantStack**</span><span class="sxs-lookup"><span data-stu-id="57952-122">**EnableMultiTenantStack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57952-123">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="57952-123">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57952-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="57952-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="57952-125">Qualificadores: **WmiDataId** (4), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="57952-125">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="57952-126">Se **for true**, a pilha de rede na VM poderá acessar a configuração de isolamento.</span><span class="sxs-lookup"><span data-stu-id="57952-126">If **true**, the network stack in the VM will be able to access the isolation configuration.</span></span> <span data-ttu-id="57952-127">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="57952-127">The default value is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="57952-128">**IsolationMode**</span><span class="sxs-lookup"><span data-stu-id="57952-128">**IsolationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57952-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57952-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57952-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="57952-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="57952-131">Qualificadores: **WmiDataId** (1), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="57952-131">Qualifiers: **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="57952-132">Se a porta está usando **VLAN** ou **VirtualSubnetId** para isolamento.</span><span class="sxs-lookup"><span data-stu-id="57952-132">Whether the port is using **VLAN** or **VirtualSubnetId** for isolation.</span></span> <span data-ttu-id="57952-133">**NativeVirtualSubnetId** é usado para redes baseadas em VIRTUALSUBNETID do WNV.</span><span class="sxs-lookup"><span data-stu-id="57952-133">**NativeVirtualSubnetId** is used for WNV VirtualSubnetId-based networks.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="57952-134">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="57952-134">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

<span data-ttu-id="57952-135">**NativeVirtualSubnetId** (1)</span><span class="sxs-lookup"><span data-stu-id="57952-135">**NativeVirtualSubnetId** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

<span data-ttu-id="57952-136">**ExternalVirtualSubnetId** (2)</span><span class="sxs-lookup"><span data-stu-id="57952-136">**ExternalVirtualSubnetId** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

<span data-ttu-id="57952-137">**VLAN** (3)</span><span class="sxs-lookup"><span data-stu-id="57952-137">**VLAN** (3)</span></span>


<span data-ttu-id="57952-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="57952-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="57952-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57952-139">Requirements</span></span>



| <span data-ttu-id="57952-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="57952-140">Requirement</span></span> | <span data-ttu-id="57952-141">Valor</span><span class="sxs-lookup"><span data-stu-id="57952-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57952-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57952-142">Minimum supported client</span></span><br/> | <span data-ttu-id="57952-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="57952-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="57952-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57952-144">Minimum supported server</span></span><br/> | <span data-ttu-id="57952-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="57952-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="57952-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="57952-146">Namespace</span></span><br/>                | <span data-ttu-id="57952-147">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="57952-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="57952-148">MOF</span><span class="sxs-lookup"><span data-stu-id="57952-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57952-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57952-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57952-150">DLL</span><span class="sxs-lookup"><span data-stu-id="57952-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57952-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57952-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57952-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="57952-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57952-153">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="57952-153">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

