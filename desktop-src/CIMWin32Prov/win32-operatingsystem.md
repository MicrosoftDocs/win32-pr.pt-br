---
description: Representa um sistema operacional baseado no Windows instalado em um computador.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164147"
---
# <a name="win32_operatingsystem-class"></a><span data-ttu-id="186cc-103">Classe do sistema \_ operacional Win32</span><span class="sxs-lookup"><span data-stu-id="186cc-103">Win32\_OperatingSystem class</span></span>

<span data-ttu-id="186cc-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ OperatingSystem do Win32** representa um sistema operacional baseado no Windows instalado em um computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-104">The **Win32\_OperatingSystem** [WMI class](../wmisdk/retrieving-a-class.md) represents a Windows-based operating system installed on a computer.</span></span>

<span data-ttu-id="186cc-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="186cc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="186cc-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="186cc-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="186cc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="186cc-107">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a><span data-ttu-id="186cc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="186cc-108">Members</span></span>

<span data-ttu-id="186cc-109">A classe de sistema **\_ operacional Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="186cc-109">The **Win32\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="186cc-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="186cc-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="186cc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="186cc-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="186cc-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="186cc-112">Methods</span></span>

<span data-ttu-id="186cc-113">A classe de sistema **\_ operacional Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="186cc-113">The **Win32\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="186cc-114">Método</span><span class="sxs-lookup"><span data-stu-id="186cc-114">Method</span></span>                                                                                     | <span data-ttu-id="186cc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="186cc-115">Description</span></span>                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="186cc-116">**Reboot**</span><span class="sxs-lookup"><span data-stu-id="186cc-116">**Reboot**</span></span>](reboot-method-in-class-win32-operatingsystem.md)                             | <span data-ttu-id="186cc-117">Desliga e reinicia o sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-117">Shuts down and then restarts the computer system.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="186cc-118">**SetDateTime**</span><span class="sxs-lookup"><span data-stu-id="186cc-118">**SetDateTime**</span></span>](setdatetime-method-in-class-win32-operatingsystem.md)                   | <span data-ttu-id="186cc-119">Permite definir a data e a hora do computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-119">Allows the computer date and time to be set.</span></span><br/>                                                                                                                                                                                                                |
| [<span data-ttu-id="186cc-120">**Desligar**</span><span class="sxs-lookup"><span data-stu-id="186cc-120">**Shutdown**</span></span>](shutdown-method-in-class-win32-operatingsystem.md)                         | <span data-ttu-id="186cc-121">Descarrega programas e DLLs no ponto em que é seguro desligar o computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-121">Unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="186cc-122">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="186cc-122">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)               | <span data-ttu-id="186cc-123">Fornece o conjunto completo de opções de desligamento com suporte dos sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="186cc-123">Provides the full set of shutdown options supported by Windows operating systems.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="186cc-124">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="186cc-124">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | <span data-ttu-id="186cc-125">Fornece o mesmo conjunto de opções de desligamento com suporte pelo método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) no sistema **\_ operacional Win32**, mas também permite que você especifique comentários, um motivo para o desligamento ou um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="186cc-125">Provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in **Win32\_OperatingSystem**, but also allows you to specify comments, a reason for shutdown, or a timeout.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="186cc-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="186cc-126">Properties</span></span>

<span data-ttu-id="186cc-127">A classe de sistema **\_ operacional Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="186cc-127">The **Win32\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="186cc-128">**BootDevice**</span><span class="sxs-lookup"><span data-stu-id="186cc-128">**BootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-131">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| informações de mapa de unidade \_ \_ \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="186cc-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-132">Nome da unidade de disco da qual o sistema operacional Windows é iniciado.</span><span class="sxs-lookup"><span data-stu-id="186cc-132">Name of the disk drive from which the Windows operating system starts.</span></span>

<span data-ttu-id="186cc-133">Exemplo: " \\ \\ Device \\ Harddisk0"</span><span class="sxs-lookup"><span data-stu-id="186cc-133">Example: "\\\\Device\\Harddisk0"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-134">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="186cc-134">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-137">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")</span><span class="sxs-lookup"><span data-stu-id="186cc-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwBuildNumber")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-138">Número de Build de um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-138">Build number of an operating system.</span></span> <span data-ttu-id="186cc-139">Ele pode ser usado para obter informações de versão mais precisas do que os números de versão de lançamento do produto.</span><span class="sxs-lookup"><span data-stu-id="186cc-139">It can be used for more precise version information than product release version numbers.</span></span>

<span data-ttu-id="186cc-140">Exemplo: "1381"</span><span class="sxs-lookup"><span data-stu-id="186cc-140">Example: "1381"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-141">**BuildType**</span><span class="sxs-lookup"><span data-stu-id="186cc-141">**BuildType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-144">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| CurrentType")</span><span class="sxs-lookup"><span data-stu-id="186cc-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|CurrentType")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-145">Tipo de compilação usado para um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-145">Type of build used for an operating system.</span></span>

<span data-ttu-id="186cc-146">Exemplos: "" Build de varejo "", "" compilação verificada ""</span><span class="sxs-lookup"><span data-stu-id="186cc-146">Examples: ""retail build"", ""checked build""</span></span>

</dd> <dt>

<span data-ttu-id="186cc-147">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="186cc-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-150">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="186cc-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-151">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="186cc-151">Short description of the object—a one-line string.</span></span> <span data-ttu-id="186cc-152">A cadeia de caracteres inclui a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-152">The string includes the operating system version.</span></span> <span data-ttu-id="186cc-153">Por exemplo, "Microsoft Windows 7 Enterprise".</span><span class="sxs-lookup"><span data-stu-id="186cc-153">For example, "Microsoft Windows 7 Enterprise ".</span></span> <span data-ttu-id="186cc-154">Essa propriedade pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="186cc-154">This property can be localized.</span></span>

<span data-ttu-id="186cc-155">**Windows Vista e Windows 7:** Esta propriedade pode conter caracteres à direita.</span><span class="sxs-lookup"><span data-stu-id="186cc-155">**Windows Vista and Windows 7:** This property may contain trailing characters.</span></span> <span data-ttu-id="186cc-156">Por exemplo, a cadeia de caracteres "Microsoft Windows 7 Enterprise" (espaço à direita incluído) pode ser necessária para recuperar informações usando essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="186cc-156">For example, the string "Microsoft Windows 7 Enterprise " (trailing space included) may be necessary to retrieve information using this property.</span></span>

<span data-ttu-id="186cc-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-158">**Código de**</span><span class="sxs-lookup"><span data-stu-id="186cc-158">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-161">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| localidade \_ IDEFAULTANSICODEPAGE")</span><span class="sxs-lookup"><span data-stu-id="186cc-161">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_IDEFAULTANSICODEPAGE")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-162">Valor da página de código que um sistema operacional usa.</span><span class="sxs-lookup"><span data-stu-id="186cc-162">Code page value an operating system uses.</span></span> <span data-ttu-id="186cc-163">Uma página de código contém uma tabela de caracteres que um sistema operacional usa para converter as cadeias para diferentes idiomas.</span><span class="sxs-lookup"><span data-stu-id="186cc-163">A code page contains a character table that an operating system uses to translate strings for different languages.</span></span> <span data-ttu-id="186cc-164">O American National Standards Institute (ANSI) lista os valores que representam as páginas de código definidas.</span><span class="sxs-lookup"><span data-stu-id="186cc-164">The American National Standards Institute (ANSI) lists values that represent defined code pages.</span></span> <span data-ttu-id="186cc-165">Se um sistema operacional não usar uma página de código ANSI, esse membro será definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="186cc-165">If an operating system does not use an ANSI code page, this member is set to 0 (zero).</span></span> <span data-ttu-id="186cc-166">A cadeia de **código** pode usar, no máximo, seis caracteres para definir o valor da página de código.</span><span class="sxs-lookup"><span data-stu-id="186cc-166">The **CodeSet** string can use a maximum of six characters to define the code page value.</span></span>

<span data-ttu-id="186cc-167">Exemplo: "1255"</span><span class="sxs-lookup"><span data-stu-id="186cc-167">Example: "1255"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-168">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="186cc-168">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-171">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de suporte do idioma nacional win32api \| [](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| \_ ICOUNTRY")</span><span class="sxs-lookup"><span data-stu-id="186cc-171">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ICOUNTRY")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-172">Código para o país/região que um sistema operacional usa.</span><span class="sxs-lookup"><span data-stu-id="186cc-172">Code for the country/region that an operating system uses.</span></span> <span data-ttu-id="186cc-173">Os valores são baseados em prefixos de discagem telefônica internacional — também conhecidos como códigos de país/região da IBM.</span><span class="sxs-lookup"><span data-stu-id="186cc-173">Values are based on international phone dialing prefixes—also referred to as IBM country/region codes.</span></span> <span data-ttu-id="186cc-174">Essa propriedade pode usar um máximo de seis caracteres para definir o valor de código de país/região.</span><span class="sxs-lookup"><span data-stu-id="186cc-174">This property can use a maximum of six characters to define the country/region code value.</span></span>

<span data-ttu-id="186cc-175">Exemplo: "1" (Estados Unidos)</span><span class="sxs-lookup"><span data-stu-id="186cc-175">Example: "1" (United States)</span></span>

</dd> <dt>

<span data-ttu-id="186cc-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="186cc-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-179">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="186cc-179">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="186cc-180">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="186cc-180">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="186cc-181">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="186cc-181">When used with other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="186cc-182">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-182">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-183">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="186cc-183">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-186">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="186cc-186">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="186cc-187">Nome da classe de criação do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="186cc-187">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="186cc-188">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-188">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-189">**CSDVersion**</span><span class="sxs-lookup"><span data-stu-id="186cc-189">**CSDVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-192">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")</span><span class="sxs-lookup"><span data-stu-id="186cc-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**szCSDVersion**")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-193">Cadeia de caracteres terminada em **nulo** que indica as Service Pack mais recentes instaladas em um computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-193">**NULL**-terminated string that indicates the latest service pack installed on a computer.</span></span> <span data-ttu-id="186cc-194">Se nenhum service pack estiver instalado, a cadeia de caracteres será **nula**.</span><span class="sxs-lookup"><span data-stu-id="186cc-194">If no service pack is installed, the string is **NULL**.</span></span>

<span data-ttu-id="186cc-195">Exemplo: "Service Pack 3"</span><span class="sxs-lookup"><span data-stu-id="186cc-195">Example: "Service Pack 3"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-196">**CSName**</span><span class="sxs-lookup"><span data-stu-id="186cc-196">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-199">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="186cc-199">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="186cc-200">Nome do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="186cc-200">Name of the scoping computer system.</span></span>

<span data-ttu-id="186cc-201">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-201">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-202">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="186cc-202">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-203">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="186cc-203">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-205">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="186cc-205">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-206">Número, em minutos, um sistema operacional é deslocado de Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="186cc-206">Number, in minutes, an operating system is offset from Greenwich mean time (GMT).</span></span> <span data-ttu-id="186cc-207">O número é positivo, negativo ou zero.</span><span class="sxs-lookup"><span data-stu-id="186cc-207">The number is positive, negative, or zero.</span></span>

