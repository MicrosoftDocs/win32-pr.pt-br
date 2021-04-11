---
description: Representa um sistema de computador executando o Windows.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089029"
---
# <a name="win32_computersystem-class"></a><span data-ttu-id="79698-103">Classe de ComputerSystem do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="79698-103">Win32\_ComputerSystem class</span></span>

<span data-ttu-id="79698-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ ComputerSystem do Win32** representa um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="79698-104">The **Win32\_ComputerSystem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a computer system running Windows.</span></span>

<span data-ttu-id="79698-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="79698-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79698-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79698-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a><span data-ttu-id="79698-107">Membros</span><span class="sxs-lookup"><span data-stu-id="79698-107">Members</span></span>

<span data-ttu-id="79698-108">A classe **Win32 \_ ComputerSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="79698-108">The **Win32\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="79698-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="79698-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="79698-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="79698-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="79698-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="79698-111">Methods</span></span>

<span data-ttu-id="79698-112">A classe **Win32 \_ ComputerSystem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="79698-112">The **Win32\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="79698-113">Método</span><span class="sxs-lookup"><span data-stu-id="79698-113">Method</span></span>                                                                                          | <span data-ttu-id="79698-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="79698-114">Description</span></span>                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79698-115">**JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="79698-115">**JoinDomainOrWorkgroup**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | <span data-ttu-id="79698-116">Adiciona um sistema de computador a um domínio ou grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="79698-116">Adds a computer system to a domain or workgroup.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="79698-117">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="79698-117">**Rename**</span></span>](rename-method-in-class-win32-computersystem.md)                                   | <span data-ttu-id="79698-118">Renomeia um computador local.</span><span class="sxs-lookup"><span data-stu-id="79698-118">Renames a local computer.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="79698-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="79698-119">**SetPowerState**</span></span>                                                                               | <span data-ttu-id="79698-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="79698-120">Not implemented.</span></span> <span data-ttu-id="79698-121">Para obter mais informações sobre como implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="79698-121">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span><br/> |
| [<span data-ttu-id="79698-122">**UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="79698-122">**UnjoinDomainOrWorkgroup**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | <span data-ttu-id="79698-123">Remove um sistema de computador de um domínio ou grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="79698-123">Removes a computer system from a domain or workgroup.</span></span><br/>                                                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="79698-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="79698-124">Properties</span></span>

<span data-ttu-id="79698-125">A classe **Win32 \_ ComputerSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="79698-125">The **Win32\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79698-126">**AdminPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="79698-126">**AdminPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| configurações de segurança de hardware \| AdminPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="79698-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|AdminPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="79698-130">Configurações de segurança de hardware do sistema para status da senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="79698-130">System hardware security settings for administrator password status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79698-131">**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-131">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79698-132">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-132">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="79698-133">**Não implementado** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-133">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-134">**Desconhecido** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-134">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-135">**AutomaticManagedPagefile**</span><span class="sxs-lookup"><span data-stu-id="79698-135">**AutomaticManagedPagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-136">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79698-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="79698-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="79698-139">Se **for true**, o sistema gerenciará o arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="79698-139">If **True**, the system manages the page file.</span></span>

</dd> <dt>

<span data-ttu-id="79698-140">**AutomaticResetBootOption**</span><span class="sxs-lookup"><span data-stu-id="79698-140">**AutomaticResetBootOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-141">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79698-143">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| reboot")</span><span class="sxs-lookup"><span data-stu-id="79698-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="79698-144">Se for **true**, a opção de redefinição automática será habilitada.</span><span class="sxs-lookup"><span data-stu-id="79698-144">If **True**, the automatic reset boot option is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="79698-145">**AutomaticResetCapability**</span><span class="sxs-lookup"><span data-stu-id="79698-145">**AutomaticResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="79698-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="79698-149">Se for **true**, a redefinição automática será habilitada.</span><span class="sxs-lookup"><span data-stu-id="79698-149">If **True**, the automatic reset is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="79698-150">**BootOptionOnLimit**</span><span class="sxs-lookup"><span data-stu-id="79698-150">**BootOptionOnLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-153">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| opção SMBIOS tipo 23 \| recursos \| de inicialização no limite")</span><span class="sxs-lookup"><span data-stu-id="79698-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilites\|Boot Option on Limit")</span></span>
</dt> </dl>

<span data-ttu-id="79698-154">O limite da opção de inicialização está ativado.</span><span class="sxs-lookup"><span data-stu-id="79698-154">Boot option limit is ON.</span></span> <span data-ttu-id="79698-155">Identifica a ação do sistema quando o valor de **ResetLimit** é atingido.</span><span class="sxs-lookup"><span data-stu-id="79698-155">Identifies the system action when the **ResetLimit** value is reached.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="79698-156">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-156">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="79698-157">**Sistema operacional** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-157">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="79698-158">**Utilitários do sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-158">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="79698-159">**Não reinicializar** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-159">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-160">**BootOptionOnWatchDog**</span><span class="sxs-lookup"><span data-stu-id="79698-160">**BootOptionOnWatchDog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-163">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("opção de inicialização de recursos do SMBIOS \| tipo 23 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilities\|Boot Option")</span></span>
</dt> </dl>

<span data-ttu-id="79698-164">O tipo de ação de reinicialização após a hora no temporizador do Watchdog é decorrido.</span><span class="sxs-lookup"><span data-stu-id="79698-164">Type of reboot action after the time on the watchdog timer is elapsed.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="79698-165">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-165">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="79698-166">**Sistema operacional** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-166">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="79698-167">**Utilitários do sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-167">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="79698-168">**Não reinicializar** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-168">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-169">**BootROMSupported**</span><span class="sxs-lookup"><span data-stu-id="79698-169">**BootROMSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-170">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-172">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="79698-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="79698-173">Se for **true**, indicará se há suporte para uma ROM de inicialização.</span><span class="sxs-lookup"><span data-stu-id="79698-173">If **True**, indicates whether a boot ROM is supported.</span></span>

</dd> <dt>

<span data-ttu-id="79698-174">**BootStatus**</span><span class="sxs-lookup"><span data-stu-id="79698-174">**BootStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-175">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79698-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-177">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 32 \| status de inicialização das informações de inicialização do sistema \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-177">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 32\|System Boot Information\|Boot Status")</span></span>
</dt> </dl>

<span data-ttu-id="79698-178">Status e campos de dados adicionais que identificam o status de inicialização.</span><span class="sxs-lookup"><span data-stu-id="79698-178">Status and Additional Data fields that identify the boot status.</span></span>

<span data-ttu-id="79698-179">Esse valor é proveniente do membro **status de inicialização** da estrutura de informações de inicialização do **sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="79698-179">This value comes from the **Boot Status** member of the **System Boot Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="79698-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="79698-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="79698-181">**Inicializaçãostate**</span><span class="sxs-lookup"><span data-stu-id="79698-181">**BootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-184">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT")</span><span class="sxs-lookup"><span data-stu-id="79698-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)\|SM\_CLEANBOOT")</span></span>
</dt> </dl>

<span data-ttu-id="79698-185">O sistema foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="79698-185">System is started.</span></span> <span data-ttu-id="79698-186">A inicialização segura de falhas ignora os arquivos de inicialização do usuário também chamados de inicialização segura.</span><span class="sxs-lookup"><span data-stu-id="79698-186">Fail-safe boot bypasses the user startup files also called SafeBoot.</span></span>

<span data-ttu-id="79698-187">A lista a seguir contém os valores necessários:</span><span class="sxs-lookup"><span data-stu-id="79698-187">The following list contains the required values:</span></span>

