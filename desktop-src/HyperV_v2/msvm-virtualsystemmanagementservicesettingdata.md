---
description: Representa as configurações do serviço de virtualização presente em um único sistema de host.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Classe Msvm_VirtualSystemManagementServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759232"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a><span data-ttu-id="29bb0-103">\_Classe Msvm VirtualSystemManagementServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="29bb0-103">Msvm\_VirtualSystemManagementServiceSettingData class</span></span>

<span data-ttu-id="29bb0-104">Representa as configurações do serviço de virtualização presente em um único sistema de host.</span><span class="sxs-lookup"><span data-stu-id="29bb0-104">Represents the settings for the virtualization service present on a single host system.</span></span> <span data-ttu-id="29bb0-105">As propriedades desta classe não podem ser modificadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="29bb0-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="29bb0-106">O cliente deve chamar o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar qualquer uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="29bb0-106">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify any of these properties.</span></span>

<span data-ttu-id="29bb0-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="29bb0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="29bb0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29bb0-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a><span data-ttu-id="29bb0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="29bb0-109">Members</span></span>

<span data-ttu-id="29bb0-110">A classe **Msvm \_ VirtualSystemManagementServiceSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="29bb0-110">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="29bb0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="29bb0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29bb0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="29bb0-112">Properties</span></span>

<span data-ttu-id="29bb0-113">A classe **Msvm \_ VirtualSystemManagementServiceSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="29bb0-113">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29bb0-114">**BiosLockString**</span><span class="sxs-lookup"><span data-stu-id="29bb0-114">**BiosLockString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span><span class="sxs-lookup"><span data-stu-id="29bb0-117">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-118">Usado por OEMs para permitir que sistemas operacionais Windows bloqueados por BIOS sejam executados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="29bb0-118">Used by OEMs to allow BIOS-locked Windows operating systems to run in the virtual machine.</span></span> <span data-ttu-id="29bb0-119">Essa cadeia de caracteres deve ter exatamente 32 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="29bb0-119">This string must be exactly 32 characters in length.</span></span>