<span data-ttu-id="186cc-208">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-208">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-209">**DataExecutionPrevention \_ 32BitApplications**</span><span class="sxs-lookup"><span data-stu-id="186cc-209">**DataExecutionPrevention\_32BitApplications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-210">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="186cc-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-212">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-213">Quando o recurso de hardware de prevenção de execução de dados estiver disponível, essa propriedade indicará que o recurso está definido para funcionar para aplicativos de 32 bits, se **for verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="186cc-213">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for 32-bit applications if **True**.</span></span> <span data-ttu-id="186cc-214">Em computadores de 64 bits, o recurso de prevenção de execução de dados é configurado no repositório [BCD (dados de configuração da inicialização)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) e as propriedades no sistema **\_ operacional Win32** são definidas de acordo.</span><span class="sxs-lookup"><span data-stu-id="186cc-214">On 64-bit computers, the data execution prevention feature is configured in the [Boot Configuration Data (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-215">**DataExecutionPrevention \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="186cc-215">**DataExecutionPrevention\_Available**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-216">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="186cc-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-218">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-219">A prevenção de execução de dados é um recurso de hardware para evitar ataques de saturação de buffer, interrompendo a execução do código em páginas de memória do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="186cc-219">Data execution prevention is a hardware feature to prevent buffer overrun attacks by stopping the execution of code on data-type memory pages.</span></span> <span data-ttu-id="186cc-220">Se for **true**, esse recurso estará disponível.</span><span class="sxs-lookup"><span data-stu-id="186cc-220">If **True**, then this feature is available.</span></span> <span data-ttu-id="186cc-221">Em computadores de 64 bits, o recurso de prevenção de execução de dados é configurado no repositório BCD e as propriedades no sistema **\_ operacional do Win32** são definidas de acordo.</span><span class="sxs-lookup"><span data-stu-id="186cc-221">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-222">**\_Drivers DataExecutionPrevention**</span><span class="sxs-lookup"><span data-stu-id="186cc-222">**DataExecutionPrevention\_Drivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-223">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="186cc-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-225">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-226">Quando o recurso de hardware de prevenção de execução de dados estiver disponível, essa propriedade indicará que o recurso está definido para funcionar para drivers se **for verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="186cc-226">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for drivers if **True**.</span></span> <span data-ttu-id="186cc-227">Em computadores de 64 bits, o recurso de prevenção de execução de dados é configurado no repositório BCD e as propriedades no sistema **\_ operacional do Win32** são definidas de acordo.</span><span class="sxs-lookup"><span data-stu-id="186cc-227">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-228">**DataExecutionPrevention \_ SupportPolicy**</span><span class="sxs-lookup"><span data-stu-id="186cc-228">**DataExecutionPrevention\_SupportPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-229">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="186cc-229">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-231">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-232">Indica qual configuração de DEP (prevenção de execução de dados) é aplicada.</span><span class="sxs-lookup"><span data-stu-id="186cc-232">Indicates which Data Execution Prevention (DEP) setting is applied.</span></span> <span data-ttu-id="186cc-233">A configuração de DEP especifica a extensão à qual a DEP se aplica a aplicativos de 32 bits no sistema.</span><span class="sxs-lookup"><span data-stu-id="186cc-233">The DEP setting specifies the extent to which DEP applies to 32-bit applications on the system.</span></span> <span data-ttu-id="186cc-234">O DEP sempre é aplicado ao kernel do Windows.</span><span class="sxs-lookup"><span data-stu-id="186cc-234">DEP is always applied to the Windows kernel.</span></span>

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span data-ttu-id="186cc-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Sempre desativado** (0)</span><span class="sxs-lookup"><span data-stu-id="186cc-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-236">A DEP é desativada para todos os aplicativos de 32 bits no computador sem exceções.</span><span class="sxs-lookup"><span data-stu-id="186cc-236">DEP is turned off for all 32-bit applications on the computer with no exceptions.</span></span> <span data-ttu-id="186cc-237">Essa configuração não está disponível para a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="186cc-237">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span data-ttu-id="186cc-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-239">O DEP está habilitado para todos os aplicativos de 32 bits no computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-239">DEP is enabled for all 32-bit applications on the computer.</span></span> <span data-ttu-id="186cc-240">Essa configuração não está disponível para a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="186cc-240">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span data-ttu-id="186cc-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Aceitar** (2)</span><span class="sxs-lookup"><span data-stu-id="186cc-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt In** (2)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-242">O DEP é habilitado para um número limitado de binários, o kernel e todos os serviços baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="186cc-242">DEP is enabled for a limited number of binaries, the kernel, and all Windows-based services.</span></span> <span data-ttu-id="186cc-243">No entanto, ela está desativada por padrão para todos os aplicativos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="186cc-243">However, it is off by default for all 32-bit applications.</span></span> <span data-ttu-id="186cc-244">Um usuário ou administrador deve escolher explicitamente o **Always on** ou a configuração de **recusa** antes que a DEP possa ser aplicada a aplicativos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="186cc-244">A user or administrator must explicitly choose either the **Always On** or the **Opt Out** setting before DEP can be applied to 32-bit applications.</span></span>

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span data-ttu-id="186cc-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Recusar** (3)</span><span class="sxs-lookup"><span data-stu-id="186cc-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Opt Out** (3)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-246">O DEP é habilitado por padrão para todos os aplicativos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="186cc-246">DEP is enabled by default for all 32-bit applications.</span></span> <span data-ttu-id="186cc-247">Um usuário ou administrador pode remover explicitamente o suporte para um aplicativo de 32 bits adicionando o aplicativo a uma lista de exceções.</span><span class="sxs-lookup"><span data-stu-id="186cc-247">A user or administrator can explicitly remove support for a 32-bit application by adding the application to an exceptions list.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-248">**Depurar**</span><span class="sxs-lookup"><span data-stu-id="186cc-248">**Debug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-249">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="186cc-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-251">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ debug")</span><span class="sxs-lookup"><span data-stu-id="186cc-251">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)\|SM\_DEBUG")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-252">O sistema operacional é uma compilação marcada (depuração).</span><span class="sxs-lookup"><span data-stu-id="186cc-252">Operating system is a checked (debug) build.</span></span> <span data-ttu-id="186cc-253">Se for **true**, a versão de depuração será instalada.</span><span class="sxs-lookup"><span data-stu-id="186cc-253">If **True**, the debugging version is installed.</span></span> <span data-ttu-id="186cc-254">As compilações verificadas fornecem verificação de erros, verificação de argumentos e código de depuração do sistema.</span><span class="sxs-lookup"><span data-stu-id="186cc-254">Checked builds provide error checking, argument verification, and system debugging code.</span></span> <span data-ttu-id="186cc-255">O código adicional em um binário marcado gera uma mensagem de erro do depurador de kernel e quebra o depurador.</span><span class="sxs-lookup"><span data-stu-id="186cc-255">Additional code in a checked binary generates a kernel debugger error message and breaks into the debugger.</span></span> <span data-ttu-id="186cc-256">Isso ajuda a determinar imediatamente a causa e o local do erro.</span><span class="sxs-lookup"><span data-stu-id="186cc-256">This helps immediately determine the cause and location of the error.</span></span> <span data-ttu-id="186cc-257">O desempenho pode ser afetado em uma compilação verificada devido ao código adicional que é executado.</span><span class="sxs-lookup"><span data-stu-id="186cc-257">Performance may be affected in a checked build due to the additional code that is executed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-258">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="186cc-258">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-259">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-260">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="186cc-260">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="186cc-261">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Descrição"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-261">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-262">Descrição do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="186cc-262">Description of the Windows operating system.</span></span> <span data-ttu-id="186cc-263">Algumas interfaces do usuário, por exemplo, aquelas que permitem a edição dessa descrição, limitam seu comprimento a 48 caracteres.</span><span class="sxs-lookup"><span data-stu-id="186cc-263">Some user interfaces for example, those that allow editing of this description, limit its length to 48 characters.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-264">**Fornecido**</span><span class="sxs-lookup"><span data-stu-id="186cc-264">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-265">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="186cc-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-267">Se **for true**, o sistema operacional será distribuído entre vários nós de sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-267">If **True**, the operating system is distributed across several computer system nodes.</span></span> <span data-ttu-id="186cc-268">Nesse caso, esses nós devem ser agrupados como um cluster.</span><span class="sxs-lookup"><span data-stu-id="186cc-268">If so, these nodes should be grouped as a cluster.</span></span>

<span data-ttu-id="186cc-269">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-269">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-270">**EncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="186cc-270">**EncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-271">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-271">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-273">Nível de criptografia para transações seguras: 40 bits, 128 bits ou *n* bits.</span><span class="sxs-lookup"><span data-stu-id="186cc-273">Encryption level for secure transactions: 40-bit, 128-bit, or *n*-bit.</span></span>

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

<span data-ttu-id="186cc-274">**40** bits (0)</span><span class="sxs-lookup"><span data-stu-id="186cc-274">**40-bit** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

<span data-ttu-id="186cc-275">**128** bits (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-275">**128-bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

<span data-ttu-id="186cc-276">**n** bits (2)</span><span class="sxs-lookup"><span data-stu-id="186cc-276">**n-bit** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-277">**ForegroundApplicationBoost**</span><span class="sxs-lookup"><span data-stu-id="186cc-277">**ForegroundApplicationBoost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-278">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="186cc-278">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-279">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="186cc-279">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="186cc-280">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="186cc-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-281">O aumento na prioridade é fornecido ao aplicativo em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="186cc-281">Increase in priority is given to the foreground application.</span></span> <span data-ttu-id="186cc-282">O aumento do aplicativo é implementado fornecendo a um aplicativo mais frações de tempo de execução (comprimentos do Quantum).</span><span class="sxs-lookup"><span data-stu-id="186cc-282">Application boost is implemented by giving an application more execution time slices (quantum lengths).</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="186cc-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="186cc-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-284">O sistema aumenta o comprimento do Quantum em 6.</span><span class="sxs-lookup"><span data-stu-id="186cc-284">The system boosts the quantum length by 6.</span></span>

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="186cc-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-286">O sistema aumenta o comprimento do Quantum em 12.</span><span class="sxs-lookup"><span data-stu-id="186cc-286">The system boosts the quantum length by 12.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="186cc-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (2)</span><span class="sxs-lookup"><span data-stu-id="186cc-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-288">O sistema aumenta o comprimento do Quantum em 18.</span><span class="sxs-lookup"><span data-stu-id="186cc-288">The system boosts the quantum length by 18.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-289">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="186cc-289">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-290">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="186cc-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-292">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="186cc-292">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-293">Número, em kilobytes, da memória física atualmente não utilizada e disponível.</span><span class="sxs-lookup"><span data-stu-id="186cc-293">Number, in kilobytes, of physical memory currently unused and available.</span></span>

<span data-ttu-id="186cc-294">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="186cc-294">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="186cc-295">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-295">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-296">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="186cc-296">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-297">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="186cc-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-299">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Configurações de memória do sistema DMTF \| 1,4 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="186cc-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-300">Número, em kilobytes, que pode ser mapeado para os arquivos de paginação do sistema operacional sem fazer com que nenhuma outra página seja trocada.</span><span class="sxs-lookup"><span data-stu-id="186cc-300">Number, in kilobytes, that can be mapped into the operating system paging files without causing any other pages to be swapped out.</span></span>

<span data-ttu-id="186cc-301">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="186cc-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="186cc-302">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-302">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-303">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="186cc-303">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-304">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="186cc-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-306">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="186cc-306">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-307">Número, em kilobytes, de memória virtual atualmente não utilizado e disponível.</span><span class="sxs-lookup"><span data-stu-id="186cc-307">Number, in kilobytes, of virtual memory currently unused and available.</span></span>

<span data-ttu-id="186cc-308">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="186cc-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="186cc-309">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-309">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="186cc-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-311">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="186cc-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-313">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="186cc-313">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-314">O objeto de data foi instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-314">Date object was installed.</span></span> <span data-ttu-id="186cc-315">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-315">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="186cc-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-317">**LargeSystemCache**</span><span class="sxs-lookup"><span data-stu-id="186cc-317">**LargeSystemCache**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-318">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-320">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="186cc-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="186cc-321">Esta propriedade é obsoleta e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="186cc-321">This property is obsolete and not supported.</span></span>

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span data-ttu-id="186cc-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Otimizar para aplicativos** (0)</span><span class="sxs-lookup"><span data-stu-id="186cc-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimize for Applications** (0)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-323">Otimize a memória para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="186cc-323">Optimize memory for applications.</span></span>

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span data-ttu-id="186cc-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Otimizar para desempenho do sistema** (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimize for System Performance** (1)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-325">Otimize a memória para o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="186cc-325">Optimize memory for system performance.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-326">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="186cc-326">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-327">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="186cc-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-329">Data e hora em que o sistema operacional foi reiniciado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="186cc-329">Date and time the operating system was last restarted.</span></span>

<span data-ttu-id="186cc-330">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-330">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-331">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="186cc-331">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-332">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="186cc-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-334">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemDate "," MIF. \|Informações gerais do DMTF \| 1,6 ")</span><span class="sxs-lookup"><span data-stu-id="186cc-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-335">Versão do sistema operacional da data e hora local.</span><span class="sxs-lookup"><span data-stu-id="186cc-335">Operating system version of the local date and time-of-day.</span></span>

<span data-ttu-id="186cc-336">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-336">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-337">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="186cc-337">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-340">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de suporte do idioma nacional win32api \| [](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| \_ ILANGUAGE")</span><span class="sxs-lookup"><span data-stu-id="186cc-340">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ILANGUAGE")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-341">Identificador de idioma usado pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-341">Language identifier used by the operating system.</span></span> <span data-ttu-id="186cc-342">Um identificador de idioma é uma abreviação numérica internacional padrão para um país/região.</span><span class="sxs-lookup"><span data-stu-id="186cc-342">A language identifier is a standard international numeric abbreviation for a country/region.</span></span> <span data-ttu-id="186cc-343">Cada idioma tem um identificador de idioma exclusivo (LANGid), um valor de 16 bits que consiste em um identificador de idioma primário e um identificador de idioma secundário.</span><span class="sxs-lookup"><span data-stu-id="186cc-343">Each language has a unique language identifier (LANGID), a 16-bit value that consists of a primary language identifier and a secondary language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-344">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="186cc-344">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-347">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-348">Nome do fabricante do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-348">Name of the operating system manufacturer.</span></span> <span data-ttu-id="186cc-349">Para sistemas baseados no Windows, esse valor é "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="186cc-349">For Windows-based systems, this value is "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="186cc-350">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="186cc-350">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-351">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-353">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemMaxProcesses ")</span><span class="sxs-lookup"><span data-stu-id="186cc-353">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-354">Número máximo de contextos de processo aos quais o sistema operacional pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="186cc-354">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="186cc-355">O valor padrão definido pelo provedor é 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="186cc-355">The default value set by the provider is 4294967295 (0xFFFFFFFF).</span></span> <span data-ttu-id="186cc-356">Se não houver um máximo fixo, o valor deverá ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="186cc-356">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="186cc-357">Em sistemas que têm um máximo fixo, esse objeto pode ajudar a diagnosticar falhas que ocorrem quando o máximo é atingido — se for desconhecido, insira 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="186cc-357">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached—if unknown, enter 4294967295 (0xFFFFFFFF).</span></span>

<span data-ttu-id="186cc-358">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-358">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-359">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="186cc-359">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-360">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="186cc-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-362">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="186cc-362">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-363">Número máximo, em quilobytes, de memória que pode ser alocado a um processo.</span><span class="sxs-lookup"><span data-stu-id="186cc-363">Maximum number, in kilobytes, of memory that can be allocated to a process.</span></span> <span data-ttu-id="186cc-364">Para sistemas operacionais sem memória virtual, normalmente esse valor é igual à quantidade total de memória física menos a memória usada pelo BIOS e pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-364">For operating systems with no virtual memory, typically this value is equal to the total amount of physical memory minus the memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="186cc-365">Para alguns sistemas operacionais, esse valor pode ser infinito; nesse caso, 0 (zero) deve ser inserido.</span><span class="sxs-lookup"><span data-stu-id="186cc-365">For some operating systems, this value may be infinity, in which case 0 (zero) should be entered.</span></span> <span data-ttu-id="186cc-366">Em outros casos, esse valor pode ser uma constante, por exemplo, 2G ou 4G.</span><span class="sxs-lookup"><span data-stu-id="186cc-366">In other cases, this value could be a constant, for example, 2G or 4G.</span></span>

<span data-ttu-id="186cc-367">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="186cc-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="186cc-368">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-368">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-369">**MUILanguages**</span><span class="sxs-lookup"><span data-stu-id="186cc-369">**MUILanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-370">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="186cc-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-372">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-373">Idiomas Multilingual User Interface Pack (MUI Pack) instalados no computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-373">Multilingual User Interface Pack (MUI Pack ) languages installed on the computer.</span></span> <span data-ttu-id="186cc-374">Por exemplo, "en-US".</span><span class="sxs-lookup"><span data-stu-id="186cc-374">For example, "en-us".</span></span> <span data-ttu-id="186cc-375">Os idiomas MUI Pack são arquivos de recursos que podem ser instalados na versão em inglês do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-375">MUI Pack languages are resource files that can be installed on the English version of the operating system.</span></span> <span data-ttu-id="186cc-376">Quando um MUI Pack é instalado, você pode alterar o idioma da interface do usuário para um dos idiomas com suporte 33.</span><span class="sxs-lookup"><span data-stu-id="186cc-376">When an MUI Pack is installed, you can can change the user interface language to one of 33 supported languages.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-377">**Nome**</span><span class="sxs-lookup"><span data-stu-id="186cc-377">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-378">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-378">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-380">Instância do sistema operacional em um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-380">Operating system instance within a computer system.</span></span>