<dl> <dd><span data-ttu-id="79698-188">"Inicialização normal"</span><span class="sxs-lookup"><span data-stu-id="79698-188">"Normal boot"</span></span></dd> <dd><span data-ttu-id="79698-189">"Inicialização segura de falhas"</span><span class="sxs-lookup"><span data-stu-id="79698-189">"Fail-safe boot"</span></span></dd> <dd><span data-ttu-id="79698-190">"Prova de falhas com inicialização de rede"</span><span class="sxs-lookup"><span data-stu-id="79698-190">"Fail-safe with network boot"</span></span></dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

<span data-ttu-id="79698-191">**Inicialização normal** ("inicialização normal")</span><span class="sxs-lookup"><span data-stu-id="79698-191">**Normal boot** ("Normal boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

<span data-ttu-id="79698-192">**Inicialização segura** ("inicialização com falha segura")</span><span class="sxs-lookup"><span data-stu-id="79698-192">**Fail-safe boot** ("Fail-safe boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

<span data-ttu-id="79698-193">**À prova de falhas com inicialização de rede** ("segurança-segura com inicialização de rede")</span><span class="sxs-lookup"><span data-stu-id="79698-193">**Fail-safe with network boot** ("Fail-safe with network boot")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-194">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="79698-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-197">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="79698-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="79698-198">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="79698-198">Short description of the object a one-line string.</span></span>

<span data-ttu-id="79698-199">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79698-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-200">**ChassisBootupState**</span><span class="sxs-lookup"><span data-stu-id="79698-200">**ChassisBootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-201">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-203">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("estado de inicialização do SMBIOS \| tipo 3 \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Bootup State")</span></span>
</dt> </dl>

<span data-ttu-id="79698-204">Inicialize o estado do chassi.</span><span class="sxs-lookup"><span data-stu-id="79698-204">Boot up state of the chassis.</span></span>

<span data-ttu-id="79698-205">Esse valor é proveniente do membro de **estado de inicialização** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="79698-205">This value comes from the **Boot-up State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79698-206">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-206">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-207">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-207">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="79698-208">**Seguro** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-208">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="79698-209">**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-209">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="79698-210">**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-210">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="79698-211">**Não recuperável** (6)</span><span class="sxs-lookup"><span data-stu-id="79698-211">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-212">**ChassisSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="79698-212">**ChassisSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-215">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| número de SKU do chassi do tipo SMBIOS 3 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Chassis\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="79698-216">O número de SKU do gabinete ou compartimento como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="79698-216">The chassis or enclosure SKU number as a string.</span></span>

<span data-ttu-id="79698-217">Esse valor é proveniente do membro **número da SKU** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="79698-217">This value comes from the **SKU Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="79698-218">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="79698-218">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="79698-219">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79698-219">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-222">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79698-222">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79698-223">Nome da primeira classe concreta na cadeia de herança de uma instância.</span><span class="sxs-lookup"><span data-stu-id="79698-223">Name of the first concrete class in the inheritance chain of an instance.</span></span> <span data-ttu-id="79698-224">Você pode usar essa propriedade com outras propriedades da classe para identificar todas as instâncias da classe e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="79698-224">You can use this property with other properties of the class to identify all instances of the class and its subclasses.</span></span>

<span data-ttu-id="79698-225">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="79698-225">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-226">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="79698-226">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-227">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="79698-227">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-228">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79698-229">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de tempo win32api diferença de \| [**\_ \_ informações de fuso horário**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="79698-229">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="79698-230">Quantidade de tempo que o sistema de computador unitário é deslocado do UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="79698-230">Amount of time the unitary computer system is offset from Coordinated Universal Time (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="79698-231">**DaylightInEffect**</span><span class="sxs-lookup"><span data-stu-id="79698-231">**DaylightInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-232">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-234">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span><span class="sxs-lookup"><span data-stu-id="79698-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Functions\|[**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span></span>
</dt> </dl>

<span data-ttu-id="79698-235">Se for **true**, o modo de economia de verão será on.</span><span class="sxs-lookup"><span data-stu-id="79698-235">If **True**, the daylight savings mode is ON.</span></span>

</dd> <dt>

<span data-ttu-id="79698-236">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="79698-236">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-239">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="79698-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="79698-240">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="79698-240">Description of the object.</span></span>

<span data-ttu-id="79698-241">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79698-241">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-242">**DNSHostName**</span><span class="sxs-lookup"><span data-stu-id="79698-242">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-245">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| GetComputerNameEx devia \| ComputerNameDnsHostname")</span><span class="sxs-lookup"><span data-stu-id="79698-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetComputerNameEx\|ComputerNameDnsHostname")</span></span>
</dt> </dl>

<span data-ttu-id="79698-246">Nome do computador local de acordo com o DNS (servidor de nomes de domínio).</span><span class="sxs-lookup"><span data-stu-id="79698-246">Name of local computer according to the domain name server (DNS).</span></span>

</dd> <dt>

<span data-ttu-id="79698-247">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="79698-247">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-250">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de gerenciamento de rede Win32API \| [**WKSTA \_ info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ langroup")</span><span class="sxs-lookup"><span data-stu-id="79698-250">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**WKSTA\_INFO\_100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100)\|wki100\_langroup")</span></span>
</dt> </dl>

<span data-ttu-id="79698-251">Nome do domínio ao qual um computador pertence.</span><span class="sxs-lookup"><span data-stu-id="79698-251">Name of the domain to which a computer belongs.</span></span>

> [!Note]  
> <span data-ttu-id="79698-252">Se o computador não fizer parte de um domínio, o nome do grupo de trabalho será retornado.</span><span class="sxs-lookup"><span data-stu-id="79698-252">If the computer is not part of a domain, then the name of the workgroup is returned.</span></span>

 

</dd> <dt>

<span data-ttu-id="79698-253">**DomainRole**</span><span class="sxs-lookup"><span data-stu-id="79698-253">**DomainRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-254">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-256">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Directory Service (DS) estruturas \| [**DSROLE \_ Primary \_ Domain \_ info \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ Machine \_ role**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| MachineRole")</span><span class="sxs-lookup"><span data-stu-id="79698-256">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Directory Service (Ds) Structures\| [**DSROLE\_PRIMARY\_DOMAIN\_INFO\_BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic)\|[**DSROLE\_MACHINE\_ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role)\| MachineRole")</span></span>
</dt> </dl>

<span data-ttu-id="79698-257">Função de um computador em um grupo de trabalho de domínio atribuído.</span><span class="sxs-lookup"><span data-stu-id="79698-257">Role of a computer in an assigned domain workgroup.</span></span> <span data-ttu-id="79698-258">Um grupo de trabalho de domínio é uma coleção de computadores na mesma rede.</span><span class="sxs-lookup"><span data-stu-id="79698-258">A domain workgroup is a collection of computers on the same network.</span></span> <span data-ttu-id="79698-259">Por exemplo, uma propriedade **DomainRole** pode mostrar que um computador é uma estação de trabalho membro.</span><span class="sxs-lookup"><span data-stu-id="79698-259">For example, a **DomainRole** property may show that a computer is a member workstation.</span></span>

<span data-ttu-id="79698-260">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79698-260">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

<span data-ttu-id="79698-261">**Estação de trabalho autônoma** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-261">**Standalone Workstation** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

<span data-ttu-id="79698-262">**Estação de trabalho membro** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-262">**Member Workstation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

<span data-ttu-id="79698-263">**Servidor autônomo** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-263">**Standalone Server** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

