---
description: A \_ classe WMI BootConfiguration do Win32 representa a configuração de inicialização de um sistema de computador executando o Windows.
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Classe Win32_BootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756433"
---
# <a name="win32_bootconfiguration-class"></a><span data-ttu-id="e55c4-103">\_Classe Win32 BootConfiguration</span><span class="sxs-lookup"><span data-stu-id="e55c4-103">Win32\_BootConfiguration class</span></span>

<span data-ttu-id="e55c4-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BootConfiguration do Win32** representa a configuração de inicialização de um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="e55c4-104">The **Win32\_BootConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the boot configuration of a computer system running Windows.</span></span>

<span data-ttu-id="e55c4-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e55c4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e55c4-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e55c4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e55c4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e55c4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a><span data-ttu-id="e55c4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e55c4-108">Members</span></span>

<span data-ttu-id="e55c4-109">A classe **Win32 \_ BootConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e55c4-109">The **Win32\_BootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="e55c4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e55c4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e55c4-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e55c4-111">Properties</span></span>

<span data-ttu-id="e55c4-112">A classe **Win32 \_ BootConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e55c4-112">The **Win32\_BootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e55c4-113">**BootDirectory**</span><span class="sxs-lookup"><span data-stu-id="e55c4-113">**BootDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-116">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| process and thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")</span><span class="sxs-lookup"><span data-stu-id="e55c4-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-117">Caminho para os arquivos do sistema necessários para inicializar o sistema.</span><span class="sxs-lookup"><span data-stu-id="e55c4-117">Path to the system files required for booting the system.</span></span>

<span data-ttu-id="e55c4-118">Exemplo: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="e55c4-118">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="e55c4-119">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e55c4-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-122">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e55c4-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-123">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="e55c4-123">Short textual description of the current object.</span></span>

<span data-ttu-id="e55c4-124">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e55c4-124">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e55c4-125">**ConfigurationPath**</span><span class="sxs-lookup"><span data-stu-id="e55c4-125">**ConfigurationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| process and thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")</span><span class="sxs-lookup"><span data-stu-id="e55c4-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-129">Caminho para os arquivos de configuração.</span><span class="sxs-lookup"><span data-stu-id="e55c4-129">Path to the configuration files.</span></span> <span data-ttu-id="e55c4-130">Esse valor pode ser semelhante ao valor na propriedade **BootDirectory** .</span><span class="sxs-lookup"><span data-stu-id="e55c4-130">This value may be similar to the value in the **BootDirectory** property.</span></span>

</dd> <dt>

<span data-ttu-id="e55c4-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e55c4-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-134">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="e55c4-134">Textual description of the current object.</span></span>

<span data-ttu-id="e55c4-135">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e55c4-135">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e55c4-136">**LastDrive**</span><span class="sxs-lookup"><span data-stu-id="e55c4-136">**LastDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="e55c4-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-140">Última letra da unidade à qual uma unidade física é atribuída.</span><span class="sxs-lookup"><span data-stu-id="e55c4-140">Last drive letter to which a physical drive is assigned.</span></span>

<span data-ttu-id="e55c4-141">Exemplo: "E:"</span><span class="sxs-lookup"><span data-stu-id="e55c4-141">Example: "E:"</span></span>

</dd> <dt>

<span data-ttu-id="e55c4-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e55c4-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-145">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="e55c4-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-146">Nome da configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e55c4-146">Name of the boot configuration.</span></span> <span data-ttu-id="e55c4-147">É um identificador para a configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e55c4-147">It is an identifier for the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e55c4-148">**ScratchDirectory**</span><span class="sxs-lookup"><span data-stu-id="e55c4-148">**ScratchDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-151">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="e55c4-151">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-152">Diretório em que os arquivos temporários podem residir durante o tempo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e55c4-152">Directory where temporary files can reside during boot time.</span></span>

</dd> <dt>

<span data-ttu-id="e55c4-153">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="e55c4-153">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-156">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e55c4-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-157">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e55c4-157">Identifier by which the current object is known.</span></span>

<span data-ttu-id="e55c4-158">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e55c4-158">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e55c4-159">**TempDirectory**</span><span class="sxs-lookup"><span data-stu-id="e55c4-159">**TempDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e55c4-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e55c4-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e55c4-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e55c4-162">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="e55c4-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="e55c4-163">Diretório onde os arquivos temporários são armazenados.</span><span class="sxs-lookup"><span data-stu-id="e55c4-163">Directory where temporary files are stored.</span></span>

<span data-ttu-id="e55c4-164">Exemplo: "C: \\ Temp"</span><span class="sxs-lookup"><span data-stu-id="e55c4-164">Example: "C:\\TEMP"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e55c4-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="e55c4-165">Remarks</span></span>

<span data-ttu-id="e55c4-166">A classe **Win32 \_ BootConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e55c4-166">The **Win32\_BootConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e55c4-167">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e55c4-167">Examples</span></span>

<span data-ttu-id="e55c4-168">A [lista as propriedades de configuração de inicialização de um computador de](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) exemplo Perl retorna informações de configuração de inicialização para um computador.</span><span class="sxs-lookup"><span data-stu-id="e55c4-168">The [List the Boot Configuration Properties of a Computer](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl sample returns boot configuration information for a computer.</span></span>

<span data-ttu-id="e55c4-169">O exemplo de VBScript a seguir retorna informações de configuração de inicialização para um computador.</span><span class="sxs-lookup"><span data-stu-id="e55c4-169">The following VBScript sample returns boot configuration information for a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



<span data-ttu-id="e55c4-170">O exemplo de código a seguir demonstra o uso da classe WMI **\_ BootConfiguration do Win32** .</span><span class="sxs-lookup"><span data-stu-id="e55c4-170">The following code sample demonstrates the use of the **Win32\_BootConfiguration** WMI class.</span></span>


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



<span data-ttu-id="e55c4-171">O exemplo de código anterior cria a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="e55c4-171">The previous code sample creates the following output:</span></span>

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a><span data-ttu-id="e55c4-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e55c4-172">Requirements</span></span>



| <span data-ttu-id="e55c4-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="e55c4-173">Requirement</span></span> | <span data-ttu-id="e55c4-174">Valor</span><span class="sxs-lookup"><span data-stu-id="e55c4-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e55c4-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e55c4-175">Minimum supported client</span></span><br/> | <span data-ttu-id="e55c4-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e55c4-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e55c4-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e55c4-177">Minimum supported server</span></span><br/> | <span data-ttu-id="e55c4-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e55c4-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e55c4-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="e55c4-179">Namespace</span></span><br/>                | <span data-ttu-id="e55c4-180">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e55c4-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e55c4-181">MOF</span><span class="sxs-lookup"><span data-stu-id="e55c4-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e55c4-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e55c4-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e55c4-183">DLL</span><span class="sxs-lookup"><span data-stu-id="e55c4-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e55c4-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e55c4-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e55c4-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="e55c4-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e55c4-186">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e55c4-186">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="e55c4-187">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e55c4-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

