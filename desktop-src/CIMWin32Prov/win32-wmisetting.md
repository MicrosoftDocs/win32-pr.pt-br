---
description: A \_ classe WMI singleton do Win32 WMISetting contém os parâmetros operacionais para o serviço WMI. Essa classe pode ter apenas uma instância, que sempre existe para cada sistema Windows e não pode ser excluída. Não é possível criar instâncias adicionais.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Classe Win32_WMISetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826171"
---
# <a name="win32_wmisetting-class"></a><span data-ttu-id="633e4-105">\_Classe Win32 WMISetting</span><span class="sxs-lookup"><span data-stu-id="633e4-105">Win32\_WMISetting class</span></span>

<span data-ttu-id="633e4-106">A [classe WMI](../wmisdk/retrieving-a-class.md) singleton do **Win32 \_ WMISetting** contém os parâmetros operacionais para o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-106">The **Win32\_WMISetting** singleton [WMI class](../wmisdk/retrieving-a-class.md) contains the operational parameters for the WMI service.</span></span> <span data-ttu-id="633e4-107">Essa classe pode ter apenas uma instância, que sempre existe para cada sistema Windows e não pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="633e4-107">This class can only have one instance, which always exists for each Windows system and cannot be deleted.</span></span> <span data-ttu-id="633e4-108">Não é possível criar instâncias adicionais.</span><span class="sxs-lookup"><span data-stu-id="633e4-108">Additional instances cannot be created.</span></span>

<span data-ttu-id="633e4-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="633e4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="633e4-110">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="633e4-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="633e4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="633e4-111">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a><span data-ttu-id="633e4-112">Membros</span><span class="sxs-lookup"><span data-stu-id="633e4-112">Members</span></span>

<span data-ttu-id="633e4-113">A classe **Win32 \_ WMISetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="633e4-113">The **Win32\_WMISetting** class has these types of members:</span></span>

-   [<span data-ttu-id="633e4-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="633e4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="633e4-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="633e4-115">Properties</span></span>

<span data-ttu-id="633e4-116">A classe **Win32 \_ WMISetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="633e4-116">The **Win32\_WMISetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="633e4-117">**ASPScriptDefaultNamespace**</span><span class="sxs-lookup"><span data-stu-id="633e4-117">**ASPScriptDefaultNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-120">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| padrão namespace")</span><span class="sxs-lookup"><span data-stu-id="633e4-120">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Default Namespace")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-121">Namespace de script padrão.</span><span class="sxs-lookup"><span data-stu-id="633e4-121">Default script namespace.</span></span> <span data-ttu-id="633e4-122">Essa propriedade contém o namespace usado por chamadas da API de script para WMI se nenhum for especificado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="633e4-122">This property contains the namespace used by calls from the Scripting API for WMI if none is specified by the caller.</span></span>

<span data-ttu-id="633e4-123">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-123">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-124">**HKEY \_ \_** \\  \\ Namespace padrão do software do computador local **Microsoft** \\ **WBEM** \\ **scripting \|**    </span><span class="sxs-lookup"><span data-stu-id="633e4-124">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **scripting\|Default Namespace**</span></span>

<span data-ttu-id="633e4-125">Exemplo: raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="633e4-125">Example: root\\cimv2</span></span>

<span data-ttu-id="633e4-126">Para obter um exemplo de script que usa essa propriedade, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="633e4-126">For an example script that uses this property, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-127">**ASPScriptEnabled**</span><span class="sxs-lookup"><span data-stu-id="633e4-127">**ASPScriptEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="633e4-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-130">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| enable for ASP")</span><span class="sxs-lookup"><span data-stu-id="633e4-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Enable for ASP")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-131">Se **for true**, o script WMI poderá ser usado em páginas de Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="633e4-131">If **True**, WMI scripting can be used on Active Server Pages (ASP).</span></span> <span data-ttu-id="633e4-132">Essa propriedade é válida em sistemas que executam apenas versões sem suporte do Windows.</span><span class="sxs-lookup"><span data-stu-id="633e4-132">This property is valid on systems running unsupported versions of Windows only.</span></span> <span data-ttu-id="633e4-133">Para sistemas Windows com suporte, o script WMI sempre é permitido no ASP.</span><span class="sxs-lookup"><span data-stu-id="633e4-133">For supported Windows systems, WMI scripting is always allowed on ASP.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-134">**AutorecoverMofs**</span><span class="sxs-lookup"><span data-stu-id="633e4-134">**AutorecoverMofs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-135">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="633e4-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-137">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Recover MOFs")</span><span class="sxs-lookup"><span data-stu-id="633e4-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Autorecover MOFs")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-138">Lista de nomes de arquivos MOF totalmente qualificados usados para inicializar ou recuperar o repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-138">List of fully qualified MOF file names used to initialize or recover the WMI repository.</span></span> <span data-ttu-id="633e4-139">A lista determina a ordem na qual os arquivos MOF são compilados.</span><span class="sxs-lookup"><span data-stu-id="633e4-139">The list determines the order in which MOF files are compiled.</span></span>