<span data-ttu-id="79698-264">**Servidor membro** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-264">**Member Server** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="79698-265">**Controlador de domínio de backup** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-265">**Backup Domain Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="79698-266">**Controlador de domínio primário** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-266">**Primary Domain Controller** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-267">**EnableDaylightSavingsTime**</span><span class="sxs-lookup"><span data-stu-id="79698-267">**EnableDaylightSavingsTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-268">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-269">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="79698-270">Habilita o horário de Verão (DST) em um computador.</span><span class="sxs-lookup"><span data-stu-id="79698-270">Enables daylight savings time (DST) on a computer.</span></span> <span data-ttu-id="79698-271">Um valor **true** indica que a hora do sistema muda para uma hora à frente ou atrás quando o DST inicia ou termina.</span><span class="sxs-lookup"><span data-stu-id="79698-271">A value of **True** indicates that the system time changes to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="79698-272">Um valor **false** indica que a hora do sistema não muda para uma hora à frente ou atrás quando o DST inicia ou termina.</span><span class="sxs-lookup"><span data-stu-id="79698-272">A value of **False** indicates that the system time does not change to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="79698-273">Um valor **NULL** indica que o status do DST é desconhecido em um sistema.</span><span class="sxs-lookup"><span data-stu-id="79698-273">A value of **NULL** indicates that the DST status is unknown on a system.</span></span>

</dd> <dt>

<span data-ttu-id="79698-274">**FrontPanelResetStatus**</span><span class="sxs-lookup"><span data-stu-id="79698-274">**FrontPanelResetStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-275">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-277">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| configurações de segurança de hardware \| FrontPanelResetStatus")</span><span class="sxs-lookup"><span data-stu-id="79698-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|FrontPanelResetStatus")</span></span>
</dt> </dl>

<span data-ttu-id="79698-278">A tabela a seguir lista as configurações de segurança de hardware para o botão redefinir em um computador.</span><span class="sxs-lookup"><span data-stu-id="79698-278">The following table lists the hardware security settings for the reset button on a computer.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79698-279">**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-279">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79698-280">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-280">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="79698-281">**Não implementado** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-281">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-282">**Desconhecido** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-282">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-283">**HypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="79698-283">**HypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-284">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-286">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="79698-286">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="79698-287">Se for **true**, um hipervisor estará presente.</span><span class="sxs-lookup"><span data-stu-id="79698-287">If **True**, a hypervisor is present.</span></span>

<span data-ttu-id="79698-288">**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="79698-288">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="79698-289">**InfraredSupported**</span><span class="sxs-lookup"><span data-stu-id="79698-289">**InfraredSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-290">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-292">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="79698-292">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="79698-293">Se **for true**, uma porta de infravermelho (ir) existirá em um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="79698-293">If **True**, an infrared (IR) port exists on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="79698-294">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="79698-294">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-295">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79698-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79698-297">Dados necessários para localizar o dispositivo de carregamento inicial ou o serviço de inicialização para solicitar que o sistema operacional seja inicializado.</span><span class="sxs-lookup"><span data-stu-id="79698-297">Data required to find the initial load device or boot service to request that the operating system start up.</span></span>

<span data-ttu-id="79698-298">Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="79698-298">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<span data-ttu-id="79698-299">**Windows Server 2008 R2:** Essa propriedade está disponível, mas vazia.</span><span class="sxs-lookup"><span data-stu-id="79698-299">**Windows Server 2008 R2:** This property is available, but empty.</span></span>

</dd> <dt>

<span data-ttu-id="79698-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="79698-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-301">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79698-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79698-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-303">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="79698-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="79698-304">O objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="79698-304">Object is installed.</span></span> <span data-ttu-id="79698-305">Um objeto não precisa de um valor para indicar que ele está instalado.</span><span class="sxs-lookup"><span data-stu-id="79698-305">An object does not need a value to indicate that it is installed.</span></span>

<span data-ttu-id="79698-306">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79698-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-307">**KeyboardPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="79698-307">**KeyboardPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-308">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-310">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| configurações de segurança de hardware \| KeyboardPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="79698-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|KeyboardPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="79698-311">Configurações de segurança de hardware do sistema para status da senha do teclado.</span><span class="sxs-lookup"><span data-stu-id="79698-311">System hardware security settings for Keyboard Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79698-312">**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-312">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79698-313">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-313">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="79698-314">**Não implementado** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-314">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-315">**Desconhecido** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-315">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-316">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="79698-316">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79698-319">Entrada de matriz da propriedade **InitialLoadInfo** que contém os dados para iniciar o sistema operacional carregado.</span><span class="sxs-lookup"><span data-stu-id="79698-319">Array entry of the **InitialLoadInfo** property that contains the data to start the loaded operating system.</span></span>

<span data-ttu-id="79698-320">Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="79698-320">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-321">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="79698-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-324">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("fabricante de informações do sistema do SMBIOS \| tipo 1 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="79698-325">Nome do fabricante de um computador.</span><span class="sxs-lookup"><span data-stu-id="79698-325">Name of a computer manufacturer.</span></span>

<span data-ttu-id="79698-326">Exemplo: Adventure Works</span><span class="sxs-lookup"><span data-stu-id="79698-326">Example: Adventure Works</span></span>

</dd> <dt>

<span data-ttu-id="79698-327">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="79698-327">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-330">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 1 \| nome do produto informações do sistema \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Product Name")</span></span>
</dt> </dl>

<span data-ttu-id="79698-331">Nome do produto que um fabricante fornece a um computador.</span><span class="sxs-lookup"><span data-stu-id="79698-331">Product name that a manufacturer gives to a computer.</span></span> <span data-ttu-id="79698-332">Essa propriedade deve ter um valor.</span><span class="sxs-lookup"><span data-stu-id="79698-332">This property must have a value.</span></span>

</dd> <dt>

<span data-ttu-id="79698-333">**Nome**</span><span class="sxs-lookup"><span data-stu-id="79698-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-336">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="79698-336">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="79698-337">Chave de uma instância do [**\_ sistema CIM**](cim-system.md) em um ambiente corporativo.</span><span class="sxs-lookup"><span data-stu-id="79698-337">Key of a [**CIM\_System**](cim-system.md) instance in an enterprise environment.</span></span>

<span data-ttu-id="79698-338">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79698-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-339">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="79698-339">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79698-342">Valor do **nome** do sistema de computador que é gerado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="79698-342">Computer system **Name** value that is generated automatically.</span></span> <span data-ttu-id="79698-343">O objeto [**CIM \_ ComputerSystem**](cim-computersystem.md) e seus derivados são objetos de nível superior do modelo CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="79698-343">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of the Common Information Model (CIM).</span></span> <span data-ttu-id="79698-344">Eles fornecem o escopo para vários componentes.</span><span class="sxs-lookup"><span data-stu-id="79698-344">They provide the scope for several components.</span></span> <span data-ttu-id="79698-345">São necessárias chaves de [**\_ sistema CIM**](cim-system.md) exclusivas, mas você pode definir uma heurística para criar o nome de sistema de sistemas **CIM \_** que gera o mesmo nome e é independente do protocolo de descoberta.</span><span class="sxs-lookup"><span data-stu-id="79698-345">Unique [**CIM\_System**](cim-system.md) keys are required, but you can define a heuristic to create the **CIM\_ComputerSystem** name that generates the same name, and is independent from the discovery protocol.</span></span> <span data-ttu-id="79698-346">Isso impede problemas de inventário e gerenciamento quando o mesmo ativo ou entidade é descoberto várias vezes, mas não pode ser resolvido para um objeto.</span><span class="sxs-lookup"><span data-stu-id="79698-346">This prevents inventory and management problems when the same asset or entity is discovered multiple times, but cannot be resolved to one object.</span></span> <span data-ttu-id="79698-347">É recomendável usar um heurístico, mas não obrigatório.</span><span class="sxs-lookup"><span data-stu-id="79698-347">Using a heuristic is recommended, but not required.</span></span>

