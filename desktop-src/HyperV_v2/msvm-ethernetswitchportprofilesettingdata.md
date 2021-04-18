---
description: Representa as configurações de perfil de porta.
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Classe Msvm_EthernetSwitchPortProfileSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768753"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a><span data-ttu-id="8adc4-103">\_Classe Msvm EthernetSwitchPortProfileSettingData</span><span class="sxs-lookup"><span data-stu-id="8adc4-103">Msvm\_EthernetSwitchPortProfileSettingData class</span></span>

<span data-ttu-id="8adc4-104">Representa as configurações de perfil de porta.</span><span class="sxs-lookup"><span data-stu-id="8adc4-104">Represents the port profile settings.</span></span>

<span data-ttu-id="8adc4-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8adc4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8adc4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8adc4-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a><span data-ttu-id="8adc4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8adc4-107">Members</span></span>

<span data-ttu-id="8adc4-108">A classe **Msvm \_ EthernetSwitchPortProfileSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8adc4-108">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8adc4-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8adc4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8adc4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8adc4-110">Properties</span></span>

<span data-ttu-id="8adc4-111">A classe **Msvm \_ EthernetSwitchPortProfileSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8adc4-111">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8adc4-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8adc4-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8adc4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8adc4-115">A short description of the object.</span></span> <span data-ttu-id="8adc4-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de perfil de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="8adc4-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-117">**CdnLabelId**</span><span class="sxs-lookup"><span data-stu-id="8adc4-117">**CdnLabelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8adc4-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-120">Qualificadores: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-120">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-121">O identificador de rótulo da CDN.</span><span class="sxs-lookup"><span data-stu-id="8adc4-121">The CDN label identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-122">**CdnLabelString**</span><span class="sxs-lookup"><span data-stu-id="8adc4-122">**CdnLabelString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-125">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-126">A cadeia de caracteres do rótulo CDN.</span><span class="sxs-lookup"><span data-stu-id="8adc4-126">The CDN label string.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8adc4-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8adc4-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-130">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="8adc4-130">A description of the object.</span></span> <span data-ttu-id="8adc4-131">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa as configurações de perfil de porta".</span><span class="sxs-lookup"><span data-stu-id="8adc4-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port profile settings.".</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8adc4-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8adc4-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-135">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="8adc4-135">A display name for the object.</span></span> <span data-ttu-id="8adc4-136">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de perfil de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="8adc4-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8adc4-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8adc4-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-140">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="8adc4-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-141">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="8adc4-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8adc4-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8adc4-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-143">**NetCfgInstanceId**</span><span class="sxs-lookup"><span data-stu-id="8adc4-143">**NetCfgInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-146">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-147">Um identificador de dispositivo exclusivo da subinterface.</span><span class="sxs-lookup"><span data-stu-id="8adc4-147">An unique device identifier of the subinterface.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-148">**PciBusNumber**</span><span class="sxs-lookup"><span data-stu-id="8adc4-148">**PciBusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8adc4-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-151">Qualificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-151">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-152">O número do barramento PCI.</span><span class="sxs-lookup"><span data-stu-id="8adc4-152">The PCI bus number.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-153">**PciDeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="8adc4-153">**PciDeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-154">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8adc4-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-156">Qualificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-156">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-157">O número do dispositivo PCI.</span><span class="sxs-lookup"><span data-stu-id="8adc4-157">The PCI device number.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-158">**PciFunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="8adc4-158">**PciFunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8adc4-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-161">Qualificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-161">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-162">O número da função PCI.</span><span class="sxs-lookup"><span data-stu-id="8adc4-162">The PCI function number.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-163">**PciSegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="8adc4-163">**PciSegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-164">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8adc4-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-166">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-166">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-167">O número do segmento de PCI.</span><span class="sxs-lookup"><span data-stu-id="8adc4-167">The PCI segment number.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-168">**ProfileData**</span><span class="sxs-lookup"><span data-stu-id="8adc4-168">**ProfileData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-169">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8adc4-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-171">Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-171">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-172">Dados adicionais para o perfil de porta.</span><span class="sxs-lookup"><span data-stu-id="8adc4-172">Additional data for the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-173">**ProfileId**</span><span class="sxs-lookup"><span data-stu-id="8adc4-173">**ProfileId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-176">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-177">O identificador do perfil de porta.</span><span class="sxs-lookup"><span data-stu-id="8adc4-177">The identifier of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-178">**ProfileName**</span><span class="sxs-lookup"><span data-stu-id="8adc4-178">**ProfileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-180">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-181">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-182">O nome do perfil de porta.</span><span class="sxs-lookup"><span data-stu-id="8adc4-182">The name of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-183">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="8adc4-183">**VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-185">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-186">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-187">O identificador do fornecedor que define o perfil.</span><span class="sxs-lookup"><span data-stu-id="8adc4-187">The identifier of the vendor defining the profile.</span></span>

</dd> <dt>

<span data-ttu-id="8adc4-188">**Nome_do_Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="8adc4-188">**VendorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8adc4-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8adc4-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8adc4-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8adc4-191">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8adc4-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8adc4-192">O nome do fornecedor que define o perfil.</span><span class="sxs-lookup"><span data-stu-id="8adc4-192">The name of the vendor defining the profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8adc4-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8adc4-193">Requirements</span></span>



| <span data-ttu-id="8adc4-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="8adc4-194">Requirement</span></span> | <span data-ttu-id="8adc4-195">Valor</span><span class="sxs-lookup"><span data-stu-id="8adc4-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8adc4-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8adc4-196">Minimum supported client</span></span><br/> | <span data-ttu-id="8adc4-197">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8adc4-197">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8adc4-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8adc4-198">Minimum supported server</span></span><br/> | <span data-ttu-id="8adc4-199">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8adc4-199">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8adc4-200">Namespace</span><span class="sxs-lookup"><span data-stu-id="8adc4-200">Namespace</span></span><br/>                | <span data-ttu-id="8adc4-201">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8adc4-201">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8adc4-202">MOF</span><span class="sxs-lookup"><span data-stu-id="8adc4-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8adc4-203"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8adc4-203"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8adc4-204">DLL</span><span class="sxs-lookup"><span data-stu-id="8adc4-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8adc4-205"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8adc4-205"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

