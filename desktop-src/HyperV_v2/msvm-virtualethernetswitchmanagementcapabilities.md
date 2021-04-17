---
description: Descreve os recursos do VirtualEthernetSwitchManagementService Msvm associado \_ .
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Classe Msvm_VirtualEthernetSwitchManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752873"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a><span data-ttu-id="bab9e-103">\_Classe Msvm VirtualEthernetSwitchManagementCapabilities</span><span class="sxs-lookup"><span data-stu-id="bab9e-103">Msvm\_VirtualEthernetSwitchManagementCapabilities class</span></span>

<span data-ttu-id="bab9e-104">Descreve os recursos do [**\_ VirtualEthernetSwitchManagementService Msvm**](msvm-virtualethernetswitchmanagementservice.md)associado.</span><span class="sxs-lookup"><span data-stu-id="bab9e-104">Describes the capabilities of the associated [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md).</span></span>

<span data-ttu-id="bab9e-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bab9e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab9e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bab9e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="bab9e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="bab9e-107">Members</span></span>

<span data-ttu-id="bab9e-108">A classe **Msvm \_ VirtualEthernetSwitchManagementCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bab9e-108">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="bab9e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bab9e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bab9e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bab9e-110">Properties</span></span>

<span data-ttu-id="bab9e-111">A classe **Msvm \_ VirtualEthernetSwitchManagementCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bab9e-111">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bab9e-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="bab9e-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-113">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bab9e-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="bab9e-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-116">Uma matriz de identificadores de método, cada um identificando um método da classe [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) que tem suporte de forma assíncrona pela implementação.</span><span class="sxs-lookup"><span data-stu-id="bab9e-116">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported asynchronously by the implementation.</span></span> <span data-ttu-id="bab9e-117">Essa propriedade é herdada do **CIM \_ VirtualSystemManagementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="bab9e-117">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

<span data-ttu-id="bab9e-118">**DefineSystem** (2)</span><span class="sxs-lookup"><span data-stu-id="bab9e-118">**DefineSystem** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

<span data-ttu-id="bab9e-119">**DestroySystem** (3)</span><span class="sxs-lookup"><span data-stu-id="bab9e-119">**DestroySystem** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

<span data-ttu-id="bab9e-120">**DestroySystemConfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="bab9e-120">**DestroySystemConfiguration** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

<span data-ttu-id="bab9e-121">**ModifyResourceSettings** (5)</span><span class="sxs-lookup"><span data-stu-id="bab9e-121">**ModifyResourceSettings** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

<span data-ttu-id="bab9e-122">**ModifySystemSettings** (6)</span><span class="sxs-lookup"><span data-stu-id="bab9e-122">**ModifySystemSettings** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

<span data-ttu-id="bab9e-123">**RemoveResources** (7)</span><span class="sxs-lookup"><span data-stu-id="bab9e-123">**RemoveResources** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

<span data-ttu-id="bab9e-124">**SelectSystemConfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="bab9e-124">**SelectSystemConfiguration** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

<span data-ttu-id="bab9e-125">**SnapshotSystem** (9)</span><span class="sxs-lookup"><span data-stu-id="bab9e-125">**SnapshotSystem** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