<span data-ttu-id="79698-348">A heurística é descrita na especificação de modelo comum do CIM V2 e pressupõe que as regras documentadas sejam usadas para determinar e atribuir um nome.</span><span class="sxs-lookup"><span data-stu-id="79698-348">The heuristic is outlined in the CIM V2 Common Model specification, and assumes that the documented rules are used to determine and assign a name.</span></span> <span data-ttu-id="79698-349">A lista de valores **NameFormat** define o pedido para atribuir um nome de sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="79698-349">The **NameFormat** values list defines the order to assign a computer system name.</span></span> <span data-ttu-id="79698-350">Várias regras são mapeadas para o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="79698-350">Several rules map to the same value.</span></span>

<span data-ttu-id="79698-351">O valor do [**\_ nome de sistema CIM**](cim-computersystem.md) que é calculado usando o heurístico é o valor de chave do sistema.</span><span class="sxs-lookup"><span data-stu-id="79698-351">The [**CIM\_ComputerSystem Name**](cim-computersystem.md) value that is calculated using the heuristic is the key value of the system.</span></span> <span data-ttu-id="79698-352">No entanto, use aliases para atribuir um nome diferente para o **CIM \_ ComputerSystem**, que pode ser mais exclusivo para sua empresa.</span><span class="sxs-lookup"><span data-stu-id="79698-352">However, use aliases to assign a different name for **CIM\_ComputerSystem**, which can be more unique to your company.</span></span>

<span data-ttu-id="79698-353">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="79698-353">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="79698-354">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="79698-354">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="79698-355">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="79698-355">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="79698-356">**Discar** ("discar")</span><span class="sxs-lookup"><span data-stu-id="79698-356">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="79698-357">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="79698-357">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="79698-358">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="79698-358">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="79698-359">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="79698-359">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="79698-360">**X25** ("X25")</span><span class="sxs-lookup"><span data-stu-id="79698-360">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="79698-361">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="79698-361">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="79698-362">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="79698-362">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="79698-363">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="79698-363">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="79698-364">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="79698-364">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="79698-365">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="79698-365">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="79698-366">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="79698-366">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="79698-367">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="79698-367">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79698-368">**Outro** ("outro")</span><span class="sxs-lookup"><span data-stu-id="79698-368">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-369">**NetworkServerModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="79698-369">**NetworkServerModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-370">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-372">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management estruturas \| [**Server \_ info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ Type \| VA \_ Type \_ Server")</span><span class="sxs-lookup"><span data-stu-id="79698-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SERVER\_INFO\_101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101)\|sv101\_type\|SV\_TYPE\_SERVER")</span></span>
</dt> </dl>

<span data-ttu-id="79698-373">Se for **true**, o modo de servidor de rede será habilitado.</span><span class="sxs-lookup"><span data-stu-id="79698-373">If **True**, the network Server Mode is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="79698-374">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="79698-374">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-375">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79698-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79698-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-377">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="79698-377">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="79698-378">Número de processadores lógicos disponíveis no computador.</span><span class="sxs-lookup"><span data-stu-id="79698-378">Number of logical processors available on the computer.</span></span>

<span data-ttu-id="79698-379">Você pode usar **NumberOfLogicalProcessors** e **NumberOfProcessors** para determinar se o computador está hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="79698-379">You can use **NumberOfLogicalProcessors** and **NumberOfProcessors** to determine if the computer is hyperthreading.</span></span> <span data-ttu-id="79698-380">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="79698-380">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="79698-381">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="79698-381">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-382">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79698-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79698-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-384">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| informações do sistema de estruturas de informação do sistema \| [**\_**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors")</span><span class="sxs-lookup"><span data-stu-id="79698-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|dwNumberOfProcessors")</span></span>
</dt> </dl>

<span data-ttu-id="79698-385">Número de processadores físicos atualmente disponíveis em um sistema.</span><span class="sxs-lookup"><span data-stu-id="79698-385">Number of physical processors currently available on a system.</span></span> <span data-ttu-id="79698-386">Este é o número de processadores habilitados para um sistema, que não inclui os processadores desabilitados.</span><span class="sxs-lookup"><span data-stu-id="79698-386">This is the number of enabled processors for a system, which does not include the disabled processors.</span></span> <span data-ttu-id="79698-387">Se um sistema de computador tiver dois processadores físicos contendo dois processadores lógicos, o valor de **NumberOfProcessors** será 2 e **NumberOfLogicalProcessors** será 4.</span><span class="sxs-lookup"><span data-stu-id="79698-387">If a computer system has two physical processors each containing two logical processors, then the value of **NumberOfProcessors** is 2 and **NumberOfLogicalProcessors** is 4.</span></span> <span data-ttu-id="79698-388">Os processadores podem ser de vários núcleos ou podem ser processadores hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="79698-388">The processors may be multicore or they may be hyperthreading processors.</span></span> <span data-ttu-id="79698-389">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="79698-389">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="79698-390">**OEMLogoBitmap**</span><span class="sxs-lookup"><span data-stu-id="79698-390">**OEMLogoBitmap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-391">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="79698-391">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="79698-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-393">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="79698-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="79698-394">Lista de dados para um bitmap criado pelo OEM (fabricante original do equipamento).</span><span class="sxs-lookup"><span data-stu-id="79698-394">List of data for a bitmap that the original equipment manufacturer (OEM) creates.</span></span>

</dd> <dt>

<span data-ttu-id="79698-395">**OEMStringArray**</span><span class="sxs-lookup"><span data-stu-id="79698-395">**OEMStringArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-396">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-396">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79698-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-398">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 11 \| OEM Strings")</span><span class="sxs-lookup"><span data-stu-id="79698-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 11\|OEM Strings")</span></span>
</dt> </dl>

<span data-ttu-id="79698-399">Lista de cadeias de caracteres de forma livre que um OEM define.</span><span class="sxs-lookup"><span data-stu-id="79698-399">List of free-form strings that an OEM defines.</span></span> <span data-ttu-id="79698-400">Por exemplo, um OEM define os números de peça para documentos de referência do sistema, informações de contato do fabricante e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="79698-400">For example, an OEM defines the part numbers for system reference documents, manufacturer contact information, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="79698-401">**PartOfDomain**</span><span class="sxs-lookup"><span data-stu-id="79698-401">**PartOfDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-402">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-404">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="79698-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="79698-405">Se for **true**, o computador será parte de um domínio.</span><span class="sxs-lookup"><span data-stu-id="79698-405">If **True**, the computer is part of a domain.</span></span> <span data-ttu-id="79698-406">Se o valor for **NULL**, o computador não está em um domínio ou o status é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="79698-406">If the value is **NULL**, the computer is not in a domain or the status is unknown.</span></span> <span data-ttu-id="79698-407">Se você remover o computador de um domínio, o valor se tornará **falso**.</span><span class="sxs-lookup"><span data-stu-id="79698-407">If you remove the computer from a domain, the value becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="79698-408">**PauseAfterReset**</span><span class="sxs-lookup"><span data-stu-id="79698-408">**PauseAfterReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-409">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="79698-409">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="79698-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-411">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 23 \| timeout"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="79698-411">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="79698-412">Tempo de espera antes que uma reinicialização seja iniciada em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="79698-412">Time delay before a reboot is initiated in milliseconds.</span></span> <span data-ttu-id="79698-413">Ele é usado após um ciclo de energia do sistema, redefinição do sistema local ou remoto e redefinição automática do sistema.</span><span class="sxs-lookup"><span data-stu-id="79698-413">It is used after a system power cycle, local or remote system reset, and automatic system reset.</span></span> <span data-ttu-id="79698-414">Um valor de 1 (menos um) indica que o valor de pausa é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="79698-414">A value of  1 (minus one) indicates that the pause value is unknown.</span></span>

