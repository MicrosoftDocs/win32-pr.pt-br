---
description: Representa os dados de status do recurso de largura de banda da porta.
ms.assetid: 1f7be0dd-3d2f-49ef-aff0-cb162389194a
title: Classe Msvm_EthernetSwitchPortBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthData
- Msvm_EthernetSwitchPortBandwidthData.InstanceID
- Msvm_EthernetSwitchPortBandwidthData.Caption
- Msvm_EthernetSwitchPortBandwidthData.Description
- Msvm_EthernetSwitchPortBandwidthData.ElementName
- Msvm_EthernetSwitchPortBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.SystemName
- Msvm_EthernetSwitchPortBandwidthData.DeviceCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.DeviceID
- Msvm_EthernetSwitchPortBandwidthData.CreationClassName
- Msvm_EthernetSwitchPortBandwidthData.Name
- Msvm_EthernetSwitchPortBandwidthData.CurrentBandwidthReservationPercentage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55e8ad735d712bdd388e42b1f4174ee1a78af184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750843"
---
# <a name="msvm_ethernetswitchportbandwidthdata-class"></a><span data-ttu-id="09880-103">\_Classe Msvm EthernetSwitchPortBandwidthData</span><span class="sxs-lookup"><span data-stu-id="09880-103">Msvm\_EthernetSwitchPortBandwidthData class</span></span>

<span data-ttu-id="09880-104">Representa os dados de status do recurso de largura de banda da porta.</span><span class="sxs-lookup"><span data-stu-id="09880-104">Represents the port bandwidth feature status data.</span></span>

<span data-ttu-id="09880-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="09880-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09880-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09880-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthData : Msvm_EthernetPortData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Feature Status";
  string Description = "Represents the port bandwidth feature status data.";
  string ElementName = "Ethernet Switch Port Bandwidth Feature Status";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName = "Msvm_EthernetSwitchPortBandwidthData";
  string Name;
  uint32 CurrentBandwidthReservationPercentage = 0;
};
```

## <a name="members"></a><span data-ttu-id="09880-107">Membros</span><span class="sxs-lookup"><span data-stu-id="09880-107">Members</span></span>

<span data-ttu-id="09880-108">A classe **Msvm \_ EthernetSwitchPortBandwidthData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="09880-108">The **Msvm\_EthernetSwitchPortBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="09880-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09880-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09880-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09880-110">Properties</span></span>

<span data-ttu-id="09880-111">A classe **Msvm \_ EthernetSwitchPortBandwidthData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="09880-111">The **Msvm\_EthernetSwitchPortBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09880-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="09880-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09880-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="09880-115">A short description of the object.</span></span> <span data-ttu-id="09880-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "status do recurso de largura de banda da porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="09880-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="09880-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09880-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09880-120">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="09880-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="09880-121">O nome da subclasse usada na criação desta instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="09880-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="09880-122">Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ EthernetSwitchPortBandwidthData".</span><span class="sxs-lookup"><span data-stu-id="09880-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortBandwidthData".</span></span>

</dd> <dt>

<span data-ttu-id="09880-123">**CurrentBandwidthReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="09880-123">**CurrentBandwidthReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09880-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09880-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="09880-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="09880-126">Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="09880-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="09880-127">A porcentagem atual da largura de banda reservada para esta porta.</span><span class="sxs-lookup"><span data-stu-id="09880-127">The current percentage of bandwidth reserved for this port.</span></span>

</dd> <dt>

<span data-ttu-id="09880-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="09880-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09880-131">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="09880-131">A description of the object.</span></span> <span data-ttu-id="09880-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa os dados de status do recurso de largura de banda da porta.".</span><span class="sxs-lookup"><span data-stu-id="09880-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="09880-133">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09880-133">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09880-136">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="09880-136">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="09880-137">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="09880-137">The scoping system's creation class name.</span></span> <span data-ttu-id="09880-138">Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="09880-138">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="09880-139">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="09880-139">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09880-142">Qualificadores: **chave**, **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="09880-142">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="09880-143">A ID do dispositivo da porta que abrange essa instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="09880-143">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="09880-144">Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="09880-144">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="09880-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="09880-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09880-148">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="09880-148">A display name for the object.</span></span> <span data-ttu-id="09880-149">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "status do recurso de largura de banda da porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="09880-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="09880-150">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09880-150">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09880-153">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="09880-153">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="09880-154">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="09880-154">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="09880-155">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09880-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09880-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="09880-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09880-159">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="09880-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="09880-160">Uma cadeia de caracteres que identifica exclusivamente essa instância de dados de porta dentro do escopo do comutador e da porta.</span><span class="sxs-lookup"><span data-stu-id="09880-160">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="09880-161">Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="09880-161">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="09880-162">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09880-162">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09880-165">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="09880-165">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="09880-166">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="09880-166">The scoping system's creation class name.</span></span> <span data-ttu-id="09880-167">Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="09880-167">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="09880-168">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="09880-168">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09880-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09880-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09880-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09880-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09880-171">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="09880-171">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="09880-172">O nome do comutador virtual que abrange essa instância de dados de porta.</span><span class="sxs-lookup"><span data-stu-id="09880-172">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="09880-173">Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="09880-173">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09880-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09880-174">Requirements</span></span>



| <span data-ttu-id="09880-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="09880-175">Requirement</span></span> | <span data-ttu-id="09880-176">Valor</span><span class="sxs-lookup"><span data-stu-id="09880-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09880-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09880-177">Minimum supported client</span></span><br/> | <span data-ttu-id="09880-178">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09880-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09880-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09880-179">Minimum supported server</span></span><br/> | <span data-ttu-id="09880-180">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09880-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09880-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="09880-181">Namespace</span></span><br/>                | <span data-ttu-id="09880-182">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="09880-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09880-183">MOF</span><span class="sxs-lookup"><span data-stu-id="09880-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09880-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09880-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09880-185">DLL</span><span class="sxs-lookup"><span data-stu-id="09880-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09880-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09880-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