<span data-ttu-id="bab9e-126">**Resources** (10)</span><span class="sxs-lookup"><span data-stu-id="bab9e-126">**AddResources** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="bab9e-127">**AddFeatureSettingsSupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="bab9e-127">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="bab9e-128">**ModifyFeatureSettingsSupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="bab9e-128">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="bab9e-129">**RemoveFeatureSettingsSupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="bab9e-129">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="bab9e-130">**AddFeatureSettingsSupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="bab9e-130">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="bab9e-131">**ModifyFeatureSettingsSupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="bab9e-131">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="bab9e-132">**RemoveFeatureSettingsSupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="bab9e-132">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bab9e-133">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="bab9e-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bab9e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-136">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="bab9e-136">A short description of the object.</span></span> <span data-ttu-id="bab9e-137">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos do serviço de gerenciamento do comutador Ethernet virtual do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="bab9e-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-138">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bab9e-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bab9e-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-141">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="bab9e-141">A description of the object.</span></span> <span data-ttu-id="bab9e-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "define os recursos do serviço de gerenciamento do comutador Ethernet virtual".</span><span class="sxs-lookup"><span data-stu-id="bab9e-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bab9e-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bab9e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-146">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="bab9e-146">A display name for the object.</span></span> <span data-ttu-id="bab9e-147">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos do serviço de gerenciamento do comutador Ethernet virtual do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="bab9e-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-148">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="bab9e-148">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-149">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="bab9e-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-151">Indica se a propriedade **ElementName** pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="bab9e-151">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="bab9e-152">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="bab9e-152">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-153">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="bab9e-153">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bab9e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-156">Especifica as restrições em **ElementName**, expressas como uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="bab9e-156">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="bab9e-157">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="bab9e-157">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-158">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="bab9e-158">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-159">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bab9e-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-161">Uma matriz de identificadores de indicação, cada um identificando uma indicação com suporte na implementação.</span><span class="sxs-lookup"><span data-stu-id="bab9e-161">An array of indication identifiers, each identifying an indication that is supported by the implementation.</span></span> <span data-ttu-id="bab9e-162">Essa propriedade é herdada do **CIM \_ VirtualSystemManagementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="bab9e-162">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>