<span data-ttu-id="186cc-381">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-381">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-382">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="186cc-382">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-383">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-385">Número de licenças de usuário para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-385">Number of user licenses for the operating system.</span></span> <span data-ttu-id="186cc-386">Se for ilimitado, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="186cc-386">If unlimited, enter 0 (zero).</span></span> <span data-ttu-id="186cc-387">Se for desconhecido, digite-1.</span><span class="sxs-lookup"><span data-stu-id="186cc-387">If unknown, enter -1.</span></span>

<span data-ttu-id="186cc-388">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-388">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-389">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="186cc-389">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-390">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-392">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemProcesses ")</span><span class="sxs-lookup"><span data-stu-id="186cc-392">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-393">Número de contextos de processo atualmente carregados ou em execução no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-393">Number of process contexts currently loaded or running on the operating system.</span></span>

<span data-ttu-id="186cc-394">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-394">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-395">**NumberOfUsers**</span><span class="sxs-lookup"><span data-stu-id="186cc-395">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-396">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-398">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemNumUsers ")</span><span class="sxs-lookup"><span data-stu-id="186cc-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-399">Número de sessões de usuário para as quais o sistema operacional está armazenando informações de estado no momento.</span><span class="sxs-lookup"><span data-stu-id="186cc-399">Number of user sessions for which the operating system is storing state information currently.</span></span>