<span data-ttu-id="79698-415">**Windows Vista:** Esta propriedade pode retornar um número desconhecido.</span><span class="sxs-lookup"><span data-stu-id="79698-415">**Windows Vista:** This property may return an unknown number.</span></span>

</dd> <dt>

<span data-ttu-id="79698-416">**PCSystemType**</span><span class="sxs-lookup"><span data-stu-id="79698-416">**PCSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-417">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-419">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="79698-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="79698-420">Tipo de computador em uso, como laptop, desktop ou Tablet.</span><span class="sxs-lookup"><span data-stu-id="79698-420">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="79698-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Não especificado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="79698-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Área de trabalho** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="79698-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Móvel** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="79698-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Estação de trabalho** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="79698-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Servidor corporativo** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="79698-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Servidor Soho** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO Server** (5)</span></span>


</dt> <dd>

<span data-ttu-id="79698-427">Servidor de pequena empresa e escritório doméstico (SOHO)</span><span class="sxs-lookup"><span data-stu-id="79698-427">Small Office and Home Office (SOHO) Server</span></span>

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="79698-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**PC de dispositivo** (6)</span><span class="sxs-lookup"><span data-stu-id="79698-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="79698-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Servidor de desempenho** (7)</span><span class="sxs-lookup"><span data-stu-id="79698-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="79698-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (8)</span><span class="sxs-lookup"><span data-stu-id="79698-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-431">**PCSystemTypeEx**</span><span class="sxs-lookup"><span data-stu-id="79698-431">**PCSystemTypeEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-432">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-434">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="79698-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="79698-435">Tipo de computador em uso, como laptop, desktop ou Tablet.</span><span class="sxs-lookup"><span data-stu-id="79698-435">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<span data-ttu-id="79698-436">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não tem suporte antes do Windows 8.1 e do Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="79698-436">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="79698-437">**Não especificado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-437">**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="79698-438">**Área de trabalho** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-438">**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="79698-439">**Móvel** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-439">**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="79698-440">**Estação de trabalho** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-440">**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="79698-441">**Servidor corporativo** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-441">**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="79698-442">**Servidor Soho** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-442">**SOHO Server** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="79698-443">**PC de dispositivo** (6)</span><span class="sxs-lookup"><span data-stu-id="79698-443">**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="79698-444">**Servidor de desempenho** (7)</span><span class="sxs-lookup"><span data-stu-id="79698-444">**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

<span data-ttu-id="79698-445">**Slate** (8)</span><span class="sxs-lookup"><span data-stu-id="79698-445">**Slate** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="79698-446">**Máximo** (9)</span><span class="sxs-lookup"><span data-stu-id="79698-446">**Maximum** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-447">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="79698-447">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-448">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-448">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79698-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-450">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controles de energia do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="79698-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="79698-451">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79698-451">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="79698-452">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="79698-452">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="79698-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79698-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79698-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="79698-457">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="79698-457">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="79698-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="79698-459">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="79698-459">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="79698-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="79698-461">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="79698-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="79698-462">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="79698-462">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="79698-463">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="79698-463">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="79698-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="79698-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="79698-465">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="79698-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="79698-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="79698-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="79698-467">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="79698-467">Timed Power-On Supported</span></span>

<span data-ttu-id="79698-468">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="79698-468">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-469">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="79698-469">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-470">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79698-470">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79698-471">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79698-472">Se **for true**, o dispositivo poderá ser gerenciado por energia, por exemplo, um dispositivo pode ser colocado no modo de suspensão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="79698-472">If **True**, device can be power-managed, for example, a device can be put into suspend mode, and so on.</span></span> <span data-ttu-id="79698-473">Essa propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, mas indica que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="79698-473">This property does not indicate that power management features are enabled currently, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="79698-474">Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="79698-474">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-475">**PowerOnPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="79698-475">**PowerOnPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-476">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-476">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-478">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| configurações de segurança de hardware \| PowerOnPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="79698-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|PowerOnPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="79698-479">Configurações de segurança de hardware do sistema para Power-On status da senha.</span><span class="sxs-lookup"><span data-stu-id="79698-479">System hardware security settings for Power-On Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79698-480">**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-480">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79698-481">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-481">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="79698-482">**Não implementado** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-482">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-483">**Desconhecido** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-483">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-484">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="79698-484">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-485">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-486">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79698-487">Estado de energia atual de um computador e seu sistema operacional associado.</span><span class="sxs-lookup"><span data-stu-id="79698-487">Current power state of a computer and its associated operating system.</span></span> <span data-ttu-id="79698-488">Os Estados de economia de energia têm os seguintes valores: valor 4 (desconhecido) indica que o sistema é conhecido em um modo de economia de energia, mas seu status exato nesse modo é desconhecido; 2 (o modo de baixa energia) indica que o sistema está em um estado de economia de energia, mas ainda funcionando e pode exibir o desempenho degradado; 3 (em espera) indica que o sistema não está funcionando, mas pode ser levado a uma potência completa rapidamente; e 7 (aviso) indica que o sistema de computador está em um estado de aviso e um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="79698-488">The power saving states have the following values: Value 4 (Unknown) indicates that the system is known to be in a power save mode, but its exact status in this mode is unknown; 2 (Low Power Mode) indicates that the system is in a power save state, but still functioning and may exhibit degraded performance; 3 (Standby) indicates that the system is not functioning, but could be brought to full power quickly; and 7 (Warning) indicates that the computer system is in a warning state and a power save mode.</span></span>

<span data-ttu-id="79698-489">Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="79698-489">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="79698-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Energia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="79698-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="79698-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="79698-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="79698-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="79698-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (6** )</span><span class="sxs-lookup"><span data-stu-id="79698-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="79698-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (7)</span><span class="sxs-lookup"><span data-stu-id="79698-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="79698-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save-hibernar** (8)</span><span class="sxs-lookup"><span data-stu-id="79698-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="79698-499">Power Save Hibernate.</span><span class="sxs-lookup"><span data-stu-id="79698-499">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="79698-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Economia **de energia – soft off** (9)</span><span class="sxs-lookup"><span data-stu-id="79698-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="79698-501">Power Save soft off.</span><span class="sxs-lookup"><span data-stu-id="79698-501">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-502">**PowerSupplyState**</span><span class="sxs-lookup"><span data-stu-id="79698-502">**PowerSupplyState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-503">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-503">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-504">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-505">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("compartimento do sistema do SMBIOS \| tipo 3 \| ou \| estado da fonte de energia do chassi")</span><span class="sxs-lookup"><span data-stu-id="79698-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Power Supply State")</span></span>
</dt> </dl>

<span data-ttu-id="79698-506">Estado da fonte de energia ou suprimentos quando a última inicialização.</span><span class="sxs-lookup"><span data-stu-id="79698-506">State of the power supply or supplies when last booted.</span></span>

<span data-ttu-id="79698-507">Esse valor é proveniente do membro do **estado da fonte de energia** do compartimento do **sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="79698-507">This value comes from the **Power Supply State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="79698-508">A lista a seguir identifica os valores para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="79698-508">The following list identifies the values for this property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79698-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="79698-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Seguro** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="79698-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="79698-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="79698-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Não recuperável** (6)</span><span class="sxs-lookup"><span data-stu-id="79698-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non-recoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="79698-515">Não recuperável</span><span class="sxs-lookup"><span data-stu-id="79698-515">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-516">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="79698-516">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-517">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-518">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79698-519">Informações de contato do proprietário do sistema primário, por exemplo, número de telefone, endereço de email e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="79698-519">Contact information for the primary system owner, for example, phone number, email address, and so on.</span></span>

<span data-ttu-id="79698-520">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="79698-520">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-521">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="79698-521">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-522">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-523">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-524">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="79698-524">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="79698-525">Nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="79698-525">Name of the primary system owner.</span></span>

