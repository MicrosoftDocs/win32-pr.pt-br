---
description: Representa os recursos de um \_ objeto CIM VirtualSystemManagementService.
ms.assetid: 484b0378-b354-49c4-b98b-a960a7b07b92
title: Classe CIM_VirtualSystemManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementCapabilities
- CIM_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- CIM_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2772068ed011a2a61cdd4f5c1396e057838b7720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778760"
---
# <a name="cim_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="b34f6-103">\_Classe CIM VirtualSystemManagementCapabilities</span><span class="sxs-lookup"><span data-stu-id="b34f6-103">CIM\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="b34f6-104">Representa os recursos de um objeto [**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b34f6-104">Represents the capabilities of a [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b34f6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string VirtualSystemTypesSupported[];
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="b34f6-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b34f6-106">Members</span></span>

<span data-ttu-id="b34f6-107">A classe **CIM \_ VirtualSystemManagementCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b34f6-107">The **CIM\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="b34f6-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b34f6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b34f6-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b34f6-109">Properties</span></span>

<span data-ttu-id="b34f6-110">A classe **CIM \_ VirtualSystemManagementCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b34f6-110">The **CIM\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b34f6-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="b34f6-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f6-112">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f6-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f6-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b34f6-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f6-114">Uma matriz que contém nomes de método para os métodos de classe [**\_ VirtualSystemManagementService do CIM**](cim-virtualsystemmanagementservice.md) com suporte para operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="b34f6-114">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="b34f6-115">**DefineSystemSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="b34f6-115">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="b34f6-116">**DestroySystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="b34f6-116">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="b34f6-117">**DestroySystemConfigurationSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="b34f6-117">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="b34f6-118">**ModifyResourceSettingsSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="b34f6-118">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="b34f6-119">**ModifySystemSettingsSupported** (6)</span><span class="sxs-lookup"><span data-stu-id="b34f6-119">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="b34f6-120">**RemoveResourcesSupported** (7)</span><span class="sxs-lookup"><span data-stu-id="b34f6-120">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="b34f6-121">**SelectSystemConfigurationSupported** (8)</span><span class="sxs-lookup"><span data-stu-id="b34f6-121">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="b34f6-122">**SnapshotSystemSupported** (9)</span><span class="sxs-lookup"><span data-stu-id="b34f6-122">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="b34f6-123">**AddResourcesSupported** (10)</span><span class="sxs-lookup"><span data-stu-id="b34f6-123">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b34f6-124">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b34f6-124">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b34f6-125">**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b34f6-125">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b34f6-126">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="b34f6-126">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f6-127">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f6-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f6-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b34f6-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f6-129">Uma matriz que contém os tipos de indicações com suporte da implementação.</span><span class="sxs-lookup"><span data-stu-id="b34f6-129">An array that contains the supported indications types of the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="b34f6-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="b34f6-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="b34f6-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="b34f6-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="b34f6-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="b34f6-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b34f6-133">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b34f6-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b34f6-134">**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b34f6-134">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b34f6-135">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="b34f6-135">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f6-136">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b34f6-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f6-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b34f6-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b34f6-138">Uma matriz que contém nomes de método para os métodos de classe [**\_ VirtualSystemManagementService do CIM**](cim-virtualsystemmanagementservice.md) com suporte para operações síncronas.</span><span class="sxs-lookup"><span data-stu-id="b34f6-138">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for synchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="b34f6-139">**DefineSystemSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="b34f6-139">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="b34f6-140">**DestroySystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="b34f6-140">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="b34f6-141">**DestroySystemConfigurationSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="b34f6-141">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="b34f6-142">**ModifyResourceSettingsSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="b34f6-142">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="b34f6-143">**ModifySystemSettingsSupported** (6)</span><span class="sxs-lookup"><span data-stu-id="b34f6-143">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="b34f6-144">**RemoveResourcesSupported** (7)</span><span class="sxs-lookup"><span data-stu-id="b34f6-144">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="b34f6-145">**SelectSystemConfigurationSupported** (8)</span><span class="sxs-lookup"><span data-stu-id="b34f6-145">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="b34f6-146">**SnapshotSystemSupported** (9)</span><span class="sxs-lookup"><span data-stu-id="b34f6-146">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="b34f6-147">**AddResourcesSupported** (10)</span><span class="sxs-lookup"><span data-stu-id="b34f6-147">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b34f6-148">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b34f6-148">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b34f6-149">**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b34f6-149">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b34f6-150">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="b34f6-150">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b34f6-151">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b34f6-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b34f6-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b34f6-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b34f6-153">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span><span class="sxs-lookup"><span data-stu-id="b34f6-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span></span>
</dt> </dl>

<span data-ttu-id="b34f6-154">O tipo de sistemas virtuais com suporte pela implementação.</span><span class="sxs-lookup"><span data-stu-id="b34f6-154">The type of virtual systems supported by the implementation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b34f6-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b34f6-155">Requirements</span></span>



| <span data-ttu-id="b34f6-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="b34f6-156">Requirement</span></span> | <span data-ttu-id="b34f6-157">Valor</span><span class="sxs-lookup"><span data-stu-id="b34f6-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b34f6-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b34f6-158">Minimum supported client</span></span><br/> | <span data-ttu-id="b34f6-159">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b34f6-159">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b34f6-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b34f6-160">Minimum supported server</span></span><br/> | <span data-ttu-id="b34f6-161">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b34f6-161">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b34f6-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="b34f6-162">Namespace</span></span><br/>                | <span data-ttu-id="b34f6-163">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b34f6-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b34f6-164">MOF</span><span class="sxs-lookup"><span data-stu-id="b34f6-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b34f6-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b34f6-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b34f6-166">DLL</span><span class="sxs-lookup"><span data-stu-id="b34f6-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b34f6-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b34f6-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b34f6-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="b34f6-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34f6-169">**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="b34f6-169">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