<span data-ttu-id="633e4-140">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-140">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-141">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| AutoRecuperação MOFs**    </span><span class="sxs-lookup"><span data-stu-id="633e4-141">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Autorecover MOFs**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-142">**AutoStartWin9X**</span><span class="sxs-lookup"><span data-stu-id="633e4-142">**AutoStartWin9X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-145">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")</span><span class="sxs-lookup"><span data-stu-id="633e4-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|AutostartWin9X")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-146">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="633e4-146">Not supported.</span></span>

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

<span data-ttu-id="633e4-147">**Não iniciar** (0)</span><span class="sxs-lookup"><span data-stu-id="633e4-147">**Don't start** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

<span data-ttu-id="633e4-148">**Início automática** (1)</span><span class="sxs-lookup"><span data-stu-id="633e4-148">**Autostart** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

<span data-ttu-id="633e4-149">**Iniciar na reinicialização** (2)</span><span class="sxs-lookup"><span data-stu-id="633e4-149">**Start on reboot** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="633e4-150">**BackupInterval que**</span><span class="sxs-lookup"><span data-stu-id="633e4-150">**BackupInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-153">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ limite do intervalo de backup do Microsoft \\ \\ WBEM \\ \\ CIMOM software Win32Registry \| "), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="633e4-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-154">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="633e4-154">Not supported.</span></span> <span data-ttu-id="633e4-155">Em vez disso, faça backup do repositório WMI manualmente.</span><span class="sxs-lookup"><span data-stu-id="633e4-155">Instead, backup the WMI repository manually.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-156">**BackupLastTime**</span><span class="sxs-lookup"><span data-stu-id="633e4-156">**BackupLastTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-157">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="633e4-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-159">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| time Functions \| GetTimeZoneInformation")</span><span class="sxs-lookup"><span data-stu-id="633e4-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Functions\|GetTimeZoneInformation")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-160">Data e hora em que o último backup foi executado.</span><span class="sxs-lookup"><span data-stu-id="633e4-160">Date and time the last backup was performed.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-161">**BuildVersion**</span><span class="sxs-lookup"><span data-stu-id="633e4-161">**BuildVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-164">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Build")</span><span class="sxs-lookup"><span data-stu-id="633e4-164">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Build")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-165">Informações de versão para o serviço WMI atualmente instalado.</span><span class="sxs-lookup"><span data-stu-id="633e4-165">Version information for the currently installed WMI service.</span></span>

<span data-ttu-id="633e4-166">Período de tempo decorrido entre os backups do banco de dados WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-166">Length of time that elapses between backups of the WMI database.</span></span>

<span data-ttu-id="633e4-167">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-167">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-168">**HKEY \_ Build do \_ computador local** \\ **software** \\ **Microsoft** \\ **WBEM \|**</span><span class="sxs-lookup"><span data-stu-id="633e4-168">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Build**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-169">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="633e4-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-172">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="633e4-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="633e4-173">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="633e4-173">Short textual description of the current object.</span></span>