<span data-ttu-id="79698-526">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="79698-526">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-527">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="79698-527">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-528">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-529">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-530">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Segurança de hardware do sistema DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="79698-530">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="79698-531">Se habilitado, o valor é 4 e o sistema de computador unitário pode ser redefinido usando os botões potência e redefinição.</span><span class="sxs-lookup"><span data-stu-id="79698-531">If enabled, the value is 4 and the unitary computer system can be reset using the power and reset buttons.</span></span> <span data-ttu-id="79698-532">Se desabilitado, o valor será 3 e uma redefinição não será permitida.</span><span class="sxs-lookup"><span data-stu-id="79698-532">If disabled, the value is 3, and a reset is not allowed.</span></span>

<span data-ttu-id="79698-533">Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="79698-533">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79698-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79698-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79698-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="79698-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Não implementado** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Not Implemented** (5)</span></span>


</dt> <dd>

<span data-ttu-id="79698-539">Não recuperável</span><span class="sxs-lookup"><span data-stu-id="79698-539">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-540">**ResetCount**</span><span class="sxs-lookup"><span data-stu-id="79698-540">**ResetCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-541">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="79698-541">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-542">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-543">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| redefinetion Count redefinence \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\|Reset Count")</span></span>
</dt> </dl>

<span data-ttu-id="79698-544">Número de redefinições automáticas desde a última redefinição.</span><span class="sxs-lookup"><span data-stu-id="79698-544">Number of automatic resets since the last reset.</span></span> <span data-ttu-id="79698-545">Um valor de 1 (menos um) indica que a contagem é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="79698-545">A value of  1 (minus one) indicates that the count is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="79698-546">**ResetLimit**</span><span class="sxs-lookup"><span data-stu-id="79698-546">**ResetLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-547">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="79698-547">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-548">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-549">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 23 limite de redefinição do \| sistema \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\| Reset Limit")</span></span>
</dt> </dl>

<span data-ttu-id="79698-550">Número de vezes consecutivas em que uma reinicialização do sistema é tentada.</span><span class="sxs-lookup"><span data-stu-id="79698-550">Number of consecutive times a system reset is attempted.</span></span> <span data-ttu-id="79698-551">Um valor de 1 (menos um) indica que o limite é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="79698-551">A value of  1 (minus one) indicates that the limit is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="79698-552">**Funções**</span><span class="sxs-lookup"><span data-stu-id="79698-552">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-553">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-553">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79698-554">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="79698-555">Lista que especifica as funções de um sistema no ambiente de tecnologia da informação.</span><span class="sxs-lookup"><span data-stu-id="79698-555">List that specifies the roles of a system in the information technology environment.</span></span>

<span data-ttu-id="79698-556">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="79698-556">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="79698-557">**Status**</span><span class="sxs-lookup"><span data-stu-id="79698-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-558">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-559">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-560">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="79698-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="79698-561">Status atual de um objeto.</span><span class="sxs-lookup"><span data-stu-id="79698-561">Current status of an object.</span></span>

<span data-ttu-id="79698-562">Por Win32_ComputerSystem, o status é sempre "OK".</span><span class="sxs-lookup"><span data-stu-id="79698-562">For Win32_ComputerSystem, the Status is always “OK”.</span></span>

<span data-ttu-id="79698-563">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79698-563">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dl>

</dd> <dt>

<span data-ttu-id="79698-564">**SupportContactDescription**</span><span class="sxs-lookup"><span data-stu-id="79698-564">**SupportContactDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-565">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-565">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79698-566">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-567">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| support Information")</span><span class="sxs-lookup"><span data-stu-id="79698-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring)\|Support Information")</span></span>
</dt> </dl>

<span data-ttu-id="79698-568">Lista das informações de contato de suporte para o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="79698-568">List of the support contact information for the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="79698-569">**SystemFamily**</span><span class="sxs-lookup"><span data-stu-id="79698-569">**SystemFamily**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-570">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-571">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-572">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| família de informações do sistema SMBIOS tipo 1 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-572">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Family")</span></span>
</dt> </dl>

<span data-ttu-id="79698-573">A família à qual pertence um computador específico.</span><span class="sxs-lookup"><span data-stu-id="79698-573">The family to which a particular computer belongs.</span></span> <span data-ttu-id="79698-574">Uma família refere-se a um conjunto de computadores que são semelhantes, mas não idênticos, de um ponto de vista de hardware ou software.</span><span class="sxs-lookup"><span data-stu-id="79698-574">A family refers to a set of computers that are similar but not identical from a hardware or software point of view.</span></span>

<span data-ttu-id="79698-575">Esse valor é proveniente do membro da **família** da estrutura de **informações do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="79698-575">This value comes from the **Family** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="79698-576">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="79698-576">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="79698-577">**SystemSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="79698-577">**SystemSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-578">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-579">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-580">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 1 \| número de SKU de informações do sistema \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-580">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="79698-581">Identifica uma configuração de computador específica para venda.</span><span class="sxs-lookup"><span data-stu-id="79698-581">Identifies a particular computer configuration for sale.</span></span> <span data-ttu-id="79698-582">Às vezes, ele também é chamado de ID do produto ou número da ordem de compra.</span><span class="sxs-lookup"><span data-stu-id="79698-582">It is sometimes also called a product ID or purchase order number.</span></span>

<span data-ttu-id="79698-583">Esse valor é proveniente do membro **número da SKU** da estrutura de informações do **sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="79698-583">This value comes from the **SKU Number** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="79698-584">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="79698-584">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="79698-585">**SystemStartupDelay**</span><span class="sxs-lookup"><span data-stu-id="79698-585">**SystemStartupDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-586">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-586">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-587">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-587">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79698-588">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilégios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| tempo limite do carregador de inicialização \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="79698-588">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint)\|Boot Loader\|timeout"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="79698-589">O **SystemStartupDelay** não está mais disponível para uso porque Boot.ini não é usado para configurar a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="79698-589">**SystemStartupDelay** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="79698-590">Em vez disso, use as [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornecidas pelo provedor WMI de dados de configuração da inicialização (BCD) ou o comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="79698-590">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="79698-591">**SystemStartupOptions**</span><span class="sxs-lookup"><span data-stu-id="79698-591">**SystemStartupOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-592">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-592">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79698-593">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-593">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79698-594">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilégios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| Operating Systems")</span><span class="sxs-lookup"><span data-stu-id="79698-594">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection)\|Operating Systems")</span></span>
</dt> </dl>

<span data-ttu-id="79698-595">O **SystemStartupOptions** não está mais disponível para uso porque Boot.ini não é usado para configurar a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="79698-595">**SystemStartupOptions** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="79698-596">Em vez disso, use as [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornecidas pelo provedor WMI de dados de configuração da inicialização (BCD) ou o comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="79698-596">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="79698-597">**SystemStartupSetting**</span><span class="sxs-lookup"><span data-stu-id="79698-597">**SystemStartupSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-598">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="79698-598">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="79698-599">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-599">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79698-600">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilégios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="79698-600">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="79698-601">O **SystemStartupSetting** não está mais disponível para uso porque Boot.ini não é usado para configurar a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="79698-601">**SystemStartupSetting** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="79698-602">Em vez disso, use as [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornecidas pelo provedor WMI de dados de configuração da inicialização (BCD) ou o comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="79698-602">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="79698-603">**SystemType**</span><span class="sxs-lookup"><span data-stu-id="79698-603">**SystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-604">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-605">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-605">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-606">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| informações do sistema de estruturas de informação do sistema \| [**\_**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture")</span><span class="sxs-lookup"><span data-stu-id="79698-606">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|wProcessorArchitecture")</span></span>
</dt> </dl>