<span data-ttu-id="29bb0-120">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-120">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="29bb0-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-124">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="29bb0-124">A short description of the object.</span></span> <span data-ttu-id="29bb0-125">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de sistema virtual do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="29bb0-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-126">**CurrentWWNNAddress**</span><span class="sxs-lookup"><span data-stu-id="29bb0-126">**CurrentWWNNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-129">O endereço WWNN (World Wide node Name) para endereços de World Wide Name gerados dinamicamente usados para adaptadores de barramento de host sintético.</span><span class="sxs-lookup"><span data-stu-id="29bb0-129">The world wide node name (WWNN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="29bb0-130">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-130">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-131">**DefaultExternalDataRoot**</span><span class="sxs-lookup"><span data-stu-id="29bb0-131">**DefaultExternalDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-134">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span><span class="sxs-lookup"><span data-stu-id="29bb0-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-135">A raiz de dados externa padrão.</span><span class="sxs-lookup"><span data-stu-id="29bb0-135">The default external data root.</span></span> <span data-ttu-id="29bb0-136">Por padrão, "*raiz* \\ ProgramData \\ \\ virtualização do Microsoft Windows \\ ".</span><span class="sxs-lookup"><span data-stu-id="29bb0-136">By default, "*root*\\ProgramData\\Microsoft\\Windows\\Virtualization".</span></span>

<span data-ttu-id="29bb0-137">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-137">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-138">**DefaultVirtualHardDiskCachingMode**</span><span class="sxs-lookup"><span data-stu-id="29bb0-138">**DefaultVirtualHardDiskCachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="29bb0-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-141">Indica se o cache de arquivos na memória deve ser usado para discos por padrão.</span><span class="sxs-lookup"><span data-stu-id="29bb0-141">Indicates whether in-memory file caching should be used for disks by default.</span></span> <span data-ttu-id="29bb0-142">Esse valor pode ser substituído em uma base por disco no campo **cachingmode** da classe [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-142">This value can be overridden on a per-disk basis in the **CachingMode** field of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="29bb0-143">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="29bb0-143">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="29bb0-144">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="29bb0-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="29bb0-145">**Sem cache** (3)</span><span class="sxs-lookup"><span data-stu-id="29bb0-145">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="29bb0-146">**Pais compartilháveis do cache** (4)</span><span class="sxs-lookup"><span data-stu-id="29bb0-146">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="29bb0-147">**DefaultVirtualHardDiskPath**</span><span class="sxs-lookup"><span data-stu-id="29bb0-147">**DefaultVirtualHardDiskPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-150">O caminho do disco rígido virtual padrão.</span><span class="sxs-lookup"><span data-stu-id="29bb0-150">The default virtual hard disk path.</span></span> <span data-ttu-id="29bb0-151">Por padrão, " \\ usuários raiz \\ \\ documentos públicos \\ discos rígidos virtuais".</span><span class="sxs-lookup"><span data-stu-id="29bb0-151">By default, "*root*\\Users\\Public\\Documents\\Virtual Hard Disks".</span></span>

<span data-ttu-id="29bb0-152">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-152">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-153">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="29bb0-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-156">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="29bb0-156">A description of the object.</span></span> <span data-ttu-id="29bb0-157">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações para o serviço de gerenciamento de sistema virtual".</span><span class="sxs-lookup"><span data-stu-id="29bb0-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-158">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="29bb0-158">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-161">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="29bb0-161">A display name for the object.</span></span> <span data-ttu-id="29bb0-162">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de sistema virtual do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="29bb0-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span> <span data-ttu-id="29bb0-163">A alteração dessa propriedade alterará a propriedade **ElementName** do derivativo [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associado.</span><span class="sxs-lookup"><span data-stu-id="29bb0-163">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-164">**EnhancedSessionModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="29bb0-164">**EnhancedSessionModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-165">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29bb0-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-167">Indica se o modo de sessão avançada é permitido no servidor.</span><span class="sxs-lookup"><span data-stu-id="29bb0-167">Indicates whether enhanced session mode is permitted on the server.</span></span> <span data-ttu-id="29bb0-168">**True** indica permitido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="29bb0-168">**True** indicates permitted, otherwise **False**.</span></span>

<span data-ttu-id="29bb0-169">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="29bb0-169">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-170">**HbaLunTimeout**</span><span class="sxs-lookup"><span data-stu-id="29bb0-170">**HbaLunTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29bb0-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-173">Especifica a quantidade de tempo que o dispositivo virtual Fibre Channel sintético aguardará que um LUN (número de unidade lógica) apareça antes de iniciar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="29bb0-173">Specifies the amount of time that the synthetic Fibre Channel virtual device will wait for a logical unit number (LUN) to appear before starting a virtual machine.</span></span>

<span data-ttu-id="29bb0-174">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-174">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-175">**HypervisorRootSchedulerEnabled**</span><span class="sxs-lookup"><span data-stu-id="29bb0-175">**HypervisorRootSchedulerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-176">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29bb0-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-178">Se o Agendador raiz do hipervisor está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="29bb0-178">Whether or not the hypervisor root scheduler is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="29bb0-179">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="29bb0-179">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="29bb0-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="29bb0-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-183">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="29bb0-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-184">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="29bb0-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="29bb0-185">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como "Microsoft:*host*", em que *host* é o nome NetBIOS do sistema de computador host.</span><span class="sxs-lookup"><span data-stu-id="29bb0-185">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*host*", where *host* is the NetBIOS name of the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-186">**MaximumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="29bb0-186">**MaximumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-189">O endereço MAC máximo para endereços MAC gerados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="29bb0-189">The maximum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="29bb0-190">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-190">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-191">**MaximumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="29bb0-191">**MaximumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-194">O endereço de WWPN (World Wide Port Name) máximo para endereços de World Wide Name gerados dinamicamente usados para adaptadores de barramento de host sintético.</span><span class="sxs-lookup"><span data-stu-id="29bb0-194">The maximum world wide port name (WWPN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="29bb0-195">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-195">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-196">**MinimumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="29bb0-196">**MinimumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-199">O endereço MAC mínimo para endereços MAC gerados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="29bb0-199">The minimum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="29bb0-200">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-200">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-201">**MinimumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="29bb0-201">**MinimumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-204">O endereço de World Wide Name de porta mínimo para endereços de World Wide Name gerados dinamicamente usados para adaptadores de barramento de host sintético.</span><span class="sxs-lookup"><span data-stu-id="29bb0-204">The minimum world wide port name address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="29bb0-205">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-205">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-206">**NumaSpanningEnabled**</span><span class="sxs-lookup"><span data-stu-id="29bb0-206">**NumaSpanningEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-207">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="29bb0-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-209">Especifica se a memória pode ser alocada de nós NUMA (acesso remoto não uniforme à memória) ao iniciar uma máquina virtual ou ao atribuir memória a uma máquina virtual por memória dinâmica.</span><span class="sxs-lookup"><span data-stu-id="29bb0-209">Specifies whether memory can be allocated from remote nonuniform memory access (NUMA) nodes when starting a virtual machine or when assigning memory to a virtual machine by dynamic memory.</span></span> <span data-ttu-id="29bb0-210">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="29bb0-210">This can be one of the following values.</span></span>



| <span data-ttu-id="29bb0-211">Valor</span><span class="sxs-lookup"><span data-stu-id="29bb0-211">Value</span></span>                                                                                | <span data-ttu-id="29bb0-212">Significado</span><span class="sxs-lookup"><span data-stu-id="29bb0-212">Meaning</span></span>                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29bb0-213"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="29bb0-213"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="29bb0-214">A memória pode ser alocada de nós NUMA locais e remotos.</span><span class="sxs-lookup"><span data-stu-id="29bb0-214">Memory can be allocated from both local and remote NUMA nodes.</span></span><br/>                   |
| <dl> <span data-ttu-id="29bb0-215"><dt>**For**</dt></span><span class="sxs-lookup"><span data-stu-id="29bb0-215"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="29bb0-216">A memória pode ser alocada somente a partir do nó NUMA atribuído à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="29bb0-216">Memory can be allocated only from the NUMA node assigned to the virtual machine.</span></span><br/> |



 

<span data-ttu-id="29bb0-217">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-217">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-218">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="29bb0-218">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-221">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações gerais do DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="29bb0-221">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-222">Descreve como o proprietário do sistema primário pode ser alcançado (por exemplo, número de telefone ou endereço de email).</span><span class="sxs-lookup"><span data-stu-id="29bb0-222">Describes how the primary system owner can be reached (for example, phone number or email address).</span></span> <span data-ttu-id="29bb0-223">Por padrão, vazio.</span><span class="sxs-lookup"><span data-stu-id="29bb0-223">By default, empty.</span></span> <span data-ttu-id="29bb0-224">Esse nome não pode exceder 256 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="29bb0-224">This name may not exceed 256 characters in length.</span></span>

<span data-ttu-id="29bb0-225">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-225">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29bb0-226">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="29bb0-226">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29bb0-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="29bb0-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29bb0-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29bb0-229">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações gerais do DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="29bb0-229">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="29bb0-230">O nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="29bb0-230">The name of the primary system owner.</span></span> <span data-ttu-id="29bb0-231">Por padrão, "administradores".</span><span class="sxs-lookup"><span data-stu-id="29bb0-231">By default, "Administrators".</span></span> <span data-ttu-id="29bb0-232">Esse valor não pode exceder 64 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="29bb0-232">This value may not exceed 64 characters in length.</span></span>

<span data-ttu-id="29bb0-233">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="29bb0-233">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29bb0-234">Comentários</span><span class="sxs-lookup"><span data-stu-id="29bb0-234">Remarks</span></span>

<span data-ttu-id="29bb0-235">O acesso à classe **Msvm \_ VirtualSystemManagementServiceSettingData** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="29bb0-235">Access to the **Msvm\_VirtualSystemManagementServiceSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="29bb0-236">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="29bb0-236">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="29bb0-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29bb0-237">Requirements</span></span>



| <span data-ttu-id="29bb0-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="29bb0-238">Requirement</span></span> | <span data-ttu-id="29bb0-239">Valor</span><span class="sxs-lookup"><span data-stu-id="29bb0-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29bb0-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29bb0-240">Minimum supported client</span></span><br/> | <span data-ttu-id="29bb0-241">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="29bb0-241">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="29bb0-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29bb0-242">Minimum supported server</span></span><br/> | <span data-ttu-id="29bb0-243">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="29bb0-243">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="29bb0-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="29bb0-244">Namespace</span></span><br/>                | <span data-ttu-id="29bb0-245">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="29bb0-245">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="29bb0-246">MOF</span><span class="sxs-lookup"><span data-stu-id="29bb0-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29bb0-247"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29bb0-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29bb0-248">DLL</span><span class="sxs-lookup"><span data-stu-id="29bb0-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29bb0-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29bb0-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29bb0-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="29bb0-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29bb0-251">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="29bb0-251">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="29bb0-252">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="29bb0-252">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="29bb0-253">[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29bb0-253">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="29bb0-254">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="29bb0-254">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