| <span data-ttu-id="bab9e-163">Valor</span><span class="sxs-lookup"><span data-stu-id="bab9e-163">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="bab9e-164">Significado</span><span class="sxs-lookup"><span data-stu-id="bab9e-164">Meaning</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="bab9e-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bab9e-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="bab9e-166">Indica se a implementação dá suporte a notificações em alterações de estado de instâncias de [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que representam recursos de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="bab9e-166">Indicates whether the implementation supports notification on state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances that represent resources of virtual systems.</span></span><br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="bab9e-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bab9e-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="bab9e-168">Indica se a implementação dá suporte a notificações em alterações de estado de instâncias de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bab9e-168">Indicates whether the implementation supports notification on state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span><br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="bab9e-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bab9e-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="bab9e-170">Indica se a implementação dá suporte a notificações em alterações de estado de instâncias de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representam sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="bab9e-170">Indicates whether the implementation supports notification on state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances that represent virtual systems.</span></span><br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="bab9e-171"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="bab9e-171"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="bab9e-172">O <dt> **fornecedor reservou**</dt> <dt>32767.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="bab9e-172"><dt>**Vendor Reserved** </dt> <dt>32767..65535 </dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="bab9e-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bab9e-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bab9e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-176">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="bab9e-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-177">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="bab9e-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bab9e-178">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bab9e-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-179">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="bab9e-179">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-180">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="bab9e-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-182">Um valor booliano que indica se o IOV (virtualização de e/s) é suportado pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="bab9e-182">A boolean value that indicates whether I/O virtualization (IOV) is supported by the platform.</span></span> <span data-ttu-id="bab9e-183">Se o valor for **true**, o IOV terá suporte da plataforma e **IOVSupportReasons** estará vazio.</span><span class="sxs-lookup"><span data-stu-id="bab9e-183">If the value is **True**, then IOV is supported by the platform and **IOVSupportReasons** will be empty.</span></span> <span data-ttu-id="bab9e-184">Caso contrário, a propriedade **IOVSupportReasons** terá os motivos pelos quais a IOV não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="bab9e-184">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-185">**IOVSupportReasons**</span><span class="sxs-lookup"><span data-stu-id="bab9e-185">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-186">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bab9e-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-188">Uma matriz de cadeias de caracteres que indica as possíveis razões pelas quais a IOV não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="bab9e-188">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="bab9e-189">Se o valor de **IOVSupport** for **true**, essa matriz estará vazia.</span><span class="sxs-lookup"><span data-stu-id="bab9e-189">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-190">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="bab9e-190">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-191">Tipo de dados: **unit16**</span><span class="sxs-lookup"><span data-stu-id="bab9e-191">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-193">Qualificadores: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="bab9e-193">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-194">Especifica o comprimento máximo com suporte da propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="bab9e-194">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="bab9e-195">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="bab9e-195">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-196">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="bab9e-196">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-197">Tipo de dados: matriz **unit16**</span><span class="sxs-lookup"><span data-stu-id="bab9e-197">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-199">Indica os possíveis Estados que podem ser solicitados ao usar o método **RequestStateChange** no elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="bab9e-199">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="bab9e-200">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities** e é sempre **nula**.</span><span class="sxs-lookup"><span data-stu-id="bab9e-200">This property is inherited from **CIM\_EnabledLogicalElementCapabilities** and is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bab9e-201">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="bab9e-201">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-202">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bab9e-202">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-204">Uma matriz de identificadores de método, cada um identificando um método da classe [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) que tem suporte de forma síncrona pela implementação.</span><span class="sxs-lookup"><span data-stu-id="bab9e-204">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported synchronously by the implementation.</span></span> <span data-ttu-id="bab9e-205">Essa propriedade é herdada do **CIM \_ VirtualSystemManagementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="bab9e-205">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="bab9e-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span><span class="sxs-lookup"><span data-stu-id="bab9e-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span><span class="sxs-lookup"><span data-stu-id="bab9e-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="bab9e-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span><span class="sxs-lookup"><span data-stu-id="bab9e-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span><span class="sxs-lookup"><span data-stu-id="bab9e-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span><span class="sxs-lookup"><span data-stu-id="bab9e-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="bab9e-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span><span class="sxs-lookup"><span data-stu-id="bab9e-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**Resources** (10)</span><span class="sxs-lookup"><span data-stu-id="bab9e-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span><span class="sxs-lookup"><span data-stu-id="bab9e-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span><span class="sxs-lookup"><span data-stu-id="bab9e-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781)</span><span class="sxs-lookup"><span data-stu-id="bab9e-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bab9e-218">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="bab9e-218">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bab9e-219">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bab9e-219">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bab9e-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bab9e-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bab9e-221">Uma matriz de cadeias de caracteres, cada uma designando um tipo de sistema virtual compatível com a implementação.</span><span class="sxs-lookup"><span data-stu-id="bab9e-221">An array of strings, each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="bab9e-222">O valor de cada elemento de matriz não **NULL** deve estar de acordo com o formato definido para a propriedade **VirtualSystemType** da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="bab9e-222">The value of each non-**Null** array element must conform to the format defined for the **VirtualSystemType** property of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span> <span data-ttu-id="bab9e-223">Essa propriedade é herdada do **CIM \_ VirtualSystemManagementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="bab9e-223">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bab9e-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bab9e-224">Requirements</span></span>



| <span data-ttu-id="bab9e-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab9e-225">Requirement</span></span> | <span data-ttu-id="bab9e-226">Valor</span><span class="sxs-lookup"><span data-stu-id="bab9e-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab9e-227">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bab9e-227">Minimum supported client</span></span><br/> | <span data-ttu-id="bab9e-228">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bab9e-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bab9e-229">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bab9e-229">Minimum supported server</span></span><br/> | <span data-ttu-id="bab9e-230">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bab9e-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bab9e-231">Namespace</span><span class="sxs-lookup"><span data-stu-id="bab9e-231">Namespace</span></span><br/>                | <span data-ttu-id="bab9e-232">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bab9e-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bab9e-233">MOF</span><span class="sxs-lookup"><span data-stu-id="bab9e-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bab9e-234"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bab9e-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bab9e-235">DLL</span><span class="sxs-lookup"><span data-stu-id="bab9e-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bab9e-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bab9e-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

