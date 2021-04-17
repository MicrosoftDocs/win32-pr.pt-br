---
description: Representa os dados de configuração de LAN virtual (VLAN).
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Classe Msvm_EthernetSwitchPortVlanSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fce6416696a99e5d928b774e2ba2a05b1dc21d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755101"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a><span data-ttu-id="e557a-103">\_Classe Msvm EthernetSwitchPortVlanSettingData</span><span class="sxs-lookup"><span data-stu-id="e557a-103">Msvm\_EthernetSwitchPortVlanSettingData class</span></span>

<span data-ttu-id="e557a-104">Representa os dados de configuração de LAN virtual (VLAN).</span><span class="sxs-lookup"><span data-stu-id="e557a-104">Represents the virtual LAN (VLAN) setting data.</span></span>

<span data-ttu-id="e557a-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e557a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e557a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e557a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a><span data-ttu-id="e557a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e557a-107">Members</span></span>

<span data-ttu-id="e557a-108">A classe **Msvm \_ EthernetSwitchPortVlanSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e557a-108">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e557a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e557a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e557a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e557a-110">Properties</span></span>

<span data-ttu-id="e557a-111">A classe **Msvm \_ EthernetSwitchPortVlanSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e557a-111">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e557a-112">**AccessVlanId**</span><span class="sxs-lookup"><span data-stu-id="e557a-112">**AccessVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e557a-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-115">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-116">Especifica o identificador de VLAN no modo de acesso.</span><span class="sxs-lookup"><span data-stu-id="e557a-116">Specifies the VLAN identifier in access mode.</span></span>

</dd> <dt>

<span data-ttu-id="e557a-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e557a-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e557a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e557a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e557a-120">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e557a-120">A short description of the object.</span></span> <span data-ttu-id="e557a-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de VLAN da porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="e557a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="e557a-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e557a-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e557a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e557a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e557a-125">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="e557a-125">A description of the object.</span></span> <span data-ttu-id="e557a-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa os dados de configuração de VLAN.".</span><span class="sxs-lookup"><span data-stu-id="e557a-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the vlan setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="e557a-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e557a-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e557a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e557a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e557a-130">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e557a-130">A display name for the object.</span></span> <span data-ttu-id="e557a-131">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de VLAN da porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="e557a-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="e557a-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e557a-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e557a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e557a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e557a-135">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e557a-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e557a-136">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="e557a-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e557a-137">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e557a-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e557a-138">**NativeVlanId**</span><span class="sxs-lookup"><span data-stu-id="e557a-138">**NativeVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e557a-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-141">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-141">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-142">Especifica o identificador de VLAN no modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="e557a-142">Specifies the VLAN identifier in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="e557a-143">**OperationMode**</span><span class="sxs-lookup"><span data-stu-id="e557a-143">**OperationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e557a-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-146">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-146">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-147">Especifica o modo de operação de VLAN.</span><span class="sxs-lookup"><span data-stu-id="e557a-147">Specifies the VLAN operation mode.</span></span>

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="e557a-148">**Acesso** (1)</span><span class="sxs-lookup"><span data-stu-id="e557a-148">**Access** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="e557a-149">**Tronco** (2)</span><span class="sxs-lookup"><span data-stu-id="e557a-149">**Trunk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

<span data-ttu-id="e557a-150">**Privado** (3)</span><span class="sxs-lookup"><span data-stu-id="e557a-150">**Private** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e557a-151">**PrimaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="e557a-151">**PrimaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-152">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e557a-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-154">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-154">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-155">Especifica o identificador de VLAN primário no modo particular.</span><span class="sxs-lookup"><span data-stu-id="e557a-155">Specifies the primary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="e557a-156">**PruneVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="e557a-156">**PruneVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-157">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e557a-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e557a-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-159">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-160">Especifica o bitmap de identificador de VLAN de remoção no modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="e557a-160">Specifies the prune VLAN identifier bitmap in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="e557a-161">**PvlanMode**</span><span class="sxs-lookup"><span data-stu-id="e557a-161">**PvlanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e557a-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-164">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-164">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-165">Especifica o modo de VLAN privada.</span><span class="sxs-lookup"><span data-stu-id="e557a-165">Specifies the private VLAN mode.</span></span>

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

<span data-ttu-id="e557a-166">**Isolado** (1)</span><span class="sxs-lookup"><span data-stu-id="e557a-166">**Isolated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

<span data-ttu-id="e557a-167">**Comunidade** (2)</span><span class="sxs-lookup"><span data-stu-id="e557a-167">**Community** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

<span data-ttu-id="e557a-168">**Promíscuo** (3)</span><span class="sxs-lookup"><span data-stu-id="e557a-168">**Promiscuous** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e557a-169">**SecondaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="e557a-169">**SecondaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-170">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e557a-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e557a-171">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-171">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-172">Qualificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-172">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-173">Especifica o identificador de VLAN secundário no modo privado.</span><span class="sxs-lookup"><span data-stu-id="e557a-173">Specifies the secondary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="e557a-174">**SecondaryVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="e557a-174">**SecondaryVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-175">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e557a-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e557a-176">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-177">Qualificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-177">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-178">Especifica o bitmap do identificador de VLAN secundário no modo privado.</span><span class="sxs-lookup"><span data-stu-id="e557a-178">Specifies the secondary VLAN identifier bitmap in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="e557a-179">**TrunkVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="e557a-179">**TrunkVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e557a-180">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e557a-180">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e557a-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e557a-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e557a-182">Qualificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e557a-182">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e557a-183">Especifica o bitmap do identificador de VLAN de tronco no modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="e557a-183">Specifies the trunk VLAN identifier bitmap in trunk mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e557a-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e557a-184">Requirements</span></span>



| <span data-ttu-id="e557a-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="e557a-185">Requirement</span></span> | <span data-ttu-id="e557a-186">Valor</span><span class="sxs-lookup"><span data-stu-id="e557a-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e557a-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e557a-187">Minimum supported client</span></span><br/> | <span data-ttu-id="e557a-188">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e557a-188">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e557a-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e557a-189">Minimum supported server</span></span><br/> | <span data-ttu-id="e557a-190">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e557a-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e557a-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="e557a-191">Namespace</span></span><br/>                | <span data-ttu-id="e557a-192">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e557a-192">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e557a-193">MOF</span><span class="sxs-lookup"><span data-stu-id="e557a-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e557a-194"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e557a-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e557a-195">DLL</span><span class="sxs-lookup"><span data-stu-id="e557a-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e557a-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e557a-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