<span data-ttu-id="633e4-174">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="633e4-174">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="633e4-175">**DatabaseDirectory**</span><span class="sxs-lookup"><span data-stu-id="633e4-175">**DatabaseDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-178">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório de \\ \\ repositório do Microsoft \\ \\ WBEM \\ \\ CIMOM software Win32Registry \| ")</span><span class="sxs-lookup"><span data-stu-id="633e4-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Repository Directory")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-179">Caminho do diretório que contém o repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-179">Directory path that contains the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-180">**DatabaseMaxSize**</span><span class="sxs-lookup"><span data-stu-id="633e4-180">**DatabaseMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-181">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-183">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB size"), [**Units**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="633e4-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-184">Tamanho máximo do repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-184">Maximum size of the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-185">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="633e4-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="633e4-188">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="633e4-188">Textual description of the current object.</span></span>

<span data-ttu-id="633e4-189">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="633e4-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="633e4-190">**EnableAnonWin9xConnections**</span><span class="sxs-lookup"><span data-stu-id="633e4-190">**EnableAnonWin9xConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-191">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="633e4-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-193">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")</span><span class="sxs-lookup"><span data-stu-id="633e4-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableAnonConnections")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-194">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="633e4-194">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-195">**EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="633e4-195">**EnableEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="633e4-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-197">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-198">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")</span><span class="sxs-lookup"><span data-stu-id="633e4-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableEvents")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-199">Se **for true**, o subsistema de eventos do WMI deverá ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="633e4-199">If **True**, the WMI event subsystem should be enabled.</span></span>

<span data-ttu-id="633e4-200">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-200">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-201">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="633e4-201">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|EnableEvents**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-202">**EnableStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="633e4-202">**EnableStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-203">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="633e4-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-204">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-204">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-205">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")</span><span class="sxs-lookup"><span data-stu-id="633e4-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableStartupHeapPreallocation")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-206">Se **for true**, o WMI criará um heap pré-alocado com o tamanho do valor **LASTSTARTUPHEAPPREALLOCATION** quando o WMI for inicializado.</span><span class="sxs-lookup"><span data-stu-id="633e4-206">If **True**, WMI creates a pre-allocated heap with the size of the **LastStartupHeapPreallocation** value when WMI is initialized.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-207">**HighThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="633e4-207">**HighThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-209">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-210">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| alto Threshold nos objetos cliente"), [**unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")</span><span class="sxs-lookup"><span data-stu-id="633e4-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-211">Taxa máxima em que os objetos criados pelo provedor podem ser entregues aos clientes.</span><span class="sxs-lookup"><span data-stu-id="633e4-211">Maximum rate at which provider-created objects can be delivered to clients.</span></span> <span data-ttu-id="633e4-212">Para acomodar diferenciais de velocidade entre provedores e clientes, o WMI mantém objetos em filas antes de entregá-los aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="633e4-212">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="633e4-213">Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponda ao provedor.</span><span class="sxs-lookup"><span data-stu-id="633e4-213">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="633e4-214">Se a memória mantida por objetos não coletados atingir **LowThresholdOnObjects**, o WMI reduzirá a adição de novos objetos à fila.</span><span class="sxs-lookup"><span data-stu-id="633e4-214">If the memory held by uncollected objects reaches **LowThresholdOnObjects**, then WMI slows down the addition of new objects into the queue.</span></span> <span data-ttu-id="633e4-215">Se os eventos não coletados continuarem a ser acumulados e a espera máxima de entrega de eventos em **MaxWaitOnClientObjects** for atingida enquanto a memória usada estiver no valor em **HIGHTHRESHOLDONCLIENTOBJECTS**, o WMI não aceitará mais objetos de provedores e retornará o **WBEM \_ e a \_ \_ \_ memória insuficiente** para os clientes.</span><span class="sxs-lookup"><span data-stu-id="633e4-215">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnClientObjects** is reached while the memory used is at the value in **HighThresholdOnClientObjects**, then WMI accepts no more objects from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-216">**HighThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="633e4-216">**HighThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-217">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-218">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-218">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-219">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ de software Microsoft \\ \\ WBEM \\ \\ CIMOM \| limite alto nos eventos"), [**unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")</span><span class="sxs-lookup"><span data-stu-id="633e4-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-220">Taxa máxima na qual os eventos devem ser entregues aos clientes.</span><span class="sxs-lookup"><span data-stu-id="633e4-220">Maximum rate at which events are to be delivered to clients.</span></span> <span data-ttu-id="633e4-221">Para acomodar diferenciais de velocidade entre provedores e clientes, os eventos de filas do WMI antes de entregá-los aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="633e4-221">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="633e4-222">Para obter mais eficiência, os consumidores devem coletar os eventos em um ritmo que corresponda ao provedor.</span><span class="sxs-lookup"><span data-stu-id="633e4-222">For more efficiency, consumers must collect the events at a pace that matches the provider.</span></span> <span data-ttu-id="633e4-223">Se a memória mantida por eventos não coletados atingir **LowThresholdOnObjects**, o WMI reduzirá a adição de novos eventos na fila.</span><span class="sxs-lookup"><span data-stu-id="633e4-223">If the memory held by uncollected events reaches **LowThresholdOnObjects**, then WMI slows down the addition of new events into the queue.</span></span> <span data-ttu-id="633e4-224">Se os eventos não coletados continuarem a ser acumulados e a espera máxima de entrega de eventos em **MaxWaitOnEvents** for atingida enquanto a memória usada estiver no valor em **HighThresholdOnEvents**, o WMI não aceitará mais eventos de provedores e retornará o **WBEM \_ e a \_ \_ \_ memória insuficiente** para os clientes.</span><span class="sxs-lookup"><span data-stu-id="633e4-224">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnEvents** is reached while the memory used is at the value in **HighThresholdOnEvents**, WMI accepts no more events from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

