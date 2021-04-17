---
description: O Win32 \_ OSRecoveryConfiguration&\# 8194; A classe WMI representa os tipos de informações que serão coletadas da memória quando o sistema operacional falhar. Isso inclui falhas de inicialização e falha do sistema.
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Classe Win32_OSRecoveryConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2371ba7ee449497e2d695e60d75c59454282d54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756034"
---
# <a name="win32_osrecoveryconfiguration-class"></a><span data-ttu-id="d70d7-104">\_Classe Win32 OSRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d70d7-104">Win32\_OSRecoveryConfiguration class</span></span>

<span data-ttu-id="d70d7-105">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OSRecoveryConfiguration do Win32** representa os tipos de informações que serão coletadas da memória quando o sistema operacional falhar.</span><span class="sxs-lookup"><span data-stu-id="d70d7-105">The **Win32\_OSRecoveryConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the types of information that will be gathered from memory when the operating system fails.</span></span> <span data-ttu-id="d70d7-106">Isso inclui falhas de inicialização e falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="d70d7-106">This includes boot failures and system crashes.</span></span>

<span data-ttu-id="d70d7-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d70d7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d70d7-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="d70d7-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d70d7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d70d7-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="d70d7-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d70d7-110">Members</span></span>

<span data-ttu-id="d70d7-111">A classe **Win32 \_ OSRecoveryConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d70d7-111">The **Win32\_OSRecoveryConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="d70d7-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d70d7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d70d7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d70d7-113">Properties</span></span>

<span data-ttu-id="d70d7-114">A classe **Win32 \_ OSRecoveryConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d70d7-114">The **Win32\_OSRecoveryConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d70d7-115">**Reinicialização**</span><span class="sxs-lookup"><span data-stu-id="d70d7-115">**AutoReboot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d70d7-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-118">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ controle \\ \\ CrashControl \| reboot")</span><span class="sxs-lookup"><span data-stu-id="d70d7-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-119">O sistema será reinicializado automaticamente durante uma operação de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d70d7-119">System will automatically reboot during a recovery operation.</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-120">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d70d7-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70d7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d70d7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-123">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d70d7-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-124">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="d70d7-124">Short textual description of the current object.</span></span>

<span data-ttu-id="d70d7-125">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d70d7-125">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-126">**DebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="d70d7-126">**DebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70d7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-129">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ controle \\ \\ CrashControl \| dumpfile")</span><span class="sxs-lookup"><span data-stu-id="d70d7-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|DumpFile")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-130">Caminho completo para o arquivo de depuração.</span><span class="sxs-lookup"><span data-stu-id="d70d7-130">Full path to the debug file.</span></span> <span data-ttu-id="d70d7-131">Um arquivo de depuração é criado com o estado de memória do computador após uma falha do computador.</span><span class="sxs-lookup"><span data-stu-id="d70d7-131">A debug file is created with the memory state of the computer after a computer failure.</span></span>

<span data-ttu-id="d70d7-132">Exemplo: "C: \\ Windows \\ Memory. dmp"</span><span class="sxs-lookup"><span data-stu-id="d70d7-132">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-133">**DebugInfoType**</span><span class="sxs-lookup"><span data-stu-id="d70d7-133">**DebugInfoType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d70d7-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-136">Tipo de informações de depuração gravadas no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="d70d7-136">Type of debugging information written to the log file.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d70d7-137">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="d70d7-137">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

<span data-ttu-id="d70d7-138">**Despejo de memória completo** (1)</span><span class="sxs-lookup"><span data-stu-id="d70d7-138">**Complete memory dump** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

<span data-ttu-id="d70d7-139">**Despejo de memória do kernel** (2)</span><span class="sxs-lookup"><span data-stu-id="d70d7-139">**Kernel memory dump** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

<span data-ttu-id="d70d7-140">**Despejo de memória pequeno** (3)</span><span class="sxs-lookup"><span data-stu-id="d70d7-140">**Small memory dump** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d70d7-141">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d70d7-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70d7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d70d7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-144">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="d70d7-144">Textual description of the current object.</span></span>

<span data-ttu-id="d70d7-145">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d70d7-145">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-146">**ExpandedDebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="d70d7-146">**ExpandedDebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70d7-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-149">Versão expandida da propriedade **DebugFilePath** .</span><span class="sxs-lookup"><span data-stu-id="d70d7-149">Expanded version of the **DebugFilePath** property.</span></span>

<span data-ttu-id="d70d7-150">Exemplo: "C: \\ Windows \\ Memory. dmp"</span><span class="sxs-lookup"><span data-stu-id="d70d7-150">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-151">**ExpandedMiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="d70d7-151">**ExpandedMiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70d7-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-154">Versão expandida da propriedade **MiniDumpDirectory** .</span><span class="sxs-lookup"><span data-stu-id="d70d7-154">Expanded version of the **MiniDumpDirectory** property.</span></span>

