---
description: Representa o estado de configuração das configurações de mesclagem de disco para uma máquina virtual.
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Classe Msvm_DiskMergeSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780979"
---
# <a name="msvm_diskmergesettingdata-class"></a><span data-ttu-id="e62a6-103">\_Classe Msvm DiskMergeSettingData</span><span class="sxs-lookup"><span data-stu-id="e62a6-103">Msvm\_DiskMergeSettingData class</span></span>

<span data-ttu-id="e62a6-104">Representa o estado de configuração das configurações de mesclagem de disco para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e62a6-104">Represents the configuration state of the disk merge settings for a virtual machine.</span></span>

<span data-ttu-id="e62a6-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e62a6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e62a6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e62a6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a><span data-ttu-id="e62a6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e62a6-107">Members</span></span>

<span data-ttu-id="e62a6-108">A classe **Msvm \_ DiskMergeSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e62a6-108">The **Msvm\_DiskMergeSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e62a6-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e62a6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e62a6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e62a6-110">Properties</span></span>

<span data-ttu-id="e62a6-111">A classe **Msvm \_ DiskMergeSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e62a6-111">The **Msvm\_DiskMergeSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e62a6-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e62a6-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e62a6-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e62a6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e62a6-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e62a6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e62a6-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e62a6-115">A short description of the object.</span></span> <span data-ttu-id="e62a6-116">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e é sempre definida como "dados de configuração de mesclagem de disco".</span><span class="sxs-lookup"><span data-stu-id="e62a6-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="e62a6-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e62a6-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e62a6-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e62a6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e62a6-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e62a6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e62a6-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="e62a6-120">A description of the object.</span></span> <span data-ttu-id="e62a6-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "dados de configuração de mesclagem de disco da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="e62a6-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="e62a6-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e62a6-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e62a6-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e62a6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e62a6-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e62a6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e62a6-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="e62a6-125">A display name for the object.</span></span> <span data-ttu-id="e62a6-126">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como "dados de configuração de mesclagem de disco".</span><span class="sxs-lookup"><span data-stu-id="e62a6-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Disk Merge Setting Data".</span></span> <span data-ttu-id="e62a6-127">A alteração dessa propriedade alterará a propriedade **ElementName** do derivativo [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associado.</span><span class="sxs-lookup"><span data-stu-id="e62a6-127">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="e62a6-128">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e62a6-128">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e62a6-129">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e62a6-129">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e62a6-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e62a6-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e62a6-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e62a6-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e62a6-132">Especifica o estado habilitado da funcionalidade de mesclagem de disco.</span><span class="sxs-lookup"><span data-stu-id="e62a6-132">Specifies the enabled state of the disk merge functionality.</span></span>

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

<span data-ttu-id="e62a6-133">**Desabilitado temporariamente** (0)</span><span class="sxs-lookup"><span data-stu-id="e62a6-133">**Temporarily disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e62a6-134">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="e62a6-134">**Enabled** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e62a6-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e62a6-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e62a6-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e62a6-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e62a6-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e62a6-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e62a6-138">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e62a6-138">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e62a6-139">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="e62a6-139">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e62a6-140">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) e é sempre definida como "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="e62a6-140">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e62a6-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e62a6-141">Requirements</span></span>



| <span data-ttu-id="e62a6-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="e62a6-142">Requirement</span></span> | <span data-ttu-id="e62a6-143">Valor</span><span class="sxs-lookup"><span data-stu-id="e62a6-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e62a6-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e62a6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e62a6-145">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e62a6-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e62a6-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e62a6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e62a6-147">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e62a6-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e62a6-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="e62a6-148">Namespace</span></span><br/>                | <span data-ttu-id="e62a6-149">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e62a6-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e62a6-150">MOF</span><span class="sxs-lookup"><span data-stu-id="e62a6-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e62a6-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e62a6-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e62a6-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e62a6-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e62a6-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e62a6-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