> [!Note]  
> <span data-ttu-id="633e4-225">A limitação só é feita para consumidores de eventos permanentes, portanto, os consumidores temporários não devem esperar a limitação quando os eventos são submetidos a backup na fila de eventos internos do WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-225">Throttling is only done for Permanent Event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="633e4-226">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-226">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-227">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| limite alto nos objetos cliente (B)**    </span><span class="sxs-lookup"><span data-stu-id="633e4-227">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-228">**InstallationDirectory**</span><span class="sxs-lookup"><span data-stu-id="633e4-228">**InstallationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-231">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório de \\ \\ instalação do Microsoft WBEM software Win32Registry \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="633e4-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Installation Directory")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-232">Caminho do diretório em que o software WMI foi instalado.</span><span class="sxs-lookup"><span data-stu-id="633e4-232">Directory path where the WMI software has been installed.</span></span> <span data-ttu-id="633e4-233">O local padrão é \\ System32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="633e4-233">The default location is \\System32\\Wbem.</span></span>

<span data-ttu-id="633e4-234">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-234">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-235">**HKEY \_ \_** Diretório de \\  \\ **instalação do software Microsoft** \\ **WBEM \|** do computador local</span><span class="sxs-lookup"><span data-stu-id="633e4-235">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Installation Directory**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-236">**LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="633e4-236">**LastStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-237">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-239">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="633e4-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-240">Tamanho do heap pré-alocado criado pelo WMI durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="633e4-240">Size of the pre-allocated heap created by WMI during initialization.</span></span>

<span data-ttu-id="633e4-241">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-241">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-242">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="633e4-242">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|LastStartupHeapPreallocation**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-243">**LoggingDirectory**</span><span class="sxs-lookup"><span data-stu-id="633e4-243">**LoggingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-245">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-246">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório de \\ \\ log do Microsoft \\ \\ WBEM \\ \\ CIMOM software Win32Registry \| ")</span><span class="sxs-lookup"><span data-stu-id="633e4-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging Directory")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-247">Caminho do diretório que contém o local dos arquivos de log do sistema WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-247">Directory path that contains the location of the WMI system log files.</span></span>

<span data-ttu-id="633e4-248">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-248">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-249">**HKEY \_ \_** Diretório de log do \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| do** software de computador local</span><span class="sxs-lookup"><span data-stu-id="633e4-249">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging Directory**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-250">**LoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="633e4-250">**LoggingLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-251">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-252">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-252">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-253">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| log")</span><span class="sxs-lookup"><span data-stu-id="633e4-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-254">Habilitação do log de eventos e o nível de detalhamento do log usado.</span><span class="sxs-lookup"><span data-stu-id="633e4-254">Enabling of event logging and the verbosity level of logging used.</span></span>

<span data-ttu-id="633e4-255">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-255">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-256">**HKEY \_ \_** Registro em \\  \\ **log do Microsoft** \\ **WBEM \| CIMOM \|** no software da máquina local</span><span class="sxs-lookup"><span data-stu-id="633e4-256">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging**</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="633e4-257">**Desativado** (0)</span><span class="sxs-lookup"><span data-stu-id="633e4-257">**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

<span data-ttu-id="633e4-258">**Log de erros** (1)</span><span class="sxs-lookup"><span data-stu-id="633e4-258">**Error logging** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