<span data-ttu-id="d70d7-155">Exemplo: "C: \\ minidespejo do Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="d70d7-155">Example: "C:\\Windows\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-156">**KernelDumpOnly**</span><span class="sxs-lookup"><span data-stu-id="d70d7-156">**KernelDumpOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-157">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d70d7-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-159">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| KernelDumpOnly")</span><span class="sxs-lookup"><span data-stu-id="d70d7-159">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|KernelDumpOnly")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-160">Somente as informações de depuração do kernel serão gravadas no arquivo de log de depuração.</span><span class="sxs-lookup"><span data-stu-id="d70d7-160">Only kernel debug information will be written to the debug log file.</span></span> <span data-ttu-id="d70d7-161">Se **for true**, somente o estado do kernel será gravado em um arquivo no caso de uma falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="d70d7-161">If **TRUE**, then only the state of the kernel is written to a file in the event of a system failure.</span></span> <span data-ttu-id="d70d7-162">Se **for false**, o sistema tentará registrar em log o estado da memória e quaisquer dispositivos que possam fornecer informações sobre o sistema quando ele falhar.</span><span class="sxs-lookup"><span data-stu-id="d70d7-162">If **FALSE**, the system will try to log the state of the memory, and any devices that can provide information about the system when it failed.</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-163">**MiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="d70d7-163">**MiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70d7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-166">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| MiniDumpDir")</span><span class="sxs-lookup"><span data-stu-id="d70d7-166">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|MiniDumpDir")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-167">Diretório em que os arquivos de despejo de memória pequenos serão registrados e acumulados.</span><span class="sxs-lookup"><span data-stu-id="d70d7-167">Directory where small memory dump files will be recorded and accumulated.</span></span>

<span data-ttu-id="d70d7-168">Exemplo: "% systemRoot% \\ minidespejo"</span><span class="sxs-lookup"><span data-stu-id="d70d7-168">Example: "%systemRoot%\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-169">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d70d7-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70d7-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d70d7-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-172">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d70d7-172">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-173">Nome de identificação para esta instância da classe **Win32 \_ OSRecoveryConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="d70d7-173">Identifying name for this instance of the **Win32\_OSRecoveryConfiguration** class.</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-174">**OverwriteExistingDebugFile**</span><span class="sxs-lookup"><span data-stu-id="d70d7-174">**OverwriteExistingDebugFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-175">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d70d7-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-176">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-177">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ controle \\ \\ CrashControl \| substituir")</span><span class="sxs-lookup"><span data-stu-id="d70d7-177">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|Overwrite")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-178">O novo arquivo de depuração substituirá um existente.</span><span class="sxs-lookup"><span data-stu-id="d70d7-178">New debug file will overwrite an existing one.</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-179">**SendAdminAlert**</span><span class="sxs-lookup"><span data-stu-id="d70d7-179">**SendAdminAlert**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-180">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d70d7-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-182">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| SendAlert")</span><span class="sxs-lookup"><span data-stu-id="d70d7-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|SendAlert")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-183">A mensagem de alerta será enviada ao administrador do sistema no caso de uma falha do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d70d7-183">Alert message will be sent to the system administrator in the event of an operating system failure.</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-184">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="d70d7-184">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70d7-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d70d7-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-187">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d70d7-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-188">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="d70d7-188">Identifier by which the current object is known.</span></span>

<span data-ttu-id="d70d7-189">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d70d7-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-190">**WriteDebugInfo**</span><span class="sxs-lookup"><span data-stu-id="d70d7-190">**WriteDebugInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-191">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d70d7-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-193">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| CrashDumpEnabled")</span><span class="sxs-lookup"><span data-stu-id="d70d7-193">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|CrashDumpEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-194">As informações de depuração são gravadas em um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="d70d7-194">Debugging information is to be written to a log file.</span></span>

</dd> <dt>

<span data-ttu-id="d70d7-195">**WriteToSystemLog**</span><span class="sxs-lookup"><span data-stu-id="d70d7-195">**WriteToSystemLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70d7-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d70d7-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-197">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70d7-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d70d7-198">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| LogEvent")</span><span class="sxs-lookup"><span data-stu-id="d70d7-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|LogEvent")</span></span>
</dt> </dl>

<span data-ttu-id="d70d7-199">Os eventos serão gravados em um log do sistema.</span><span class="sxs-lookup"><span data-stu-id="d70d7-199">Events will be written to a system log.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d70d7-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="d70d7-200">Remarks</span></span>

<span data-ttu-id="d70d7-201">A classe **Win32 \_ OSRecoveryConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="d70d7-201">The **Win32\_OSRecoveryConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d70d7-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d70d7-202">Requirements</span></span>



| <span data-ttu-id="d70d7-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="d70d7-203">Requirement</span></span> | <span data-ttu-id="d70d7-204">Valor</span><span class="sxs-lookup"><span data-stu-id="d70d7-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d70d7-205">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d70d7-205">Minimum supported client</span></span><br/> | <span data-ttu-id="d70d7-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d70d7-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d70d7-207">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d70d7-207">Minimum supported server</span></span><br/> | <span data-ttu-id="d70d7-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d70d7-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d70d7-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="d70d7-209">Namespace</span></span><br/>                | <span data-ttu-id="d70d7-210">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d70d7-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d70d7-211">MOF</span><span class="sxs-lookup"><span data-stu-id="d70d7-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d70d7-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d70d7-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d70d7-213">DLL</span><span class="sxs-lookup"><span data-stu-id="d70d7-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d70d7-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d70d7-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d70d7-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="d70d7-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d70d7-216">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d70d7-216">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="d70d7-217">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d70d7-217">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