<span data-ttu-id="186cc-400">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-400">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-401">**OperatingSystemSKU**</span><span class="sxs-lookup"><span data-stu-id="186cc-401">**OperatingSystemSKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-402">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-404">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-405">Número de SKU (unidade de manutenção de estoque) do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-405">Stock Keeping Unit (SKU) number for the operating system.</span></span> <span data-ttu-id="186cc-406">Esses valores são os mesmos que o \**Product \_ \** _ Constants definido em Winnt. h, que são usados com a função [_ *GetProductInfo* \*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="186cc-406">These values are the same as the \**PRODUCT\_\** _ constants defined in WinNT.h that are used with the [_ *GetProductInfo*\*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span>

<span data-ttu-id="186cc-407">A lista a seguir lista os possíveis valores de SKU.</span><span class="sxs-lookup"><span data-stu-id="186cc-407">The following list lists possible SKU values.</span></span>

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span data-ttu-id="186cc-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Produto \_ Indefinido** (0)</span><span class="sxs-lookup"><span data-stu-id="186cc-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUCT\_UNDEFINED** (0)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-409">Indefinido</span><span class="sxs-lookup"><span data-stu-id="186cc-409">Undefined</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span data-ttu-id="186cc-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Produto \_ ULTIMATE** (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUCT\_ULTIMATE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-411">Ultimate Edition, por exemplo, Windows Vista Ultimate.</span><span class="sxs-lookup"><span data-stu-id="186cc-411">Ultimate Edition, e.g. Windows Vista Ultimate.</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span data-ttu-id="186cc-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Produto \_ INÍCIO \_ básico** (2)</span><span class="sxs-lookup"><span data-stu-id="186cc-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUCT\_HOME\_BASIC** (2)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-413">Home Basic Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-413">Home Basic Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span data-ttu-id="186cc-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Produto \_ HOME \_ Premium** (3)</span><span class="sxs-lookup"><span data-stu-id="186cc-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUCT\_HOME\_PREMIUM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-415">Home Premium Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-415">Home Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span data-ttu-id="186cc-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Produto \_ ENTERPRISE** (4)</span><span class="sxs-lookup"><span data-stu-id="186cc-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUCT\_ENTERPRISE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-417">Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-417">Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span data-ttu-id="186cc-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Produto \_ NEGÓCIOS** (6)</span><span class="sxs-lookup"><span data-stu-id="186cc-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUCT\_BUSINESS** (6)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-419">Business Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-419">Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span data-ttu-id="186cc-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Produto \_ \_Servidor Standard** (7)</span><span class="sxs-lookup"><span data-stu-id="186cc-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUCT\_STANDARD\_SERVER** (7)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-421">Windows Server Standard Edition (instalação da experiência desktop)</span><span class="sxs-lookup"><span data-stu-id="186cc-421">Windows Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span data-ttu-id="186cc-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Produto \_ \_Servidor do datacenter** (8)</span><span class="sxs-lookup"><span data-stu-id="186cc-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUCT\_DATACENTER\_SERVER** (8)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-423">Windows Server Datacenter Edition (instalação da experiência desktop)</span><span class="sxs-lookup"><span data-stu-id="186cc-423">Windows Server Datacenter Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span data-ttu-id="186cc-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Produto \_ \_Servidor do SMALLBUSINESS** (9)</span><span class="sxs-lookup"><span data-stu-id="186cc-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUCT\_SMALLBUSINESS\_SERVER** (9)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-425">Edição do Small Business Server</span><span class="sxs-lookup"><span data-stu-id="186cc-425">Small Business Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span data-ttu-id="186cc-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Produto \_ \_Servidor corporativo** (10)</span><span class="sxs-lookup"><span data-stu-id="186cc-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUCT\_ENTERPRISE\_SERVER** (10)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-427">Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-427">Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span data-ttu-id="186cc-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Produto \_ INÍCIO** (11)</span><span class="sxs-lookup"><span data-stu-id="186cc-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUCT\_STARTER** (11)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-429"> Starter Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-429">Starter Edition</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span data-ttu-id="186cc-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Produto \_ Datacenter \_ Server \_ Core** (12)</span><span class="sxs-lookup"><span data-stu-id="186cc-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE** (12)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-431">Datacenter Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-431">Datacenter Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span data-ttu-id="186cc-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Produto \_ STANDARD \_ Server \_ Core** (13)</span><span class="sxs-lookup"><span data-stu-id="186cc-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUCT\_STANDARD\_SERVER\_CORE** (13)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-433">Standard Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-433">Standard Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span data-ttu-id="186cc-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Produto \_ ENTERPRISE \_ Server \_ Core** (14)</span><span class="sxs-lookup"><span data-stu-id="186cc-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE** (14)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-435">Enterprise Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-435">Enterprise Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span data-ttu-id="186cc-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Produto \_ \_Servidor Web** (17)</span><span class="sxs-lookup"><span data-stu-id="186cc-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUCT\_WEB\_SERVER** (17)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-437">Edição do servidor Web</span><span class="sxs-lookup"><span data-stu-id="186cc-437">Web Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span data-ttu-id="186cc-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Produto \_ \_Servidor inicial** (19)</span><span class="sxs-lookup"><span data-stu-id="186cc-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUCT\_HOME\_SERVER** (19)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-439">Home Server Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-439">Home Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span data-ttu-id="186cc-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Produto \_ \_ \_ Servidor do Storage Express** (20)</span><span class="sxs-lookup"><span data-stu-id="186cc-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER** (20)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-441">Storage Express Server Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-441">Storage Express Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span data-ttu-id="186cc-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Produto \_ \_ \_ Servidor padrão de armazenamento** (21)</span><span class="sxs-lookup"><span data-stu-id="186cc-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER** (21)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-443">Windows Storage Server Standard Edition (instalação da experiência desktop)</span><span class="sxs-lookup"><span data-stu-id="186cc-443">Windows Storage Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span data-ttu-id="186cc-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Produto \_ \_ \_ Servidor de grupo de trabalho de armazenamento** (22)</span><span class="sxs-lookup"><span data-stu-id="186cc-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER** (22)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-445">Windows Storage Server Workgroup Edition (instalação da experiência desktop)</span><span class="sxs-lookup"><span data-stu-id="186cc-445">Windows Storage Server Workgroup Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span data-ttu-id="186cc-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Produto \_ \_ \_ Servidor corporativo de armazenamento** (23)</span><span class="sxs-lookup"><span data-stu-id="186cc-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER** (23)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-447">Armazenamento Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-447">Storage Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span data-ttu-id="186cc-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Produto \_ SERVIDOR \_ para o \_ SMALLBUSINESS** (24)</span><span class="sxs-lookup"><span data-stu-id="186cc-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUCT\_SERVER\_FOR\_SMALLBUSINESS** (24)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-449">Servidor para Small Business Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-449">Server For Small Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span data-ttu-id="186cc-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Produto \_ \_Servidor do SMALLBUSINESS \_ Premium** (25)</span><span class="sxs-lookup"><span data-stu-id="186cc-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM** (25)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-451">Small Business Server Premium Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-451">Small Business Server Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span data-ttu-id="186cc-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Produto \_ ENTERPRISE \_ N** (27)</span><span class="sxs-lookup"><span data-stu-id="186cc-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUCT\_ENTERPRISE\_N** (27)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-453">Windows Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-453">Windows Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span data-ttu-id="186cc-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Produto \_ ULTIMATE \_ N** (28)</span><span class="sxs-lookup"><span data-stu-id="186cc-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUCT\_ULTIMATE\_N** (28)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-455">Windows Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-455">Windows Ultimate Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span data-ttu-id="186cc-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Produto \_ \_ \_ Núcleo do servidor Web** (29)</span><span class="sxs-lookup"><span data-stu-id="186cc-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUCT\_WEB\_SERVER\_CORE** (29)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-457">Windows Server Web Server Edition (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-457">Windows Server Web Server Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span data-ttu-id="186cc-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Produto \_ STANDARD \_ Server \_ V** (36)</span><span class="sxs-lookup"><span data-stu-id="186cc-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUCT\_STANDARD\_SERVER\_V** (36)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-459">Windows Server Standard Edition sem Hyper-V</span><span class="sxs-lookup"><span data-stu-id="186cc-459">Windows Server Standard Edition without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span data-ttu-id="186cc-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Produto \_ \_Servidor do datacenter \_ V** (37)</span><span class="sxs-lookup"><span data-stu-id="186cc-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUCT\_DATACENTER\_SERVER\_V** (37)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-461">Windows Server Datacenter Edition sem Hyper-V (instalação completa)</span><span class="sxs-lookup"><span data-stu-id="186cc-461">Windows Server Datacenter Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span data-ttu-id="186cc-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Produto \_ ENTERPRISE \_ Server \_ V** (38)</span><span class="sxs-lookup"><span data-stu-id="186cc-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_V** (38)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-463">Windows Server Enterprise Edition sem Hyper-V (instalação completa)</span><span class="sxs-lookup"><span data-stu-id="186cc-463">Windows Server Enterprise Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span data-ttu-id="186cc-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Produto \_ Datacenter \_ Server \_ Core \_ V** (39)</span><span class="sxs-lookup"><span data-stu-id="186cc-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE\_V** (39)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-465">Windows Server Datacenter Edition sem Hyper-V (instalação do Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-465">Windows Server Datacenter Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span data-ttu-id="186cc-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Produto \_ STANDARD \_ Server \_ Core \_ V** (40)</span><span class="sxs-lookup"><span data-stu-id="186cc-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUCT\_STANDARD\_SERVER\_CORE\_V** (40)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-467">Windows Server Standard Edition sem Hyper-V (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-467">Windows Server Standard Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span data-ttu-id="186cc-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Produto \_ ENTERPRISE \_ Server \_ Core \_ V** (41)</span><span class="sxs-lookup"><span data-stu-id="186cc-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE\_V** (41)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-469">Windows Server Enterprise Edition sem Hyper-V (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-469">Windows Server Enterprise Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span data-ttu-id="186cc-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Produto \_ HYPERV** (42)</span><span class="sxs-lookup"><span data-stu-id="186cc-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUCT\_HYPERV** (42)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-471">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="186cc-471">Microsoft Hyper-V Server</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span data-ttu-id="186cc-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Produto \_ STORAGE \_ Express \_ Server \_ Core** (43)</span><span class="sxs-lookup"><span data-stu-id="186cc-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER\_CORE** (43)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-473">Storage Server Express Edition (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-473">Storage Server Express Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span data-ttu-id="186cc-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Produto \_ \_ \_ Server \_ Core do STORAGE Standard** (44)</span><span class="sxs-lookup"><span data-stu-id="186cc-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER\_CORE** (44)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-475">Storage Server Standard Edition (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-475">Storage Server Standard Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span data-ttu-id="186cc-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Produto \_ \_ \_ \_ Núcleo do servidor de grupo de trabalho de armazenamento** (45)</span><span class="sxs-lookup"><span data-stu-id="186cc-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER\_CORE** (45)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-477">Storage Server Workgroup Edition (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-477">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span data-ttu-id="186cc-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Produto \_ ARMAZENAMENTO \_ Enterprise \_ Server \_ Core** (46)</span><span class="sxs-lookup"><span data-stu-id="186cc-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER\_CORE** (46)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-479">Storage Server Workgroup Edition (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-479">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span data-ttu-id="186cc-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Produto \_ PROFESSIONAL** (48)</span><span class="sxs-lookup"><span data-stu-id="186cc-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUCT\_PROFESSIONAL** (48)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-481">Windows Professional</span><span class="sxs-lookup"><span data-stu-id="186cc-481">Windows Professional</span></span>

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span data-ttu-id="186cc-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Produto \_ \_ \_ Servidor da solução SB** (50)</span><span class="sxs-lookup"><span data-stu-id="186cc-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUCT\_SB\_SOLUTION\_SERVER** (50)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-483">Windows Server Essentials (instalação da experiência desktop)</span><span class="sxs-lookup"><span data-stu-id="186cc-483">Windows Server Essentials (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span data-ttu-id="186cc-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Produto \_ \_Servidor do SMALLBUSINESS \_ Premium \_ Core** (63)</span><span class="sxs-lookup"><span data-stu-id="186cc-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM\_CORE** (63)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-485">Small Business Server Premium (instalação do Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-485">Small Business Server Premium (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span data-ttu-id="186cc-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Produto \_ Servidor de CLUSTER \_ \_ V** (64)</span><span class="sxs-lookup"><span data-stu-id="186cc-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUCT\_CLUSTER\_SERVER\_V** (64)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-487">Windows Compute Cluster Server sem Hyper-V</span><span class="sxs-lookup"><span data-stu-id="186cc-487">Windows Compute Cluster Server without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span data-ttu-id="186cc-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Produto \_ \_ARM principal** (97)</span><span class="sxs-lookup"><span data-stu-id="186cc-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUCT\_CORE\_ARM** (97)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-489">Windows RT</span><span class="sxs-lookup"><span data-stu-id="186cc-489">Windows RT</span></span>

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span data-ttu-id="186cc-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**Produto \_ NÚCLEO** (101)</span><span class="sxs-lookup"><span data-stu-id="186cc-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUCT\_CORE** (101)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-491">Página inicial do Windows</span><span class="sxs-lookup"><span data-stu-id="186cc-491">Windows Home</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span data-ttu-id="186cc-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Produto \_ \_WMC profissional** (103)</span><span class="sxs-lookup"><span data-stu-id="186cc-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUCT\_PROFESSIONAL\_WMC** (103)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-493">Windows Professional com Media Center</span><span class="sxs-lookup"><span data-stu-id="186cc-493">Windows Professional with Media Center</span></span>

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span data-ttu-id="186cc-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Produto \_ MOBILE \_ Core** (104)</span><span class="sxs-lookup"><span data-stu-id="186cc-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUCT\_MOBILE\_CORE** (104)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-495">Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="186cc-495">Windows Mobile</span></span>

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span data-ttu-id="186cc-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Produto \_ IOTUAP** (123)</span><span class="sxs-lookup"><span data-stu-id="186cc-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUCT\_IOTUAP** (123)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-497">Windows IoT (Internet das Coisas) Core</span><span class="sxs-lookup"><span data-stu-id="186cc-497">Windows IoT (Internet of Things) Core</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span data-ttu-id="186cc-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Produto \_ Datacenter \_ nano \_ SERVER** (143)</span><span class="sxs-lookup"><span data-stu-id="186cc-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUCT\_DATACENTER\_NANO\_SERVER** (143)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-499">Windows Server Datacenter Edition (instalação do nano Server)</span><span class="sxs-lookup"><span data-stu-id="186cc-499">Windows Server Datacenter Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span data-ttu-id="186cc-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Produto \_ \_ \_ Servidor nano STANDARD** (144)</span><span class="sxs-lookup"><span data-stu-id="186cc-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUCT\_STANDARD\_NANO\_SERVER** (144)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-501">Windows Server Standard Edition (instalação do nano Server)</span><span class="sxs-lookup"><span data-stu-id="186cc-501">Windows Server Standard Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span data-ttu-id="186cc-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Produto \_ Datacenter \_ WS \_ Server \_ Core** (147)</span><span class="sxs-lookup"><span data-stu-id="186cc-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUCT\_DATACENTER\_WS\_SERVER\_CORE** (147)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-503">Windows Server Datacenter Edition (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-503">Windows Server Datacenter Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span data-ttu-id="186cc-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Produto \_ STANDARD \_ WS \_ Server \_ Core** (148)</span><span class="sxs-lookup"><span data-stu-id="186cc-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUCT\_STANDARD\_WS\_SERVER\_CORE** (148)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-505">Windows Server Standard Edition (instalação Server Core)</span><span class="sxs-lookup"><span data-stu-id="186cc-505">Windows Server Standard Edition (Server Core installation)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-506">**Organização**</span><span class="sxs-lookup"><span data-stu-id="186cc-506">**Organization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-507">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-508">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-508">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-509">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")</span><span class="sxs-lookup"><span data-stu-id="186cc-509">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|RegisteredOrganization")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-510">Nome da empresa para o usuário registrado do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-510">Company name for the registered user of the operating system.</span></span>

<span data-ttu-id="186cc-511">Exemplo: "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="186cc-511">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-512">**OSArchitecture**</span><span class="sxs-lookup"><span data-stu-id="186cc-512">**OSArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-513">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-513">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-514">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-515">Arquitetura do sistema operacional, em vez do processador.</span><span class="sxs-lookup"><span data-stu-id="186cc-515">Architecture of the operating system, as opposed to the processor.</span></span> <span data-ttu-id="186cc-516">Essa propriedade pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="186cc-516">This property can be localized.</span></span>

<span data-ttu-id="186cc-517">Exemplo: 32 bits</span><span class="sxs-lookup"><span data-stu-id="186cc-517">Example: 32-bit</span></span>

</dd> <dt>

<span data-ttu-id="186cc-518">**OSLanguage**</span><span class="sxs-lookup"><span data-stu-id="186cc-518">**OSLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-519">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-519">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-520">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-520">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-521">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| localidade do painel de controle padrão do Win32Registry \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="186cc-521">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|DEFAULT\\\\Control Panel\\\\International\|Locale")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-522">Versão de idioma do sistema operacional instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-522">Language version of the operating system installed.</span></span> <span data-ttu-id="186cc-523">A lista a seguir lista os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="186cc-523">The following list lists the possible values.</span></span> <span data-ttu-id="186cc-524">Exemplo: 0x0807 (alemão, Suíça).</span><span class="sxs-lookup"><span data-stu-id="186cc-524">Example: 0x0807 (German, Switzerland).</span></span>

<dt>

<span data-ttu-id="186cc-525">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="186cc-525">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-526">Árabe</span><span class="sxs-lookup"><span data-stu-id="186cc-526">Arabic</span></span>

</dd> <dt>

<span data-ttu-id="186cc-527">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="186cc-527">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-528">Chinês (simplificado) – China</span><span class="sxs-lookup"><span data-stu-id="186cc-528">Chinese (Simplified)– China</span></span>

</dd> <dt>

<span data-ttu-id="186cc-529">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="186cc-529">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-530">Inglês</span><span class="sxs-lookup"><span data-stu-id="186cc-530">English</span></span>

</dd> <dt>

<span data-ttu-id="186cc-531">1025 (0x401)</span><span class="sxs-lookup"><span data-stu-id="186cc-531">1025 (0x401)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-532">Árabe – Arábia Saudita</span><span class="sxs-lookup"><span data-stu-id="186cc-532">Arabic – Saudi Arabia</span></span>

</dd> <dt>

<span data-ttu-id="186cc-533">1026 (0x402)</span><span class="sxs-lookup"><span data-stu-id="186cc-533">1026 (0x402)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-534">Búlgaro</span><span class="sxs-lookup"><span data-stu-id="186cc-534">Bulgarian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-535">1027 (0x403)</span><span class="sxs-lookup"><span data-stu-id="186cc-535">1027 (0x403)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-536">Catalão</span><span class="sxs-lookup"><span data-stu-id="186cc-536">Catalan</span></span>

</dd> <dt>

<span data-ttu-id="186cc-537">1028 (0x404)</span><span class="sxs-lookup"><span data-stu-id="186cc-537">1028 (0x404)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-538">Chinês (tradicional) – Taiwan</span><span class="sxs-lookup"><span data-stu-id="186cc-538">Chinese (Traditional) – Taiwan</span></span>

</dd> <dt>

<span data-ttu-id="186cc-539">1029 (0x405)</span><span class="sxs-lookup"><span data-stu-id="186cc-539">1029 (0x405)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-540">Tcheco</span><span class="sxs-lookup"><span data-stu-id="186cc-540">Czech</span></span>

</dd> <dt>

<span data-ttu-id="186cc-541">1030 (0x406)</span><span class="sxs-lookup"><span data-stu-id="186cc-541">1030 (0x406)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-542">Dinamarquês</span><span class="sxs-lookup"><span data-stu-id="186cc-542">Danish</span></span>

</dd> <dt>

<span data-ttu-id="186cc-543">1031 (0x407)</span><span class="sxs-lookup"><span data-stu-id="186cc-543">1031 (0x407)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-544">Alemão – Alemanha</span><span class="sxs-lookup"><span data-stu-id="186cc-544">German – Germany</span></span>

</dd> <dt>

<span data-ttu-id="186cc-545">1032 (0x408)</span><span class="sxs-lookup"><span data-stu-id="186cc-545">1032 (0x408)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-546">Grego</span><span class="sxs-lookup"><span data-stu-id="186cc-546">Greek</span></span>

</dd> <dt>

<span data-ttu-id="186cc-547">1033 (0x409)</span><span class="sxs-lookup"><span data-stu-id="186cc-547">1033 (0x409)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-548">Inglês – Estados Unidos</span><span class="sxs-lookup"><span data-stu-id="186cc-548">English – United States</span></span>

</dd> <dt>

<span data-ttu-id="186cc-549">1034 (0x40A)</span><span class="sxs-lookup"><span data-stu-id="186cc-549">1034 (0x40A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-550">Espanhol – classificação tradicional</span><span class="sxs-lookup"><span data-stu-id="186cc-550">Spanish – Traditional Sort</span></span>

</dd> <dt>

<span data-ttu-id="186cc-551">1035 (0x40B)</span><span class="sxs-lookup"><span data-stu-id="186cc-551">1035 (0x40B)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-552">Finlandês</span><span class="sxs-lookup"><span data-stu-id="186cc-552">Finnish</span></span>

</dd> <dt>

<span data-ttu-id="186cc-553">1036 (0x40C)</span><span class="sxs-lookup"><span data-stu-id="186cc-553">1036 (0x40C)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-554">Francês – França</span><span class="sxs-lookup"><span data-stu-id="186cc-554">French – France</span></span>

</dd> <dt>

<span data-ttu-id="186cc-555">1037 (0x40D)</span><span class="sxs-lookup"><span data-stu-id="186cc-555">1037 (0x40D)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-556">Hebraico</span><span class="sxs-lookup"><span data-stu-id="186cc-556">Hebrew</span></span>

</dd> <dt>

<span data-ttu-id="186cc-557">1038 (0x40E)</span><span class="sxs-lookup"><span data-stu-id="186cc-557">1038 (0x40E)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-558">Húngaro</span><span class="sxs-lookup"><span data-stu-id="186cc-558">Hungarian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-559">1039 (0x40F)</span><span class="sxs-lookup"><span data-stu-id="186cc-559">1039 (0x40F)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-560">Islandês</span><span class="sxs-lookup"><span data-stu-id="186cc-560">Icelandic</span></span>

</dd> <dt>

<span data-ttu-id="186cc-561">1040 (0x410)</span><span class="sxs-lookup"><span data-stu-id="186cc-561">1040 (0x410)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-562">Italiano – Itália</span><span class="sxs-lookup"><span data-stu-id="186cc-562">Italian – Italy</span></span>

</dd> <dt>

<span data-ttu-id="186cc-563">1041 (0x411)</span><span class="sxs-lookup"><span data-stu-id="186cc-563">1041 (0x411)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-564">Japonês</span><span class="sxs-lookup"><span data-stu-id="186cc-564">Japanese</span></span>

</dd> <dt>

<span data-ttu-id="186cc-565">1042 (0x412)</span><span class="sxs-lookup"><span data-stu-id="186cc-565">1042 (0x412)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-566">Coreano</span><span class="sxs-lookup"><span data-stu-id="186cc-566">Korean</span></span>

</dd> <dt>

<span data-ttu-id="186cc-567">1043 (0x413)</span><span class="sxs-lookup"><span data-stu-id="186cc-567">1043 (0x413)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-568">Holandês – Holanda</span><span class="sxs-lookup"><span data-stu-id="186cc-568">Dutch – Netherlands</span></span>

</dd> <dt>

<span data-ttu-id="186cc-569">1044 (0x414)</span><span class="sxs-lookup"><span data-stu-id="186cc-569">1044 (0x414)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-570">Norueguês – Bokmal</span><span class="sxs-lookup"><span data-stu-id="186cc-570">Norwegian – Bokmal</span></span>

</dd> <dt>

<span data-ttu-id="186cc-571">1045 (0x415)</span><span class="sxs-lookup"><span data-stu-id="186cc-571">1045 (0x415)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-572">Polonês</span><span class="sxs-lookup"><span data-stu-id="186cc-572">Polish</span></span>

</dd> <dt>

<span data-ttu-id="186cc-573">1046 (0x416)</span><span class="sxs-lookup"><span data-stu-id="186cc-573">1046 (0x416)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-574">Português – Brasil</span><span class="sxs-lookup"><span data-stu-id="186cc-574">Portuguese – Brazil</span></span>

</dd> <dt>

<span data-ttu-id="186cc-575">1047 (0x417)</span><span class="sxs-lookup"><span data-stu-id="186cc-575">1047 (0x417)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-576">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="186cc-576">Rhaeto-Romanic</span></span>

</dd> <dt>

<span data-ttu-id="186cc-577">1048 (0x418)</span><span class="sxs-lookup"><span data-stu-id="186cc-577">1048 (0x418)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-578">Romeno</span><span class="sxs-lookup"><span data-stu-id="186cc-578">Romanian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-579">1049 (0x419)</span><span class="sxs-lookup"><span data-stu-id="186cc-579">1049 (0x419)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-580">Russo</span><span class="sxs-lookup"><span data-stu-id="186cc-580">Russian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-581">1050 (0x41A)</span><span class="sxs-lookup"><span data-stu-id="186cc-581">1050 (0x41A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-582">Croata</span><span class="sxs-lookup"><span data-stu-id="186cc-582">Croatian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-583">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="186cc-583">1051 (0x41B)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-584">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="186cc-584">Slovak</span></span>

</dd> <dt>

<span data-ttu-id="186cc-585">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="186cc-585">1052 (0x41C)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-586">Albanês</span><span class="sxs-lookup"><span data-stu-id="186cc-586">Albanian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-587">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="186cc-587">1053 (0x41D)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-588">Sueco</span><span class="sxs-lookup"><span data-stu-id="186cc-588">Swedish</span></span>

</dd> <dt>

<span data-ttu-id="186cc-589">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="186cc-589">1054 (0x41E)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-590">Tailandês</span><span class="sxs-lookup"><span data-stu-id="186cc-590">Thai</span></span>

</dd> <dt>

<span data-ttu-id="186cc-591">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="186cc-591">1055 (0x41F)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-592">Turco</span><span class="sxs-lookup"><span data-stu-id="186cc-592">Turkish</span></span>

</dd> <dt>

<span data-ttu-id="186cc-593">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="186cc-593">1056 (0x420)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-594">Urdu</span><span class="sxs-lookup"><span data-stu-id="186cc-594">Urdu</span></span>

</dd> <dt>

<span data-ttu-id="186cc-595">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="186cc-595">1057 (0x421)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-596">Indonésio</span><span class="sxs-lookup"><span data-stu-id="186cc-596">Indonesian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-597">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="186cc-597">1058 (0x422)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-598">Ucraniano</span><span class="sxs-lookup"><span data-stu-id="186cc-598">Ukrainian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-599">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="186cc-599">1059 (0x423)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-600">Bielorrusso</span><span class="sxs-lookup"><span data-stu-id="186cc-600">Belarusian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-601">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="186cc-601">1060 (0x424)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-602">Esloveno</span><span class="sxs-lookup"><span data-stu-id="186cc-602">Slovenian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-603">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="186cc-603">1061 (0x425)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-604">Estoniano</span><span class="sxs-lookup"><span data-stu-id="186cc-604">Estonian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-605">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="186cc-605">1062 (0x426)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-606">Letão</span><span class="sxs-lookup"><span data-stu-id="186cc-606">Latvian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-607">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="186cc-607">1063 (0x427)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-608">Lituano</span><span class="sxs-lookup"><span data-stu-id="186cc-608">Lithuanian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-609">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="186cc-609">1065 (0x429)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-610">Persa</span><span class="sxs-lookup"><span data-stu-id="186cc-610">Persian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-611">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="186cc-611">1066 (0x42A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-612">Vietnamita</span><span class="sxs-lookup"><span data-stu-id="186cc-612">Vietnamese</span></span>

</dd> <dt>

<span data-ttu-id="186cc-613">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="186cc-613">1069 (0x42D)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-614">Basco (País Basco)</span><span class="sxs-lookup"><span data-stu-id="186cc-614">Basque (Basque)</span></span>

</dd> <dt>

<span data-ttu-id="186cc-615">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="186cc-615">1070 (0x42E)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-616">Sérvio</span><span class="sxs-lookup"><span data-stu-id="186cc-616">Serbian</span></span>

</dd> <dt>

<span data-ttu-id="186cc-617">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="186cc-617">1071 (0x42F)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-618">Macedônio (nordeste da Macedônia)</span><span class="sxs-lookup"><span data-stu-id="186cc-618">Macedonian (North Macedonia)</span></span>

</dd> <dt>

<span data-ttu-id="186cc-619">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="186cc-619">1072 (0x430)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-620">Sutu</span><span class="sxs-lookup"><span data-stu-id="186cc-620">Sutu</span></span>

</dd> <dt>

<span data-ttu-id="186cc-621">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="186cc-621">1073 (0x431)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-622">Xitsonga</span><span class="sxs-lookup"><span data-stu-id="186cc-622">Tsonga</span></span>

</dd> <dt>

<span data-ttu-id="186cc-623">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="186cc-623">1074 (0x432)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-624">Tswana</span><span class="sxs-lookup"><span data-stu-id="186cc-624">Tswana</span></span>

</dd> <dt>

<span data-ttu-id="186cc-625">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="186cc-625">1076 (0x434)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-626">Xhosa</span><span class="sxs-lookup"><span data-stu-id="186cc-626">Xhosa</span></span>

</dd> <dt>

<span data-ttu-id="186cc-627">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="186cc-627">1077 (0x435)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-628">Zulu</span><span class="sxs-lookup"><span data-stu-id="186cc-628">Zulu</span></span>

</dd> <dt>

<span data-ttu-id="186cc-629">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="186cc-629">1078 (0x436)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-630">Africâner</span><span class="sxs-lookup"><span data-stu-id="186cc-630">Afrikaans</span></span>

</dd> <dt>

<span data-ttu-id="186cc-631">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="186cc-631">1080 (0x438)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-632">Faroês</span><span class="sxs-lookup"><span data-stu-id="186cc-632">Faeroese</span></span>

</dd> <dt>

<span data-ttu-id="186cc-633">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="186cc-633">1081 (0x439)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-634">Híndi</span><span class="sxs-lookup"><span data-stu-id="186cc-634">Hindi</span></span>

</dd> <dt>

<span data-ttu-id="186cc-635">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="186cc-635">1082 (0x43A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-636">Maltês</span><span class="sxs-lookup"><span data-stu-id="186cc-636">Maltese</span></span>

</dd> <dt>

<span data-ttu-id="186cc-637">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="186cc-637">1084 (0x43C)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-638">Gaélico escocês (Reino Unido)</span><span class="sxs-lookup"><span data-stu-id="186cc-638">Scottish Gaelic (United Kingdom)</span></span>

</dd> <dt>

<span data-ttu-id="186cc-639">1085 (0x43D)</span><span class="sxs-lookup"><span data-stu-id="186cc-639">1085 (0x43D)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-640">Iídiche</span><span class="sxs-lookup"><span data-stu-id="186cc-640">Yiddish</span></span>

</dd> <dt>

<span data-ttu-id="186cc-641">1086 (0x43E)</span><span class="sxs-lookup"><span data-stu-id="186cc-641">1086 (0x43E)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-642">Malaio – Malásia</span><span class="sxs-lookup"><span data-stu-id="186cc-642">Malay – Malaysia</span></span>

</dd> <dt>

<span data-ttu-id="186cc-643">2049 (0x801)</span><span class="sxs-lookup"><span data-stu-id="186cc-643">2049 (0x801)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-644">Árabe – Iraque</span><span class="sxs-lookup"><span data-stu-id="186cc-644">Arabic – Iraq</span></span>

</dd> <dt>

<span data-ttu-id="186cc-645">2052 (0x804)</span><span class="sxs-lookup"><span data-stu-id="186cc-645">2052 (0x804)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-646">Chinês (simplificado) – PRC</span><span class="sxs-lookup"><span data-stu-id="186cc-646">Chinese (Simplified) – PRC</span></span>

</dd> <dt>

<span data-ttu-id="186cc-647">2055 (0x807)</span><span class="sxs-lookup"><span data-stu-id="186cc-647">2055 (0x807)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-648">Alemão – Suíça</span><span class="sxs-lookup"><span data-stu-id="186cc-648">German – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="186cc-649">2057 (0x809)</span><span class="sxs-lookup"><span data-stu-id="186cc-649">2057 (0x809)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-650">Inglês – Reino Unido</span><span class="sxs-lookup"><span data-stu-id="186cc-650">English – United Kingdom</span></span>

</dd> <dt>

<span data-ttu-id="186cc-651">2058 (0x80A)</span><span class="sxs-lookup"><span data-stu-id="186cc-651">2058 (0x80A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-652">Espanhol – México</span><span class="sxs-lookup"><span data-stu-id="186cc-652">Spanish – Mexico</span></span>

</dd> <dt>

<span data-ttu-id="186cc-653">2060 (0x80C)</span><span class="sxs-lookup"><span data-stu-id="186cc-653">2060 (0x80C)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-654">Francês – Bélgica</span><span class="sxs-lookup"><span data-stu-id="186cc-654">French – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="186cc-655">2064 (0x810)</span><span class="sxs-lookup"><span data-stu-id="186cc-655">2064 (0x810)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-656">Italiano – Suíça</span><span class="sxs-lookup"><span data-stu-id="186cc-656">Italian – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="186cc-657">2067 (0x813)</span><span class="sxs-lookup"><span data-stu-id="186cc-657">2067 (0x813)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-658">Holandês – Bélgica</span><span class="sxs-lookup"><span data-stu-id="186cc-658">Dutch – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="186cc-659">2068 (0x814)</span><span class="sxs-lookup"><span data-stu-id="186cc-659">2068 (0x814)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-660">Norueguês – Nynorsk</span><span class="sxs-lookup"><span data-stu-id="186cc-660">Norwegian – Nynorsk</span></span>

</dd> <dt>

<span data-ttu-id="186cc-661">2070 (0x816)</span><span class="sxs-lookup"><span data-stu-id="186cc-661">2070 (0x816)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-662">Português – Portugal</span><span class="sxs-lookup"><span data-stu-id="186cc-662">Portuguese – Portugal</span></span>

</dd> <dt>

<span data-ttu-id="186cc-663">2072 (0x818)</span><span class="sxs-lookup"><span data-stu-id="186cc-663">2072 (0x818)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-664">Romeno – Moldova</span><span class="sxs-lookup"><span data-stu-id="186cc-664">Romanian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="186cc-665">2073 (0x819)</span><span class="sxs-lookup"><span data-stu-id="186cc-665">2073 (0x819)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-666">Russo – Moldova</span><span class="sxs-lookup"><span data-stu-id="186cc-666">Russian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="186cc-667">2074 (0x81A)</span><span class="sxs-lookup"><span data-stu-id="186cc-667">2074 (0x81A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-668">Sérvio – latino</span><span class="sxs-lookup"><span data-stu-id="186cc-668">Serbian – Latin</span></span>

</dd> <dt>

<span data-ttu-id="186cc-669">2077 (0x81D)</span><span class="sxs-lookup"><span data-stu-id="186cc-669">2077 (0x81D)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-670">Sueco – Finlândia</span><span class="sxs-lookup"><span data-stu-id="186cc-670">Swedish – Finland</span></span>

</dd> <dt>

<span data-ttu-id="186cc-671">3073 (0xC01)</span><span class="sxs-lookup"><span data-stu-id="186cc-671">3073 (0xC01)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-672">Árabe – Egito</span><span class="sxs-lookup"><span data-stu-id="186cc-672">Arabic – Egypt</span></span>

</dd> <dt>

<span data-ttu-id="186cc-673">3076 (0xC04)</span><span class="sxs-lookup"><span data-stu-id="186cc-673">3076 (0xC04)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-674">Chinês (tradicional) – RAE de Hong Kong</span><span class="sxs-lookup"><span data-stu-id="186cc-674">Chinese (Traditional) – Hong Kong SAR</span></span>

</dd> <dt>

<span data-ttu-id="186cc-675">3079 (0xC07)</span><span class="sxs-lookup"><span data-stu-id="186cc-675">3079 (0xC07)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-676">Alemão – Áustria</span><span class="sxs-lookup"><span data-stu-id="186cc-676">German – Austria</span></span>

</dd> <dt>

<span data-ttu-id="186cc-677">3081 (0xC09)</span><span class="sxs-lookup"><span data-stu-id="186cc-677">3081 (0xC09)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-678">Inglês – Austrália</span><span class="sxs-lookup"><span data-stu-id="186cc-678">English – Australia</span></span>

</dd> <dt>

<span data-ttu-id="186cc-679">3082 (0xC0A)</span><span class="sxs-lookup"><span data-stu-id="186cc-679">3082 (0xC0A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-680">Espanhol – classificação internacional</span><span class="sxs-lookup"><span data-stu-id="186cc-680">Spanish – International Sort</span></span>

</dd> <dt>

<span data-ttu-id="186cc-681">3084 (0xC0C)</span><span class="sxs-lookup"><span data-stu-id="186cc-681">3084 (0xC0C)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-682">Francês – Canadá</span><span class="sxs-lookup"><span data-stu-id="186cc-682">French – Canada</span></span>

</dd> <dt>

<span data-ttu-id="186cc-683">3098 (0xC1A)</span><span class="sxs-lookup"><span data-stu-id="186cc-683">3098 (0xC1A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-684">Sérvio – cirílico</span><span class="sxs-lookup"><span data-stu-id="186cc-684">Serbian – Cyrillic</span></span>

</dd> <dt>

<span data-ttu-id="186cc-685">4097 (0x1001)</span><span class="sxs-lookup"><span data-stu-id="186cc-685">4097 (0x1001)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-686">Árabe – Líbia</span><span class="sxs-lookup"><span data-stu-id="186cc-686">Arabic – Libya</span></span>

</dd> <dt>

<span data-ttu-id="186cc-687">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="186cc-687">4100 (0x1004)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-688">Chinês (simplificado) – Cingapura</span><span class="sxs-lookup"><span data-stu-id="186cc-688">Chinese (Simplified) – Singapore</span></span>

</dd> <dt>

<span data-ttu-id="186cc-689">4103 (0x1007)</span><span class="sxs-lookup"><span data-stu-id="186cc-689">4103 (0x1007)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-690">Alemão – Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="186cc-690">German – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="186cc-691">4105 (0x1009)</span><span class="sxs-lookup"><span data-stu-id="186cc-691">4105 (0x1009)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-692">Inglês – Canadá</span><span class="sxs-lookup"><span data-stu-id="186cc-692">English – Canada</span></span>

</dd> <dt>

<span data-ttu-id="186cc-693">4106 (0x100A)</span><span class="sxs-lookup"><span data-stu-id="186cc-693">4106 (0x100A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-694">Espanhol – Guatemala</span><span class="sxs-lookup"><span data-stu-id="186cc-694">Spanish – Guatemala</span></span>

</dd> <dt>

<span data-ttu-id="186cc-695">4108 (0x100C)</span><span class="sxs-lookup"><span data-stu-id="186cc-695">4108 (0x100C)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-696">Francês – Suíça</span><span class="sxs-lookup"><span data-stu-id="186cc-696">French – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="186cc-697">5121 (0x1401)</span><span class="sxs-lookup"><span data-stu-id="186cc-697">5121 (0x1401)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-698">Árabe – Argélia</span><span class="sxs-lookup"><span data-stu-id="186cc-698">Arabic – Algeria</span></span>

</dd> <dt>

<span data-ttu-id="186cc-699">5127 (0x1407)</span><span class="sxs-lookup"><span data-stu-id="186cc-699">5127 (0x1407)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-700">Alemão – Liechtenstein</span><span class="sxs-lookup"><span data-stu-id="186cc-700">German – Liechtenstein</span></span>

</dd> <dt>

<span data-ttu-id="186cc-701">5129 (0x1409)</span><span class="sxs-lookup"><span data-stu-id="186cc-701">5129 (0x1409)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-702">Inglês – Nova Zelândia</span><span class="sxs-lookup"><span data-stu-id="186cc-702">English – New Zealand</span></span>

</dd> <dt>

<span data-ttu-id="186cc-703">5130 (0x140A)</span><span class="sxs-lookup"><span data-stu-id="186cc-703">5130 (0x140A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-704">Espanhol – Costa Rica</span><span class="sxs-lookup"><span data-stu-id="186cc-704">Spanish – Costa Rica</span></span>

</dd> <dt>

<span data-ttu-id="186cc-705">5132 (0x140C)</span><span class="sxs-lookup"><span data-stu-id="186cc-705">5132 (0x140C)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-706">Francês – Luxemburgo</span><span class="sxs-lookup"><span data-stu-id="186cc-706">French – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="186cc-707">6145 (0x1801)</span><span class="sxs-lookup"><span data-stu-id="186cc-707">6145 (0x1801)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-708">Árabe – Marrocos</span><span class="sxs-lookup"><span data-stu-id="186cc-708">Arabic – Morocco</span></span>

</dd> <dt>

<span data-ttu-id="186cc-709">6153 (0x1809)</span><span class="sxs-lookup"><span data-stu-id="186cc-709">6153 (0x1809)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-710">Inglês – Irlanda</span><span class="sxs-lookup"><span data-stu-id="186cc-710">English – Ireland</span></span>

</dd> <dt>

<span data-ttu-id="186cc-711">6154 (0x180A)</span><span class="sxs-lookup"><span data-stu-id="186cc-711">6154 (0x180A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-712">Espanhol – Panamá</span><span class="sxs-lookup"><span data-stu-id="186cc-712">Spanish – Panama</span></span>

</dd> <dt>

<span data-ttu-id="186cc-713">7169 (0x1C01)</span><span class="sxs-lookup"><span data-stu-id="186cc-713">7169 (0x1C01)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-714">Árabe – Tunísia</span><span class="sxs-lookup"><span data-stu-id="186cc-714">Arabic – Tunisia</span></span>

</dd> <dt>

<span data-ttu-id="186cc-715">7177 (0x1C09)</span><span class="sxs-lookup"><span data-stu-id="186cc-715">7177 (0x1C09)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-716">Inglês – África do Sul</span><span class="sxs-lookup"><span data-stu-id="186cc-716">English – South Africa</span></span>

</dd> <dt>

<span data-ttu-id="186cc-717">7178 (0x1C0A)</span><span class="sxs-lookup"><span data-stu-id="186cc-717">7178 (0x1C0A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-718">Espanhol – República Dominicana</span><span class="sxs-lookup"><span data-stu-id="186cc-718">Spanish – Dominican Republic</span></span>

</dd> <dt>

<span data-ttu-id="186cc-719">8193 (0x2001)</span><span class="sxs-lookup"><span data-stu-id="186cc-719">8193 (0x2001)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-720">Árabe – Omã</span><span class="sxs-lookup"><span data-stu-id="186cc-720">Arabic – Oman</span></span>

</dd> <dt>

<span data-ttu-id="186cc-721">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="186cc-721">8201 (0x2009)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-722">Inglês – Jamaica</span><span class="sxs-lookup"><span data-stu-id="186cc-722">English – Jamaica</span></span>

</dd> <dt>

<span data-ttu-id="186cc-723">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="186cc-723">8202 (0x200A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-724">Espanhol – Venezuela</span><span class="sxs-lookup"><span data-stu-id="186cc-724">Spanish – Venezuela</span></span>

</dd> <dt>

<span data-ttu-id="186cc-725">9217 (0x2401)</span><span class="sxs-lookup"><span data-stu-id="186cc-725">9217 (0x2401)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-726">Árabe – Iêmen</span><span class="sxs-lookup"><span data-stu-id="186cc-726">Arabic – Yemen</span></span>

</dd> <dt>

<span data-ttu-id="186cc-727">9226 (0x240A)</span><span class="sxs-lookup"><span data-stu-id="186cc-727">9226 (0x240A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-728">Espanhol – Colômbia</span><span class="sxs-lookup"><span data-stu-id="186cc-728">Spanish – Colombia</span></span>

</dd> <dt>

<span data-ttu-id="186cc-729">10241 (0x2801)</span><span class="sxs-lookup"><span data-stu-id="186cc-729">10241 (0x2801)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-730">Árabe – Síria</span><span class="sxs-lookup"><span data-stu-id="186cc-730">Arabic – Syria</span></span>

</dd> <dt>

<span data-ttu-id="186cc-731">10249 (0x2809)</span><span class="sxs-lookup"><span data-stu-id="186cc-731">10249 (0x2809)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-732">Inglês – Belize</span><span class="sxs-lookup"><span data-stu-id="186cc-732">English – Belize</span></span>

</dd> <dt>

<span data-ttu-id="186cc-733">10250 (0x280A)</span><span class="sxs-lookup"><span data-stu-id="186cc-733">10250 (0x280A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-734">Espanhol – Peru</span><span class="sxs-lookup"><span data-stu-id="186cc-734">Spanish – Peru</span></span>

</dd> <dt>

<span data-ttu-id="186cc-735">11265 (0x2C01)</span><span class="sxs-lookup"><span data-stu-id="186cc-735">11265 (0x2C01)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-736">Árabe – Jordânia</span><span class="sxs-lookup"><span data-stu-id="186cc-736">Arabic – Jordan</span></span>

</dd> <dt>

<span data-ttu-id="186cc-737">11273 (0x2C09)</span><span class="sxs-lookup"><span data-stu-id="186cc-737">11273 (0x2C09)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-738">Inglês – Trinidad</span><span class="sxs-lookup"><span data-stu-id="186cc-738">English – Trinidad</span></span>

</dd> <dt>

<span data-ttu-id="186cc-739">11274 (0x2C0A)</span><span class="sxs-lookup"><span data-stu-id="186cc-739">11274 (0x2C0A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-740">Espanhol – Argentina</span><span class="sxs-lookup"><span data-stu-id="186cc-740">Spanish – Argentina</span></span>

</dd> <dt>

<span data-ttu-id="186cc-741">12289 (0x3001)</span><span class="sxs-lookup"><span data-stu-id="186cc-741">12289 (0x3001)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-742">Árabe – Líbano</span><span class="sxs-lookup"><span data-stu-id="186cc-742">Arabic – Lebanon</span></span>

</dd> <dt>

<span data-ttu-id="186cc-743">12298 (0x300A)</span><span class="sxs-lookup"><span data-stu-id="186cc-743">12298 (0x300A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-744">Espanhol – Equador</span><span class="sxs-lookup"><span data-stu-id="186cc-744">Spanish – Ecuador</span></span>

</dd> <dt>

<span data-ttu-id="186cc-745">13313 (0x3401)</span><span class="sxs-lookup"><span data-stu-id="186cc-745">13313 (0x3401)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-746">Árabe – Kuwait</span><span class="sxs-lookup"><span data-stu-id="186cc-746">Arabic – Kuwait</span></span>

</dd> <dt>

<span data-ttu-id="186cc-747">13322 (0x340A)</span><span class="sxs-lookup"><span data-stu-id="186cc-747">13322 (0x340A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-748">Espanhol – Chile</span><span class="sxs-lookup"><span data-stu-id="186cc-748">Spanish – Chile</span></span>

</dd> <dt>

<span data-ttu-id="186cc-749">14337 (0x3801)</span><span class="sxs-lookup"><span data-stu-id="186cc-749">14337 (0x3801)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-750">Árabe – E.A.U.</span><span class="sxs-lookup"><span data-stu-id="186cc-750">Arabic – U.A.E.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-751">14346 (0x380A)</span><span class="sxs-lookup"><span data-stu-id="186cc-751">14346 (0x380A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-752">Espanhol – Uruguai</span><span class="sxs-lookup"><span data-stu-id="186cc-752">Spanish – Uruguay</span></span>

</dd> <dt>

<span data-ttu-id="186cc-753">15361 (0x3C01)</span><span class="sxs-lookup"><span data-stu-id="186cc-753">15361 (0x3C01)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-754">Árabe – Bahrein</span><span class="sxs-lookup"><span data-stu-id="186cc-754">Arabic – Bahrain</span></span>

</dd> <dt>

<span data-ttu-id="186cc-755">15370 (0x3C0A)</span><span class="sxs-lookup"><span data-stu-id="186cc-755">15370 (0x3C0A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-756">Espanhol – Paraguai</span><span class="sxs-lookup"><span data-stu-id="186cc-756">Spanish – Paraguay</span></span>

</dd> <dt>

<span data-ttu-id="186cc-757">16385 (0x4001)</span><span class="sxs-lookup"><span data-stu-id="186cc-757">16385 (0x4001)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-758">Árabe – Catar</span><span class="sxs-lookup"><span data-stu-id="186cc-758">Arabic – Qatar</span></span>

</dd> <dt>

<span data-ttu-id="186cc-759">16394 (0x400A)</span><span class="sxs-lookup"><span data-stu-id="186cc-759">16394 (0x400A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-760">Espanhol – Bolívia</span><span class="sxs-lookup"><span data-stu-id="186cc-760">Spanish – Bolivia</span></span>

</dd> <dt>

<span data-ttu-id="186cc-761">17418 (0x440A)</span><span class="sxs-lookup"><span data-stu-id="186cc-761">17418 (0x440A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-762">Espanhol – El Salvador</span><span class="sxs-lookup"><span data-stu-id="186cc-762">Spanish – El Salvador</span></span>

</dd> <dt>

<span data-ttu-id="186cc-763">18442 (0x480A)</span><span class="sxs-lookup"><span data-stu-id="186cc-763">18442 (0x480A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-764">Espanhol – Honduras</span><span class="sxs-lookup"><span data-stu-id="186cc-764">Spanish – Honduras</span></span>

</dd> <dt>

<span data-ttu-id="186cc-765">19466 (0x4C0A)</span><span class="sxs-lookup"><span data-stu-id="186cc-765">19466 (0x4C0A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-766">Espanhol – Nicarágua</span><span class="sxs-lookup"><span data-stu-id="186cc-766">Spanish – Nicaragua</span></span>

</dd> <dt>

<span data-ttu-id="186cc-767">20490 (0x500A)</span><span class="sxs-lookup"><span data-stu-id="186cc-767">20490 (0x500A)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-768">Espanhol – Porto Rico</span><span class="sxs-lookup"><span data-stu-id="186cc-768">Spanish – Puerto Rico</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-769">**OSProductSuite**</span><span class="sxs-lookup"><span data-stu-id="186cc-769">**OSProductSuite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-770">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-770">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-771">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-771">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-772">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ controloptions do \\ \\ \| ProductSuite"), [**bitvalues**](../wmisdk/standard-qualifiers.md) ("pequenas empresas", "Enterprise", "backoffice", "servidor de comunicação", "Terminal Server", "pequenas empresas (restritos)", "NT embutido", "Data Center")</span><span class="sxs-lookup"><span data-stu-id="186cc-772">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\ProductOptions\|ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-773">Inclusões de produto do sistema instaladas e licenciadas para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-773">Installed and licensed system product additions to the operating system.</span></span> <span data-ttu-id="186cc-774">Por exemplo, o valor de 146 (0x92) para **OSProductSuite** indica Enterprise, serviços de terminal e Data Center (bits um, quatro e sete conjuntos).</span><span class="sxs-lookup"><span data-stu-id="186cc-774">For example, the value of 146 (0x92) for **OSProductSuite** indicates Enterprise, Terminal Services, and Data Center (bits one, four, and seven set).</span></span> <span data-ttu-id="186cc-775">A lista a seguir lista os possíveis valores.</span><span class="sxs-lookup"><span data-stu-id="186cc-775">The following list lists possible values.</span></span>

<dt>

<span data-ttu-id="186cc-776">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="186cc-776">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-777">O Microsoft Small Business Server já foi instalado, mas pode ter sido atualizado para outra versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="186cc-777">Microsoft Small Business Server was once installed, but may have been upgraded to another version of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-778">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="186cc-778">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-779">O Windows Server 2008 Enterprise está instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-779">Windows Server 2008 Enterprise is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-780">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="186cc-780">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-781">Os componentes do Windows backoffice estão instalados.</span><span class="sxs-lookup"><span data-stu-id="186cc-781">Windows BackOffice components are installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-782">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="186cc-782">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-783">O servidor de comunicação está instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-783">Communication Server is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-784">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="186cc-784">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-785">Os serviços de terminal estão instalados.</span><span class="sxs-lookup"><span data-stu-id="186cc-785">Terminal Services is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-786">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="186cc-786">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-787">O Microsoft Small Business Server é instalado com a licença de cliente restritiva.</span><span class="sxs-lookup"><span data-stu-id="186cc-787">Microsoft Small Business Server is installed with the restrictive client license.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-788">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="186cc-788">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-789">O Windows Embedded está instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-789">Windows Embedded is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-790">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="186cc-790">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-791">Uma edição do datacenter está instalada.</span><span class="sxs-lookup"><span data-stu-id="186cc-791">A Datacenter edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-792">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="186cc-792">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-793">Os serviços de terminal estão instalados, mas há suporte para apenas uma sessão interativa.</span><span class="sxs-lookup"><span data-stu-id="186cc-793">Terminal Services is installed, but only one interactive session is supported.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-794">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="186cc-794">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-795">O Windows Home Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-795">Windows Home Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-796">1024 (0x400)</span><span class="sxs-lookup"><span data-stu-id="186cc-796">1024 (0x400)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-797">A edição do servidor Web está instalada.</span><span class="sxs-lookup"><span data-stu-id="186cc-797">Web Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-798">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="186cc-798">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-799">O Storage Server Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-799">Storage Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-800">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="186cc-800">16384 (0x4000)</span></span>
</dt> <dd>

<span data-ttu-id="186cc-801">O Compute Cluster Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-801">Compute Cluster Edition is installed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-802">**OSType**</span><span class="sxs-lookup"><span data-stu-id="186cc-802">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-803">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="186cc-803">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-804">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-804">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-805">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="186cc-805">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-806">Tipo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-806">Type of operating system.</span></span> <span data-ttu-id="186cc-807">A lista a seguir identifica os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="186cc-807">The following list identifies the possible values.</span></span>

<span data-ttu-id="186cc-808">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-808">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="186cc-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="186cc-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="186cc-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="186cc-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="186cc-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-812">MACROS</span><span class="sxs-lookup"><span data-stu-id="186cc-812">MACROS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="186cc-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="186cc-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="186cc-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="186cc-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="186cc-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="186cc-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="186cc-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="186cc-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="186cc-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="186cc-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="186cc-818"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="186cc-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="186cc-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="186cc-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="186cc-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="186cc-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="186cc-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="186cc-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="186cc-822"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="186cc-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="186cc-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="186cc-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="186cc-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="186cc-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="186cc-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="186cc-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="186cc-826"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="186cc-826"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="186cc-827"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="186cc-827"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="186cc-828"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="186cc-828"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="186cc-829"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="186cc-829"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="186cc-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="186cc-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="186cc-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="186cc-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="186cc-832"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="186cc-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="186cc-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="186cc-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="186cc-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="186cc-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="186cc-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="186cc-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="186cc-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="186cc-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="186cc-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="186cc-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="186cc-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="186cc-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="186cc-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="186cc-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd>

<span data-ttu-id="186cc-840">Solaris</span><span class="sxs-lookup"><span data-stu-id="186cc-840">Solaris</span></span>

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="186cc-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="186cc-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="186cc-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="186cc-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="186cc-843"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="186cc-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="186cc-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="186cc-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="186cc-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="186cc-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="186cc-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="186cc-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="186cc-847"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="186cc-847"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="186cc-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="186cc-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="186cc-849"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="186cc-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="186cc-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="186cc-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="186cc-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="186cc-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="186cc-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="186cc-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="186cc-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="186cc-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="186cc-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="186cc-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="186cc-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="186cc-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="186cc-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="186cc-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="186cc-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="186cc-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="186cc-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="186cc-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="186cc-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="186cc-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="186cc-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="186cc-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="186cc-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="186cc-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="186cc-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="186cc-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="186cc-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="186cc-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="186cc-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="186cc-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="186cc-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="186cc-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="186cc-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="186cc-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="186cc-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="186cc-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="186cc-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="186cc-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="186cc-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="186cc-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="186cc-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="186cc-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="186cc-871"><span id="OS_390"></span><span id="os_390"></span>**Os/390** (60)</span><span class="sxs-lookup"><span data-stu-id="186cc-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="186cc-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="186cc-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="186cc-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="186cc-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-874">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="186cc-874">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-875">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-875">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-876">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-876">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-877">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="186cc-877">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-878">Descrição adicional para a versão atual do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-878">Additional description for the current operating system version.</span></span>

<span data-ttu-id="186cc-879">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-879">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-880">**PAEEnabled**</span><span class="sxs-lookup"><span data-stu-id="186cc-880">**PAEEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-881">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="186cc-881">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-882">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-882">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-883">Se **for true**, as extensões de endereço físico (PAE) serão habilitadas pelo sistema operacional em execução nos processadores Intel.</span><span class="sxs-lookup"><span data-stu-id="186cc-883">If **True**, the physical address extensions (PAE) are enabled by the operating system running on Intel processors.</span></span> <span data-ttu-id="186cc-884">O PAE permite que os aplicativos resolvam mais de 4 GB de memória física.</span><span class="sxs-lookup"><span data-stu-id="186cc-884">PAE allows applications to address more than 4 GB of physical memory.</span></span> <span data-ttu-id="186cc-885">Quando o PAE está habilitado, o sistema operacional usa a conversão de endereços linear de três níveis em vez de dois níveis.</span><span class="sxs-lookup"><span data-stu-id="186cc-885">When PAE is enabled, the operating system uses three-level linear address translation rather than two-level.</span></span> <span data-ttu-id="186cc-886">Fornecer mais memória física a um aplicativo reduz a necessidade de trocar memória para o arquivo de paginação e aumenta o desempenho.</span><span class="sxs-lookup"><span data-stu-id="186cc-886">Providing more physical memory to an application reduces the need to swap memory to the page file and increases performance.</span></span> <span data-ttu-id="186cc-887">Para habilitar, PAE, use a opção "/PAE" no arquivo de Boot.ini.</span><span class="sxs-lookup"><span data-stu-id="186cc-887">To enable, PAE, use the "/PAE" switch in the Boot.ini file.</span></span> <span data-ttu-id="186cc-888">Para obter mais informações sobre o recurso de extensão de endereço físico, consulte <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .</span><span class="sxs-lookup"><span data-stu-id="186cc-888">For more information about the Physical Address Extension feature, see <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912>.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-889">**PlusProductID**</span><span class="sxs-lookup"><span data-stu-id="186cc-889">**PlusProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-890">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-890">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-891">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-891">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-892">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus!</span><span class="sxs-lookup"><span data-stu-id="186cc-892">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="186cc-893">ProductId ")</span><span class="sxs-lookup"><span data-stu-id="186cc-893">ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-894">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="186cc-894">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-895">**PlusVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="186cc-895">**PlusVersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-896">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-896">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-897">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-897">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-898">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus!</span><span class="sxs-lookup"><span data-stu-id="186cc-898">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="186cc-899">VersionNumber ")</span><span class="sxs-lookup"><span data-stu-id="186cc-899">VersionNumber")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-900">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="186cc-900">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-901">**PortableOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="186cc-901">**PortableOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-902">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="186cc-902">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-903">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-903">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-904">Especifica se o sistema operacional foi inicializado a partir de um dispositivo USB externo.</span><span class="sxs-lookup"><span data-stu-id="186cc-904">Specifies whether the operating system booted from an external USB device.</span></span> <span data-ttu-id="186cc-905">Se for true, o sistema operacional detectou que está inicializando em um dispositivo de armazenamento conectado localmente com suporte.</span><span class="sxs-lookup"><span data-stu-id="186cc-905">If true, the operating system has detected it is booting on a supported locally connected storage device.</span></span>

<span data-ttu-id="186cc-906">**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="186cc-906">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-907">**Primário**</span><span class="sxs-lookup"><span data-stu-id="186cc-907">**Primary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-908">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="186cc-908">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-909">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-909">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-910">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="186cc-910">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-911">Especifica se este é o sistema operacional primário.</span><span class="sxs-lookup"><span data-stu-id="186cc-911">Specifies whether this is the primary operating system.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-912">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="186cc-912">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-913">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-913">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-914">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-914">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-915">Informações adicionais do sistema.</span><span class="sxs-lookup"><span data-stu-id="186cc-915">Additional system information.</span></span>

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

<span data-ttu-id="186cc-916">**Estação de trabalho** (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-916">**Work Station** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

<span data-ttu-id="186cc-917">**Controlador de domínio** (2)</span><span class="sxs-lookup"><span data-stu-id="186cc-917">**Domain Controller** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="186cc-918">**Servidor** (3)</span><span class="sxs-lookup"><span data-stu-id="186cc-918">**Server** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-919">**QuantumLength**</span><span class="sxs-lookup"><span data-stu-id="186cc-919">**QuantumLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-920">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="186cc-920">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-921">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="186cc-921">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="186cc-922">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="186cc-922">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-923">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="186cc-923">Not supported</span></span>

<span data-ttu-id="186cc-924">\* \* Windows Server 2008 e Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="186cc-924">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="186cc-925">A propriedade **QuantumLength** define o número de tiques de relógio por Quantum.</span><span class="sxs-lookup"><span data-stu-id="186cc-925">The **QuantumLength** property defines the number of clock ticks per quantum.</span></span> <span data-ttu-id="186cc-926">Um Quantum é uma unidade de tempo de execução que o Agendador tem permissão para fornecer a um aplicativo antes de alternar para outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="186cc-926">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to other applications.</span></span> <span data-ttu-id="186cc-927">Quando um thread executa um Quantum, o kernel o captura e o move para o final de uma fila para aplicativos com prioridades iguais.</span><span class="sxs-lookup"><span data-stu-id="186cc-927">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="186cc-928">O comprimento real do quantum de um thread varia em diferentes plataformas do Windows.</span><span class="sxs-lookup"><span data-stu-id="186cc-928">The actual length of a thread's quantum varies across different Windows platforms.</span></span> <span data-ttu-id="186cc-929">Somente para Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="186cc-929">For Windows NT/Windows 2000 only.</span></span>

<span data-ttu-id="186cc-930">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="186cc-930">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="186cc-931">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="186cc-931">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

<span data-ttu-id="186cc-932">**Uma marca** (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-932">**One tick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

<span data-ttu-id="186cc-933">**Duas tiques** (2)</span><span class="sxs-lookup"><span data-stu-id="186cc-933">**Two ticks** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-934">**Quantumtype**</span><span class="sxs-lookup"><span data-stu-id="186cc-934">**QuantumType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-935">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="186cc-935">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-936">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="186cc-936">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="186cc-937">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="186cc-937">Not supported</span></span>

<span data-ttu-id="186cc-938">\* \* Windows Server 2008 e Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="186cc-938">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="186cc-939">A propriedade **quantumtype** especifica uma Quantum de comprimento fixo ou variável.</span><span class="sxs-lookup"><span data-stu-id="186cc-939">The **QuantumType** property specifies either fixed or variable length quantums.</span></span> <span data-ttu-id="186cc-940">O padrão do Windows é a Quantum de comprimento variável em que o aplicativo em primeiro plano tem uma Quantum mais longa do que os aplicativos em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="186cc-940">Windows defaults to variable length quantums where the foreground application has a longer quantum than the background applications.</span></span> <span data-ttu-id="186cc-941">O padrão do Windows Server é a Quantum de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="186cc-941">Windows Server defaults to fixed-length quantums.</span></span> <span data-ttu-id="186cc-942">Um Quantum é uma unidade de tempo de execução que o Agendador tem permissão para fornecer a um aplicativo antes de alternar para outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="186cc-942">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to another application.</span></span> <span data-ttu-id="186cc-943">Quando um thread executa um Quantum, o kernel o captura e o move para o final de uma fila para aplicativos com prioridades iguais.</span><span class="sxs-lookup"><span data-stu-id="186cc-943">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="186cc-944">O comprimento real do quantum de um thread varia em diferentes plataformas do Windows.</span><span class="sxs-lookup"><span data-stu-id="186cc-944">The actual length of a thread's quantum varies across different Windows platforms.</span></span>

<span data-ttu-id="186cc-945">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="186cc-945">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="186cc-946">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="186cc-946">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="186cc-947">**Fixo** (1)</span><span class="sxs-lookup"><span data-stu-id="186cc-947">**Fixed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

<span data-ttu-id="186cc-948">**Variável** (2)</span><span class="sxs-lookup"><span data-stu-id="186cc-948">**Variable** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-949">**RegisteredUser**</span><span class="sxs-lookup"><span data-stu-id="186cc-949">**RegisteredUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-950">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-950">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-951">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-952">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| RegisteredOwner")</span><span class="sxs-lookup"><span data-stu-id="186cc-952">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|RegisteredOwner")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-953">Nome do usuário registrado do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-953">Name of the registered user of the operating system.</span></span>

<span data-ttu-id="186cc-954">Exemplo: "Ben Smith"</span><span class="sxs-lookup"><span data-stu-id="186cc-954">Example: "Ben Smith"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-955">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="186cc-955">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-956">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-956">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-957">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-958">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="186cc-958">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-959">Número de identificação de série do produto do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-959">Operating system product serial identification number.</span></span>

<span data-ttu-id="186cc-960">Exemplo: "10497-OEM-0031416-71674"</span><span class="sxs-lookup"><span data-stu-id="186cc-960">Example: "10497-OEM-0031416-71674"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-961">**ServicePackMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="186cc-961">**ServicePackMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-962">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="186cc-962">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-963">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-963">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-964">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")</span><span class="sxs-lookup"><span data-stu-id="186cc-964">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMajor**")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-965">Número de versão principal do service pack instalado no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-965">Major version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="186cc-966">Se nenhum service pack tiver sido instalado, o valor será 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="186cc-966">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-967">**ServicePackMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="186cc-967">**ServicePackMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-968">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="186cc-968">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-969">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-969">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-970">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")</span><span class="sxs-lookup"><span data-stu-id="186cc-970">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMinor**")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-971">Número de versão secundária do service pack instalado no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="186cc-971">Minor version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="186cc-972">Se nenhum service pack tiver sido instalado, o valor será 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="186cc-972">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-973">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="186cc-973">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-974">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="186cc-974">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-975">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-975">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-976">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Configurações de memória do sistema DMTF \| 1,3 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="186cc-976">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-977">O número total de quilobytes que podem ser armazenados nos arquivos de paginação do sistema operacional – 0 (zero) indica que não há arquivos de paginação.</span><span class="sxs-lookup"><span data-stu-id="186cc-977">Total number of kilobytes that can be stored in the operating system paging files—0 (zero) indicates that there are no paging files.</span></span> <span data-ttu-id="186cc-978">Lembre-se de que esse número não representa o tamanho físico real do arquivo de paginação no disco.</span><span class="sxs-lookup"><span data-stu-id="186cc-978">Be aware that this number does not represent the actual physical size of the paging file on disk.</span></span>

<span data-ttu-id="186cc-979">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="186cc-979">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="186cc-980">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-980">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-981">**Status**</span><span class="sxs-lookup"><span data-stu-id="186cc-981">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-982">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-982">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-983">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-983">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-984">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="186cc-984">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-985">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="186cc-985">Current status of the object.</span></span> <span data-ttu-id="186cc-986">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="186cc-986">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="186cc-987">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitada para inteligente, pode funcionar corretamente, mas prevê uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="186cc-987">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="186cc-988">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="186cc-988">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="186cc-989">O status do serviço se aplica ao trabalho administrativo, como espelhamento de espelho de um disco, recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="186cc-989">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="186cc-990">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="186cc-990">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="186cc-991">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-991">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="186cc-992">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="186cc-992">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="186cc-993">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="186cc-993">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="186cc-994">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="186cc-994">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="186cc-995">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="186cc-995">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="186cc-996">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="186cc-996">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="186cc-997">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="186cc-997">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="186cc-998">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="186cc-998">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="186cc-999">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="186cc-999">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="186cc-1000">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="186cc-1000">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="186cc-1001">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="186cc-1001">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="186cc-1002">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="186cc-1002">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="186cc-1003">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="186cc-1003">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-1004">**SuiteMask**</span><span class="sxs-lookup"><span data-stu-id="186cc-1004">**SuiteMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1005">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="186cc-1005">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1006">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1006">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1007">Qualificadores: [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**bitvalues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, backoffice Edition", "Windows Server, Communications Edition", "serviços de terminal da Microsoft", "Windows Server, Small Business Edition restrito", "Windows Embedded", "Windows Server, Datacenter Edition", "usuário único", "Windows Home Edition", "Windows Server, Web Edition")</span><span class="sxs-lookup"><span data-stu-id="186cc-1007">Qualifiers: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1008">Sinalizadores de bits que identificam os pacotes de produtos disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="186cc-1008">Bit flags that identify the product suites available on the system.</span></span>

<span data-ttu-id="186cc-1009">Por exemplo, para especificar pessoal e BackOffice, defina **SuiteMask** como `4 | 512` ou `516` .</span><span class="sxs-lookup"><span data-stu-id="186cc-1009">For example, to specify both Personal and BackOffice, set **SuiteMask** to `4 | 512` or `516`.</span></span>

<dt>

<span data-ttu-id="186cc-1010">1</span><span class="sxs-lookup"><span data-stu-id="186cc-1010">1</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1011">Pequenas empresas</span><span class="sxs-lookup"><span data-stu-id="186cc-1011">Small Business</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1012">2</span><span class="sxs-lookup"><span data-stu-id="186cc-1012">2</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1013">Enterprise</span><span class="sxs-lookup"><span data-stu-id="186cc-1013">Enterprise</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1014">4</span><span class="sxs-lookup"><span data-stu-id="186cc-1014">4</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1015">BackOffice</span><span class="sxs-lookup"><span data-stu-id="186cc-1015">BackOffice</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1016">8</span><span class="sxs-lookup"><span data-stu-id="186cc-1016">8</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1017">Comunicações</span><span class="sxs-lookup"><span data-stu-id="186cc-1017">Communications</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1018">16</span><span class="sxs-lookup"><span data-stu-id="186cc-1018">16</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1019">Serviços de Terminal</span><span class="sxs-lookup"><span data-stu-id="186cc-1019">Terminal Services</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1020">32</span><span class="sxs-lookup"><span data-stu-id="186cc-1020">32</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1021">Pequena empresa restrita</span><span class="sxs-lookup"><span data-stu-id="186cc-1021">Small Business Restricted</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1022">64</span><span class="sxs-lookup"><span data-stu-id="186cc-1022">64</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1023">Edição inserida</span><span class="sxs-lookup"><span data-stu-id="186cc-1023">Embedded Edition</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1024">128</span><span class="sxs-lookup"><span data-stu-id="186cc-1024">128</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1025">Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-1025">Datacenter Edition</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1026">256</span><span class="sxs-lookup"><span data-stu-id="186cc-1026">256</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1027">Usuário único</span><span class="sxs-lookup"><span data-stu-id="186cc-1027">Single User</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1028">512</span><span class="sxs-lookup"><span data-stu-id="186cc-1028">512</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1029">Home Edition</span><span class="sxs-lookup"><span data-stu-id="186cc-1029">Home Edition</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1030">1024</span><span class="sxs-lookup"><span data-stu-id="186cc-1030">1024</span></span>
</dt> <dd>

<span data-ttu-id="186cc-1031">Edição do servidor Web</span><span class="sxs-lookup"><span data-stu-id="186cc-1031">Web Server Edition</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="186cc-1032">**SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="186cc-1032">**SystemDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1033">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-1033">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1034">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1034">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1035">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de registro win32api \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| caminhos \| TargetDevice")</span><span class="sxs-lookup"><span data-stu-id="186cc-1035">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Registry Functions\|[**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring)\|Paths\|TargetDevice")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1036">Partição do disco físico na qual o sistema operacional está instalado.</span><span class="sxs-lookup"><span data-stu-id="186cc-1036">Physical disk partition on which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1037">**SystemDirectory**</span><span class="sxs-lookup"><span data-stu-id="186cc-1037">**SystemDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1038">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-1038">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1039">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1039">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1040">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de informações do sistema win32api [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span><span class="sxs-lookup"><span data-stu-id="186cc-1040">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1041">Diretório do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-1041">System directory of the operating system.</span></span>

<span data-ttu-id="186cc-1042">Exemplo: "C: \\ Windows \\ System32"</span><span class="sxs-lookup"><span data-stu-id="186cc-1042">Example: "C:\\WINDOWS\\SYSTEM32"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1043">**SystemDrive**</span><span class="sxs-lookup"><span data-stu-id="186cc-1043">**SystemDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1044">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-1044">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1045">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1045">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1046">Letra da unidade de disco na qual o sistema operacional reside.</span><span class="sxs-lookup"><span data-stu-id="186cc-1046">Letter of the disk drive on which the operating system resides.</span></span> <span data-ttu-id="186cc-1047">Exemplo: "C:"</span><span class="sxs-lookup"><span data-stu-id="186cc-1047">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1048">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="186cc-1048">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1049">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="186cc-1049">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1050">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1050">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1051">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="186cc-1051">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1052">Espaço total de permuta em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="186cc-1052">Total swap space in kilobytes.</span></span> <span data-ttu-id="186cc-1053">Esse valor pode ser **NULL** (não especificado) se o espaço de permuta não for diferenciado dos arquivos de paginação.</span><span class="sxs-lookup"><span data-stu-id="186cc-1053">This value may be **NULL** (unspecified) if the swap space is not distinguished from page files.</span></span> <span data-ttu-id="186cc-1054">No entanto, alguns sistemas operacionais distinguem esses conceitos.</span><span class="sxs-lookup"><span data-stu-id="186cc-1054">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="186cc-1055">Por exemplo, no UNIX, processos inteiros podem ser trocados quando a lista de páginas gratuita cai e permanece abaixo de uma quantidade especificada.</span><span class="sxs-lookup"><span data-stu-id="186cc-1055">For example, in UNIX, whole processes can be swapped out when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="186cc-1056">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="186cc-1056">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="186cc-1057">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-1057">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1058">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="186cc-1058">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1059">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="186cc-1059">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1060">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1060">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1061">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="186cc-1061">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1062">Número, em kilobytes, de memória virtual.</span><span class="sxs-lookup"><span data-stu-id="186cc-1062">Number, in kilobytes, of virtual memory.</span></span> <span data-ttu-id="186cc-1063">Por exemplo, isso pode ser calculado adicionando a quantidade de RAM total à quantidade de espaço de paginação, ou seja, adicionando a quantidade de memória ou agregada pelo sistema de computador à propriedade, **SizeStoredInPagingFiles**.</span><span class="sxs-lookup"><span data-stu-id="186cc-1063">For example, this may be calculated by adding the amount of total RAM to the amount of paging space, that is, adding the amount of memory in or aggregated by the computer system to the property, **SizeStoredInPagingFiles**.</span></span>

<span data-ttu-id="186cc-1064">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="186cc-1064">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="186cc-1065">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-1065">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1066">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="186cc-1066">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1067">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="186cc-1067">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1068">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1068">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1069">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="186cc-1069">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1070">Quantidade total, em kilobytes, da memória física disponível para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-1070">Total amount, in kilobytes, of physical memory available to the operating system.</span></span> <span data-ttu-id="186cc-1071">Esse valor não indica necessariamente a quantidade real de memória física, mas o que é relatado para o sistema operacional como disponível para ele.</span><span class="sxs-lookup"><span data-stu-id="186cc-1071">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="186cc-1072">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="186cc-1072">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="186cc-1073">Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-1073">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1074">**Versão**</span><span class="sxs-lookup"><span data-stu-id="186cc-1074">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1075">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-1075">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1076">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1076">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1077">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")</span><span class="sxs-lookup"><span data-stu-id="186cc-1077">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwMajorVersion, dwMinorVersion")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1078">Número de versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-1078">Version number of the operating system.</span></span>

<span data-ttu-id="186cc-1079">Exemplo: "4,0"</span><span class="sxs-lookup"><span data-stu-id="186cc-1079">Example: "4.0"</span></span>

</dd> <dt>

<span data-ttu-id="186cc-1080">**WindowsDirectory**</span><span class="sxs-lookup"><span data-stu-id="186cc-1080">**WindowsDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186cc-1081">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="186cc-1081">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1082">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="186cc-1082">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186cc-1083">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| funções de informações do sistema \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span><span class="sxs-lookup"><span data-stu-id="186cc-1083">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span></span>
</dt> </dl>

<span data-ttu-id="186cc-1084">Diretório do Windows do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-1084">Windows directory of the operating system.</span></span>

<span data-ttu-id="186cc-1085">Exemplo: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="186cc-1085">Example: "C:\\WINDOWS"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="186cc-1086">Comentários</span><span class="sxs-lookup"><span data-stu-id="186cc-1086">Remarks</span></span>

<span data-ttu-id="186cc-1087">A classe de sistema **\_ operacional Win32** é derivada do [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="186cc-1087">The **Win32\_OperatingSystem** class is derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<span data-ttu-id="186cc-1088">Qualquer sistema operacional que pode ser instalado em um computador que possa executar um sistema operacional baseado no Windows é um descendente ou membro dessa classe.</span><span class="sxs-lookup"><span data-stu-id="186cc-1088">Any operating system that can be installed on a computer that can run a Windows-based operating system is a descendant or member of this class.</span></span> <span data-ttu-id="186cc-1089">**Win32 \_ O OperatingSystem** é uma classe singleton.</span><span class="sxs-lookup"><span data-stu-id="186cc-1089">**Win32\_OperatingSystem** is a singleton class.</span></span> <span data-ttu-id="186cc-1090">Para obter a instância única, use "@" para a chave.</span><span class="sxs-lookup"><span data-stu-id="186cc-1090">To get the single instance, use "@" for the key.</span></span>

<span data-ttu-id="186cc-1091">Ao contrário da maioria das outras classes WMI geradas pelo MgmtClassGen, o método **OperatingSystem. CreateInstance**() retornará um objeto **OperatingSystem** em branco.</span><span class="sxs-lookup"><span data-stu-id="186cc-1091">Unlike most of the other WMI classes generated by MgmtClassGen, the **OperatingSystem.CreateInstance**() method will return a blank **OperatingSystem** object.</span></span> <span data-ttu-id="186cc-1092">Portanto, se você estiver usando C \# com MgmtClassGen, poderá usar o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="186cc-1092">Therefore, if you are using C\# with MgmtClassGen, you can use the following code:</span></span>


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a><span data-ttu-id="186cc-1093">Exemplos</span><span class="sxs-lookup"><span data-stu-id="186cc-1093">Examples</span></span>

<span data-ttu-id="186cc-1094">Você pode encontrar um exemplo de VBScript que obtém os dados do sistema operacional e do processador do [**Win32 \_ ComputerSystem**](win32-computersystem.md), do [**\_ processador Win32**](win32-processor.md)e do **\_ OperatingSystem do Win32** nos exemplos de tópico do [**\_ processador Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="186cc-1094">You can find a VBScript example that obtains operating system and processor data from [**Win32\_ComputerSystem**](win32-computersystem.md), [**Win32\_Processor**](win32-processor.md), and **Win32\_OperatingSystem** in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="186cc-1095">A amostra [gerar relatórios do ambiente do Exchange usando](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) o PowerShell PowerShell na galeria do TechNet usa uma classe do sistema **\_ operacional Win32** como parte de um aplicativo maior para gerar relatórios de ambiente do Exchange.</span><span class="sxs-lookup"><span data-stu-id="186cc-1095">The [Generate Exchange Environment Reports using Powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell sample on TechNet Gallery uses a **Win32\_OperatingSystem** class as part of a larger application to generate exchange environment reports.</span></span>

<span data-ttu-id="186cc-1096">A amostra [obter tempo de atividade do servidor usando WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) na galeria do TechNet usa a propriedade **LastBootupTime** para determinar quanto tempo o servidor esteve ativo.</span><span class="sxs-lookup"><span data-stu-id="186cc-1096">The [Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) sample in the TechNet Gallery uses the **LastBootupTime** property to determine how long the server has been active.</span></span> <span data-ttu-id="186cc-1097">O exemplo também usa a opção Timeout para garantir que a chamada WMI não pare.</span><span class="sxs-lookup"><span data-stu-id="186cc-1097">The sample also uses the timeout option to ensure that the WMI call does not hang.</span></span>

<span data-ttu-id="186cc-1098">O exemplo de código VBScript do [recuperador de informações do WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) na galeria do TechNet usa a classe **Win32 \_ OperatingSystem** para recuperar informações do sistema operacional de vários computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="186cc-1098">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_OperatingSystem** class to retrieve OS information from a number of remote computers.</span></span>

<span data-ttu-id="186cc-1099">O script a seguir obtém as instâncias de **\_ OperatingSystem do Win32** no namespace padrão "raiz \\ CIMv2" e, em seguida, exibe informações sobre o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="186cc-1099">The following script obtains the instances of **Win32\_OperatingSystem** in the default "Root\\CIMv2" namespace, and then displays information about the operating system.</span></span>


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="186cc-1100">O exemplo de código do PowerShell a seguir exibe todas as informações operacionais sobre o sistema operacional atual.</span><span class="sxs-lookup"><span data-stu-id="186cc-1100">The following PowerShell code sample displays all the operating information about the current OS.</span></span>


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a><span data-ttu-id="186cc-1101">Requisitos</span><span class="sxs-lookup"><span data-stu-id="186cc-1101">Requirements</span></span>



| <span data-ttu-id="186cc-1102">Requisito</span><span class="sxs-lookup"><span data-stu-id="186cc-1102">Requirement</span></span> | <span data-ttu-id="186cc-1103">Valor</span><span class="sxs-lookup"><span data-stu-id="186cc-1103">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="186cc-1104">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="186cc-1104">Minimum supported client</span></span><br/> | <span data-ttu-id="186cc-1105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="186cc-1105">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="186cc-1106">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="186cc-1106">Minimum supported server</span></span><br/> | <span data-ttu-id="186cc-1107">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="186cc-1107">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="186cc-1108">Namespace</span><span class="sxs-lookup"><span data-stu-id="186cc-1108">Namespace</span></span><br/>                | <span data-ttu-id="186cc-1109">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="186cc-1109">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="186cc-1110">MOF</span><span class="sxs-lookup"><span data-stu-id="186cc-1110">MOF</span></span><br/>                      | <dl> <span data-ttu-id="186cc-1111"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="186cc-1111"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="186cc-1112">DLL</span><span class="sxs-lookup"><span data-stu-id="186cc-1112">DLL</span></span><br/>                      | <dl> <span data-ttu-id="186cc-1113"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="186cc-1113"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="186cc-1114">Confira também</span><span class="sxs-lookup"><span data-stu-id="186cc-1114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186cc-1115">**Sistema \_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="186cc-1115">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="186cc-1116">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="186cc-1116">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="186cc-1117">Tarefas do WMI: sistemas operacionais</span><span class="sxs-lookup"><span data-stu-id="186cc-1117">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[<span data-ttu-id="186cc-1118">Tarefas do WMI: hardware do computador</span><span class="sxs-lookup"><span data-stu-id="186cc-1118">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[<span data-ttu-id="186cc-1119">Tarefas do WMI: gerenciamento de desktop</span><span class="sxs-lookup"><span data-stu-id="186cc-1119">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