<span data-ttu-id="79698-607">Sistema em execução no computador baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="79698-607">System running on the Windows-based computer.</span></span> <span data-ttu-id="79698-608">Essa propriedade deve ter um valor.</span><span class="sxs-lookup"><span data-stu-id="79698-608">This property must have a value.</span></span>

<span data-ttu-id="79698-609">A lista a seguir identifica alguns dos valores possíveis para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="79698-609">The following list identifies some of the possible values for this property.</span></span>

<dl> <dd><span data-ttu-id="79698-610">"PC baseado em x64"</span><span class="sxs-lookup"><span data-stu-id="79698-610">"x64-based PC"</span></span></dd> <dd><span data-ttu-id="79698-611">"PC baseado em x86"</span><span class="sxs-lookup"><span data-stu-id="79698-611">"X86-based PC"</span></span></dd> <dd><span data-ttu-id="79698-612">"PC baseado em MIPS"</span><span class="sxs-lookup"><span data-stu-id="79698-612">"MIPS-based PC"</span></span></dd> <dd><span data-ttu-id="79698-613">"PC baseado em Alpha"</span><span class="sxs-lookup"><span data-stu-id="79698-613">"Alpha-based PC"</span></span></dd> <dd><span data-ttu-id="79698-614">"Power PC"</span><span class="sxs-lookup"><span data-stu-id="79698-614">"Power PC"</span></span></dd> <dd><span data-ttu-id="79698-615">"SH-x PC"</span><span class="sxs-lookup"><span data-stu-id="79698-615">"SH-x PC"</span></span></dd> <dd><span data-ttu-id="79698-616">"PC StrongARM"</span><span class="sxs-lookup"><span data-stu-id="79698-616">"StrongARM PC"</span></span></dd> <dd><span data-ttu-id="79698-617">"PC Intel de 64 bits"</span><span class="sxs-lookup"><span data-stu-id="79698-617">"64-bit Intel PC"</span></span></dd> <dd><span data-ttu-id="79698-618">"PC Alpha de 64 bits"</span><span class="sxs-lookup"><span data-stu-id="79698-618">"64-bit Alpha PC"</span></span></dd> <dd><span data-ttu-id="79698-619">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="79698-619">"Unknown"</span></span></dd> <dd><span data-ttu-id="79698-620">"Computador x86-Nec98"</span><span class="sxs-lookup"><span data-stu-id="79698-620">"X86-Nec98 PC"</span></span></dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