<span data-ttu-id="633e4-259">**Log de erros detalhado** (2)</span><span class="sxs-lookup"><span data-stu-id="633e4-259">**Verbose Error logging** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="633e4-260">**LowThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="633e4-260">**LowThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-261">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-262">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-263">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ de software Microsoft \\ \\ WBEM \\ \\ CIMOM \| limite baixo em objetos de cliente"), [**unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")</span><span class="sxs-lookup"><span data-stu-id="633e4-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-264">Taxa na qual o WMI começa a reduzir a criação de novos objetos criados para clientes.</span><span class="sxs-lookup"><span data-stu-id="633e4-264">Rate at which WMI starts to slow the creation of new objects created for clients.</span></span> <span data-ttu-id="633e4-265">Para acomodar diferenciais de velocidade entre provedores e clientes, o WMI mantém objetos em filas antes de entregá-los aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="633e4-265">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="633e4-266">Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponda ao provedor.</span><span class="sxs-lookup"><span data-stu-id="633e4-266">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="633e4-267">Se a taxa de solicitações de objetos atingir **LowThresholdOnClientObjects**, o WMI reduzirá gradualmente a criação de novos objetos para corresponder à taxa de uso do cliente.</span><span class="sxs-lookup"><span data-stu-id="633e4-267">If the rate of requests for objects reaches **LowThresholdOnClientObjects**, then WMI gradually slows down the creation of new objects to match the client's rate of use.</span></span> <span data-ttu-id="633e4-268">Essa lentidão começa quando a taxa na qual os objetos estão sendo criados excede o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="633e4-268">This slowdown starts when the rate at which objects are being created exceeds the value of this property.</span></span> <span data-ttu-id="633e4-269">Consulte **HighThresholdOnClientObjects**.</span><span class="sxs-lookup"><span data-stu-id="633e4-269">See **HighThresholdOnClientObjects**.</span></span>

<span data-ttu-id="633e4-270">Essa propriedade reflete o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-270">This property reflects the registry value.</span></span>

<span data-ttu-id="633e4-271">**Chave \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| limite alto nos objetos cliente (B)**    </span><span class="sxs-lookup"><span data-stu-id="633e4-271">**KEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-272">**LowThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="633e4-272">**LowThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-273">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-274">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-274">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-275">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ de software Microsoft \\ \\ WBEM \\ \\ CIMOM \| limite baixo nos eventos"), [**unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")</span><span class="sxs-lookup"><span data-stu-id="633e4-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-276">Taxa na qual o WMI começa a reduzir a entrega de novos eventos.</span><span class="sxs-lookup"><span data-stu-id="633e4-276">Rate at which WMI starts to slow the delivery of new events.</span></span> <span data-ttu-id="633e4-277">Para acomodar diferenciais de velocidade entre provedores e clientes, os eventos de filas do WMI antes de entregá-los aos consumidores.</span><span class="sxs-lookup"><span data-stu-id="633e4-277">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="633e4-278">Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponda ao provedor.</span><span class="sxs-lookup"><span data-stu-id="633e4-278">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="633e4-279">Se a fila ficar fora de controle, as restrições de WMI — ficarão mais lentas — a entrega de eventos gradualmente para alinhar com a taxa do cliente.</span><span class="sxs-lookup"><span data-stu-id="633e4-279">If the queue grows out of control, WMI throttles—slows down—the delivery of events gradually to align with the client rate.</span></span> <span data-ttu-id="633e4-280">Essa lentidão começa quando a taxa na qual os eventos são gerados excede o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="633e4-280">This slowdown starts when the rate at which events are generated exceeds the value of this property.</span></span> <span data-ttu-id="633e4-281">Consulte **HighThresholdOnEvents**.</span><span class="sxs-lookup"><span data-stu-id="633e4-281">See **HighThresholdOnEvents**.</span></span>

> [!Note]  
> <span data-ttu-id="633e4-282">A limitação só é feita para consumidores de eventos permanentes, portanto, os consumidores temporários não devem esperar a limitação quando os eventos são submetidos a backup na fila de eventos internos do WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-282">Throttling is only done for permanent event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="633e4-283">Essa propriedade reflete o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-283">This property reflects the registry value.</span></span>

<span data-ttu-id="633e4-284">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| limite alto nos objetos cliente {B}**    </span><span class="sxs-lookup"><span data-stu-id="633e4-284">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects {B}**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-285">**MaxLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="633e4-285">**MaxLogFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-286">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-287">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-288">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| tamanho máximo do arquivo de log"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="633e4-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Log File Max Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-289">Tamanho máximo dos arquivos de log produzidos pelo serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-289">Maximum size of the log files produced by the WMI service.</span></span>

<span data-ttu-id="633e4-290">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-290">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-291">**HKEY \_ \_** \\  \\  \\ **\| \| Tamanho máximo do arquivo de log do Microsoft WBEM CIMOM** software do computador local</span><span class="sxs-lookup"><span data-stu-id="633e4-291">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Log File Max Size**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-292">**MaxWaitOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="633e4-292">**MaxWaitOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-293">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-294">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-294">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-295">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max em eventos"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="633e4-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-296">Quantidade de tempo que um objeto recém-criado espera para ser usado pelo cliente antes de ser descartado e um valor de erro é retornado.</span><span class="sxs-lookup"><span data-stu-id="633e4-296">Amount of time a newly created object waits to be used by the client before it is discarded and an error value is returned.</span></span> <span data-ttu-id="633e4-297">Essa propriedade interage com as propriedades **LowThresholdOnClientObjects** e **HighThresholdOnClientObjects** para limitação — lentidão – a entrega de objetos aos consumidores quando o consumidor está recebendo os objetos muito lentamente.</span><span class="sxs-lookup"><span data-stu-id="633e4-297">This property interacts with the **LowThresholdOnClientObjects** and **HighThresholdOnClientObjects** properties to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

</dd> <dt>

<span data-ttu-id="633e4-298">**MaxWaitOnEvents**</span><span class="sxs-lookup"><span data-stu-id="633e4-298">**MaxWaitOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-299">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="633e4-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-300">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="633e4-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="633e4-301">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max em eventos"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="633e4-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-302">Quantidade de tempo para o qual um evento enviado a um cliente é colocado na fila antes de ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="633e4-302">Amount of time for which an event sent to a client is queued before being discarded.</span></span> <span data-ttu-id="633e4-303">Essa propriedade interacts0 com **LowThresholdOnEvents** e **HighThresholdOnEvents** para a limitação — retardamento — a entrega de objetos aos consumidores quando o consumidor está recebendo os objetos muito lentamente.</span><span class="sxs-lookup"><span data-stu-id="633e4-303">This property interacts0 with **LowThresholdOnEvents** and **HighThresholdOnEvents** to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

<span data-ttu-id="633e4-304">Essa propriedade reflete o valor do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-304">This property reflects the registry value.</span></span>

<span data-ttu-id="633e4-305">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| máx. de eventos (MS)**    </span><span class="sxs-lookup"><span data-stu-id="633e4-305">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Max Wait On Events (ms)**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-306">**MofSelfInstallDirectory**</span><span class="sxs-lookup"><span data-stu-id="633e4-306">**MofSelfInstallDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-309">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory")</span><span class="sxs-lookup"><span data-stu-id="633e4-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|MOF Self-Install Directory")</span></span>
</dt> </dl>

<span data-ttu-id="633e4-310">Caminho do diretório para aplicativos que instalam arquivos MOF no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-310">Directory path for applications that install MOF files to the WMI repository.</span></span> <span data-ttu-id="633e4-311">O WMI compila automaticamente todos os arquivos MOF colocados nesse diretório e, dependendo de seu sucesso, move o MOF para um subdiretório rotulado bom ou ruim.</span><span class="sxs-lookup"><span data-stu-id="633e4-311">WMI automatically compiles any MOF files placed in this directory and, depending on its success, moves the MOF to a subdirectory labeled good or bad.</span></span> <span data-ttu-id="633e4-312">Se o \# comando [pragma autoautorecover](../wmisdk/pragma-autorecover.md) for incluído, o nome de arquivo totalmente qualificado será adicionado à lista **AUTORECOVERMOFS** usada quando o WMI estiver inicializando ou recuperando o repositório.</span><span class="sxs-lookup"><span data-stu-id="633e4-312">If the \# [pragma autorecover](../wmisdk/pragma-autorecover.md) command is included, the fully qualified file name is added to the **AutorecoverMofs** list used when WMI is initializing or recovering the repository.</span></span> <span data-ttu-id="633e4-313">A lista determina a ordem na qual MOFs são compilados.</span><span class="sxs-lookup"><span data-stu-id="633e4-313">The list determines the order in which MOFs are compiled.</span></span>

<span data-ttu-id="633e4-314">Essa propriedade reflete o valor na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="633e4-314">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="633e4-315">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = diretório de instalação**</span><span class="sxs-lookup"><span data-stu-id="633e4-315">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|MOF Self=Install Directory**</span></span>

</dd> <dt>

<span data-ttu-id="633e4-316">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="633e4-316">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633e4-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="633e4-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="633e4-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="633e4-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633e4-319">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="633e4-319">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="633e4-320">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="633e4-320">Identifier by which the current object is known.</span></span>

<span data-ttu-id="633e4-321">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="633e4-321">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="633e4-322">Comentários</span><span class="sxs-lookup"><span data-stu-id="633e4-322">Remarks</span></span>

<span data-ttu-id="633e4-323">A classe **Win32 \_ WMISetting** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="633e4-323">The **Win32\_WMISetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span> <span data-ttu-id="633e4-324">Somente uma instância dessa classe pode existir em um computador.</span><span class="sxs-lookup"><span data-stu-id="633e4-324">Only one instance of this class can exist on a computer.</span></span>

<span data-ttu-id="633e4-325">Saber como o WMI é configurado em um computador pode ser muito útil quando você está Depurando scripts ou Solucionando problemas com o próprio serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-325">Knowing how WMI is configured on a computer can be very useful when you are debugging scripts or troubleshooting problems with the WMI service itself.</span></span> <span data-ttu-id="633e4-326">Por exemplo, muitos scripts WMI são escritos sob a suposição de que raiz \\ cimv2 é o namespace padrão no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="633e4-326">For example, many WMI scripts are written under the assumption that root\\cimv2 is the default namespace on the target computer.</span></span> <span data-ttu-id="633e4-327">Como resultado, os criadores de script que precisam acessar uma classe em "raiz \\ CIMv2" geralmente não incluem o namespace no moniker GetObject, conforme mostrado no exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="633e4-327">As a result, script writers who need to access a class in "Root\\CIMv2" often fail to include the namespace in the GetObject moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

<span data-ttu-id="633e4-328">Se raiz \\ cimv2 não for o namespace padrão no computador de destino, esse script falhará.</span><span class="sxs-lookup"><span data-stu-id="633e4-328">If root\\cimv2 is not the default namespace on the target computer, this script will fail.</span></span> <span data-ttu-id="633e4-329">Para evitar que isso aconteça, a raiz do namespace \\ cimv2 deve ser incluída no moniker, conforme mostrado no exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="633e4-329">To prevent this from happening, the namespace root\\cimv2 must be included in the moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

<span data-ttu-id="633e4-330">Se o namespace padrão no computador de destino for diferente do namespace assumido por um script, o script falhará.</span><span class="sxs-lookup"><span data-stu-id="633e4-330">If the default namespace on the target computer is different from the namespace assumed by a script, the script will fail.</span></span> <span data-ttu-id="633e4-331">Além disso, o usuário receberá a mensagem de erro um pouco enganosa "classe inválida".</span><span class="sxs-lookup"><span data-stu-id="633e4-331">On top of that, the user will be presented with the somewhat misleading error message "Invalid class."</span></span> <span data-ttu-id="633e4-332">Na verdade, a falha não é porque a classe é inválida, mas porque a classe não pode ser encontrada no namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="633e4-332">In truth, the failure is not because the class is invalid but because the class cannot be found in the default namespace.</span></span> <span data-ttu-id="633e4-333">Esse é um problema difícil de solucionar problemas, pois é provável que você investigue possíveis problemas com a classe em vez de problemas com o namespace que foi (ou, neste caso, não foi) especificado.</span><span class="sxs-lookup"><span data-stu-id="633e4-333">This is a difficult problem to troubleshoot, because you are likely to investigate possible problems with the class rather than problems with the namespace that was (or, in this case, was not) specified.</span></span>

<span data-ttu-id="633e4-334">Você pode usar a **classe \_ WMISetting do Win32** para determinar como o WMI foi configurado em um computador.</span><span class="sxs-lookup"><span data-stu-id="633e4-334">You can use the **Win32\_WMISetting** class to determine how WMI has been configured on a computer.</span></span> <span data-ttu-id="633e4-335">Os detalhes de configuração, como o namespace padrão ou o número de Build do WMI, podem ser úteis para solucionar problemas de script.</span><span class="sxs-lookup"><span data-stu-id="633e4-335">Configuration details such as the default namespace or the WMI build number can be useful in troubleshooting script problems.</span></span> <span data-ttu-id="633e4-336">Essas configurações também fornecem informações administrativas importantes, como, ou até mesmo, se os erros do WMI são registrados em um computador e quais provedores de WMI serão automaticamente recarregados se você precisar recriar o repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-336">These settings also provide important administrative information such as how, or even whether, WMI errors are logged on a computer and which WMI providers will automatically be reloaded if you need to rebuild the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="633e4-337">Exemplos</span><span class="sxs-lookup"><span data-stu-id="633e4-337">Examples</span></span>

<span data-ttu-id="633e4-338">O exemplo de código do VBScript [Modificar configurações do WMI](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) na galeria do TechNet usa a classe **Win32 \_ WMISetting** para configurar o intervalo de backup e o nível de log do WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-338">The [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to configure the WMI backup interval and logging level.</span></span>

<span data-ttu-id="633e4-339">A [lista do exemplo de código VBScript do namespace padrão](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) na galeria do TechNet usa a classe **Win32 \_ WMISetting** para recuperar e exibir a configuração atual do WMI "namespace padrão para script".</span><span class="sxs-lookup"><span data-stu-id="633e4-339">The [List the Default Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to retrieve and display the current WMI "Default namespace for scripting" setting.</span></span>

<span data-ttu-id="633e4-340">O exemplo de código de [Modificar o namespace padrão do WMI](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) do VBScript na galeria do TechNet usa a propriedade **ASPScriptDefaultNamespace** para definir a configuração "namespace padrão para script" do WMI como "raiz \\ cimv2".</span><span class="sxs-lookup"><span data-stu-id="633e4-340">The [Modify the Default WMI Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript code example on the TechNet Gallery uses the **ASPScriptDefaultNamespace** property to set the WMI "Default namespace for scripting" setting to "root\\cimv2".</span></span>

<span data-ttu-id="633e4-341">A [lista todas as configurações do WMI](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) exemplo de código VBSCript usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações do WMI configuradas em um computador.</span><span class="sxs-lookup"><span data-stu-id="633e4-341">The [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="633e4-342">O exemplo de código JavaScript [listar informações de configuração do WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações do WMI configuradas em um computador.</span><span class="sxs-lookup"><span data-stu-id="633e4-342">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="633e4-343">A [lista de informações de configuração do WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) exemplo de código Python usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações de WMI configuradas em um computador.</span><span class="sxs-lookup"><span data-stu-id="633e4-343">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) Python code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="633e4-344">O exemplo de código do objeto de [informações de configuração do WMI de lista](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) REXX usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações de WMI configuradas em um computador.</span><span class="sxs-lookup"><span data-stu-id="633e4-344">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="633e4-345">O exemplo de código VBScript a seguir mostra como obter a versão do WMI em execução no computador local.</span><span class="sxs-lookup"><span data-stu-id="633e4-345">The following VBScript code example shows how to obtain the version of WMI running on the local computer.</span></span> <span data-ttu-id="633e4-346">O "Win32 \_ WMISetting = @" indica a única instância da classe.</span><span class="sxs-lookup"><span data-stu-id="633e4-346">The "Win32\_WMISetting=@" indicates the single instance of the class.</span></span> <span data-ttu-id="633e4-347">Para obter mais informações, consulte versões do WMI.</span><span class="sxs-lookup"><span data-stu-id="633e4-347">For more information, see WMI versions.</span></span>


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a><span data-ttu-id="633e4-348">Requisitos</span><span class="sxs-lookup"><span data-stu-id="633e4-348">Requirements</span></span>



| <span data-ttu-id="633e4-349">Requisito</span><span class="sxs-lookup"><span data-stu-id="633e4-349">Requirement</span></span> | <span data-ttu-id="633e4-350">Valor</span><span class="sxs-lookup"><span data-stu-id="633e4-350">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="633e4-351">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="633e4-351">Minimum supported client</span></span><br/> | <span data-ttu-id="633e4-352">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="633e4-352">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="633e4-353">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="633e4-353">Minimum supported server</span></span><br/> | <span data-ttu-id="633e4-354">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="633e4-354">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="633e4-355">Namespace</span><span class="sxs-lookup"><span data-stu-id="633e4-355">Namespace</span></span><br/>                | <span data-ttu-id="633e4-356">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="633e4-356">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="633e4-357">MOF</span><span class="sxs-lookup"><span data-stu-id="633e4-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="633e4-358"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="633e4-358"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="633e4-359">DLL</span><span class="sxs-lookup"><span data-stu-id="633e4-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="633e4-360"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="633e4-360"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="633e4-361">Confira também</span><span class="sxs-lookup"><span data-stu-id="633e4-361">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633e4-362">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="633e4-362">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="633e4-363">Classes de gerenciamento de serviço WMI</span><span class="sxs-lookup"><span data-stu-id="633e4-363">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