<span data-ttu-id="79698-621">**PC baseado em x86** ("PC baseado em x86")</span><span class="sxs-lookup"><span data-stu-id="79698-621">**X86-based PC** ("X86-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

<span data-ttu-id="79698-622">**PC baseado em MIPS** ("PC baseado em MIPS")</span><span class="sxs-lookup"><span data-stu-id="79698-622">**MIPS-based PC** ("MIPS-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

<span data-ttu-id="79698-623">**PC baseado em Alpha** ("PC baseado em Alpha")</span><span class="sxs-lookup"><span data-stu-id="79698-623">**Alpha-based PC** ("Alpha-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

<span data-ttu-id="79698-624">**Power PC** ("Power PC")</span><span class="sxs-lookup"><span data-stu-id="79698-624">**Power PC** ("Power PC")</span></span>


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

<span data-ttu-id="79698-625">**Sh-x PC** ("sh-x PC")</span><span class="sxs-lookup"><span data-stu-id="79698-625">**SH-x PC** ("SH-x PC")</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

<span data-ttu-id="79698-626">**STRONGARM PC** ("StrongARM PC")</span><span class="sxs-lookup"><span data-stu-id="79698-626">**StrongARM PC** ("StrongARM PC")</span></span>


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

<span data-ttu-id="79698-627">**PC Intel de 64 bits** ("PC intel de 64 bits")</span><span class="sxs-lookup"><span data-stu-id="79698-627">**64-bit Intel PC** ("64-bit Intel PC")</span></span>


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

<span data-ttu-id="79698-628">**PC baseado em x64** ("PC baseado em x64")</span><span class="sxs-lookup"><span data-stu-id="79698-628">**x64-based PC** ("x64-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-629">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="79698-629">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

<span data-ttu-id="79698-630">**Computador x86-Nec98** ("x86-Nec98 PC")</span><span class="sxs-lookup"><span data-stu-id="79698-630">**X86-Nec98 PC** ("X86-Nec98 PC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-631">**Termalstate**</span><span class="sxs-lookup"><span data-stu-id="79698-631">**ThermalState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-632">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-632">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-633">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-634">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("compartimento do sistema do SMBIOS \| tipo 3 \| ou \| estado térmico do chassi")</span><span class="sxs-lookup"><span data-stu-id="79698-634">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Thermal State")</span></span>
</dt> </dl>

<span data-ttu-id="79698-635">Estado térmico do sistema quando a última inicialização.</span><span class="sxs-lookup"><span data-stu-id="79698-635">Thermal state of the system when last booted.</span></span>

<span data-ttu-id="79698-636">Esse valor é proveniente do membro de **estado térmico** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="79698-636">This value comes from the **Thermal State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79698-637">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-637">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-638">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-638">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="79698-639">**Seguro** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-639">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="79698-640">**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-640">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="79698-641">**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-641">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="79698-642">**Não recuperável** (6)</span><span class="sxs-lookup"><span data-stu-id="79698-642">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-643">**TotalPhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="79698-643">**TotalPhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-644">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79698-644">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79698-645">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-646">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de gerenciamento de memória win32api \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="79698-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus)\|dwTotalPhys"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="79698-647">Tamanho total da memória física.</span><span class="sxs-lookup"><span data-stu-id="79698-647">Total size of physical memory.</span></span> <span data-ttu-id="79698-648">Lembre-se de que, em algumas circunstâncias, essa propriedade pode não retornar um valor preciso para a memória física.</span><span class="sxs-lookup"><span data-stu-id="79698-648">Be aware that, under some circumstances, this property may not return an accurate value for the physical memory.</span></span> <span data-ttu-id="79698-649">Por exemplo, não será preciso se o BIOS estiver usando parte da memória física.</span><span class="sxs-lookup"><span data-stu-id="79698-649">For example, it is not accurate if the BIOS is using some of the physical memory.</span></span> <span data-ttu-id="79698-650">Para um valor preciso, use a propriedade **Capacity** no [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="79698-650">For an accurate value, use the **Capacity** property in [**Win32\_PhysicalMemory**](win32-physicalmemory.md) instead.</span></span>

<span data-ttu-id="79698-651">Exemplo: 67108864</span><span class="sxs-lookup"><span data-stu-id="79698-651">Example: 67108864</span></span>

<span data-ttu-id="79698-652">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="79698-652">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="79698-653">**UserName**</span><span class="sxs-lookup"><span data-stu-id="79698-653">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-654">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-654">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-655">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-655">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-656">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| funções de informações do sistema \ \| [**username**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span><span class="sxs-lookup"><span data-stu-id="79698-656">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Functions\|[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span></span>
</dt> </dl>

<span data-ttu-id="79698-657">Nome de um usuário que está conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="79698-657">Name of a user that is logged on currently.</span></span> <span data-ttu-id="79698-658">Essa propriedade deve ter um valor.</span><span class="sxs-lookup"><span data-stu-id="79698-658">This property must have a value.</span></span> <span data-ttu-id="79698-659">Em uma sessão de serviços de terminal, **username** retorna o nome do usuário que fez logon no console, não o usuário conectado durante a sessão de serviço de terminal.</span><span class="sxs-lookup"><span data-stu-id="79698-659">In a terminal services session, **UserName** returns the name of the user that is logged on to the console not the user logged on during the terminal service session.</span></span>

<span data-ttu-id="79698-660">Exemplo: jeffsmith</span><span class="sxs-lookup"><span data-stu-id="79698-660">Example: jeffsmith</span></span>

</dd> <dt>

<span data-ttu-id="79698-661">**Ativartype**</span><span class="sxs-lookup"><span data-stu-id="79698-661">**WakeUpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-662">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79698-662">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79698-663">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79698-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79698-664">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| tipo de ativação de informações do sistema SMBIOS tipo 1 \| ")</span><span class="sxs-lookup"><span data-stu-id="79698-664">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Wake-up Type")</span></span>
</dt> </dl>

<span data-ttu-id="79698-665">Evento que faz com que o sistema ligue.</span><span class="sxs-lookup"><span data-stu-id="79698-665">Event that causes the system to power up.</span></span>

<span data-ttu-id="79698-666">Esse valor é proveniente do membro do **tipo de ativação** da estrutura de **informações do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="79698-666">This value comes from the **Wake-up Type** member of the **System Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="79698-667">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="79698-667">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79698-668">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79698-668">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79698-669">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79698-669">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

<span data-ttu-id="79698-670">**Temporizador APM** (3)</span><span class="sxs-lookup"><span data-stu-id="79698-670">**APM Timer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

<span data-ttu-id="79698-671">**Modem Ring** (4)</span><span class="sxs-lookup"><span data-stu-id="79698-671">**Modem Ring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

<span data-ttu-id="79698-672">**LAN remota** (5)</span><span class="sxs-lookup"><span data-stu-id="79698-672">**LAN Remote** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

<span data-ttu-id="79698-673">**Botão de energia** (6)</span><span class="sxs-lookup"><span data-stu-id="79698-673">**Power Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

<span data-ttu-id="79698-674">**PME \# de PCI** 7</span><span class="sxs-lookup"><span data-stu-id="79698-674">**PCI PME\#** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

<span data-ttu-id="79698-675">**Energia CA restaurada** (8)</span><span class="sxs-lookup"><span data-stu-id="79698-675">**AC Power Restored** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79698-676">**Grupo de trabalho**</span><span class="sxs-lookup"><span data-stu-id="79698-676">**Workgroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79698-677">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79698-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79698-678">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="79698-678">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="79698-679">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="79698-679">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="79698-680">Nome do grupo de trabalho deste computador.</span><span class="sxs-lookup"><span data-stu-id="79698-680">Name of the workgroup for this computer.</span></span> <span data-ttu-id="79698-681">Se o valor da propriedade **PartOfDomain** for **false**, o nome do grupo de trabalho será retornado.</span><span class="sxs-lookup"><span data-stu-id="79698-681">If the value of the **PartOfDomain** property is **False**, then the name of the workgroup is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79698-682">Comentários</span><span class="sxs-lookup"><span data-stu-id="79698-682">Remarks</span></span>

<span data-ttu-id="79698-683">Para determinar o número total de instâncias de processador associadas a um objeto de sistema de computador, use a classe de associação [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="79698-683">To determine the total number of processor instances associated with a computer system object, use the [**Win32\_ComputerSystemProcessor**](win32-computersystemprocessor.md) association class.</span></span>

<span data-ttu-id="79698-684">Uma instância de **\_ ComputerSystem do Win32** que tem vários processadores físicos tem várias instâncias de [**\_ processador Win32**](win32-processor.md) associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="79698-684">A **Win32\_ComputerSystem** instance that has multiple physical processors has multiple [**Win32\_Processor**](win32-processor.md) instances associated with it.</span></span> <span data-ttu-id="79698-685">Se o valor de **NumberOfLogicalProcessors** for maior que o valor de **NumberOfProcessors** , o sistema de computador será um sistema de vários núcleos ou terá um ou mais processadores habilitados para hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="79698-685">If the value of **NumberOfLogicalProcessors** is greater than the value of **NumberOfProcessors** then the computer system is either a multicore system or has one or more processors enabled for hyperthreading.</span></span> <span data-ttu-id="79698-686">Para obter mais informações, consulte a seção Propriedades e comentários do **NumberOfLogicalProcessors** e do **NumberOfCores** no **\_ processador Win32**.</span><span class="sxs-lookup"><span data-stu-id="79698-686">For more information, see the **NumberOfLogicalProcessors** and **NumberOfCores** properties and Remarks section in **Win32\_Processor**.</span></span>

<span data-ttu-id="79698-687">A classe de **\_ ComputerSystem do Win32** é derivada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="79698-687">The **Win32\_ComputerSystem** class is derived from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

## <a name="examples"></a><span data-ttu-id="79698-688">Exemplos</span><span class="sxs-lookup"><span data-stu-id="79698-688">Examples</span></span>

<span data-ttu-id="79698-689">O [exemplo de código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) do centro de scripts a seguir usa o **\_ sistema** de computadores Win32 para recuperar informações de vários sistemas de computador e EXIBI-los em uma GUI.</span><span class="sxs-lookup"><span data-stu-id="79698-689">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) uses the **Win32\_ComputerSystem** to retrieve information from a number of computer systems, and display them in a GUI.</span></span>

<span data-ttu-id="79698-690">Você pode encontrar um exemplo de script que obtém os dados do sistema operacional e do processador do **Win32 \_ ComputerSystem**, do [**\_ processador Win32**](win32-processor.md)e do [**\_ OperatingSystem do Win32**](win32-operatingsystem.md) nos exemplos de tópico do [**\_ processador Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="79698-690">You can find an example script that obtains operating system and processor data from **Win32\_ComputerSystem**, [**Win32\_Processor**](win32-processor.md), and [**Win32\_OperatingSystem**](win32-operatingsystem.md) in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="79698-691">O exemplo de VBScript a seguir descreve como recuperar o nome de domínio do computador local de instâncias do **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="79698-691">The following VBScript sample describes how to retrieve the domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



<span data-ttu-id="79698-692">O exemplo do Perl a seguir descreve como recuperar o nome do computador local de instâncias do **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="79698-692">The following Perl sample describes how to retrieve the local machine name from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="79698-693">O exemplo do Perl a seguir descreve como recuperar o nome de domínio DNS do computador local de instâncias do **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="79698-693">The following Perl sample describes how to retrieve the DNS domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="79698-694">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79698-694">Requirements</span></span>



| <span data-ttu-id="79698-695">Requisito</span><span class="sxs-lookup"><span data-stu-id="79698-695">Requirement</span></span> | <span data-ttu-id="79698-696">Valor</span><span class="sxs-lookup"><span data-stu-id="79698-696">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79698-697">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79698-697">Minimum supported client</span></span><br/> | <span data-ttu-id="79698-698">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79698-698">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79698-699">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79698-699">Minimum supported server</span></span><br/> | <span data-ttu-id="79698-700">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79698-700">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79698-701">Namespace</span><span class="sxs-lookup"><span data-stu-id="79698-701">Namespace</span></span><br/>                | <span data-ttu-id="79698-702">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="79698-702">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79698-703">MOF</span><span class="sxs-lookup"><span data-stu-id="79698-703">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79698-704"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79698-704"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79698-705">DLL</span><span class="sxs-lookup"><span data-stu-id="79698-705">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79698-706"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79698-706"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79698-707">Confira também</span><span class="sxs-lookup"><span data-stu-id="79698-707">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79698-708">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="79698-708">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dt>

<span data-ttu-id="79698-709">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79698-709">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="79698-710">Tarefas do WMI: contas e domínios</span><span class="sxs-lookup"><span data-stu-id="79698-710">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="79698-711">Tarefas do WMI: hardware do computador</span><span class="sxs-lookup"><span data-stu-id="79698-711">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="79698-712">Tarefas do WMI: gerenciamento de desktop</span><span class="sxs-lookup"><span data-stu-id="79698-712">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

