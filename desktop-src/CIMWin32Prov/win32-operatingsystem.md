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
# <a name="win32_operatingsystem-class"></a>Classe do sistema \_ operacional Win32

A [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ OperatingSystem do Win32** representa um sistema operacional baseado no Windows instalado em um computador.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe de sistema **\_ operacional Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de sistema **\_ operacional Win32** tem esses métodos.



| Método                                                                                     | Descrição                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reboot**](reboot-method-in-class-win32-operatingsystem.md)                             | Desliga e reinicia o sistema de computador.<br/>                                                                                                                                                                                                           |
| [**SetDateTime**](setdatetime-method-in-class-win32-operatingsystem.md)                   | Permite definir a data e a hora do computador.<br/>                                                                                                                                                                                                                |
| [**Desligar**](shutdown-method-in-class-win32-operatingsystem.md)                         | Descarrega programas e DLLs no ponto em que é seguro desligar o computador.<br/>                                                                                                                                                                           |
| [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)               | Fornece o conjunto completo de opções de desligamento com suporte dos sistemas operacionais Windows.<br/>                                                                                                                                                                           |
| [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | Fornece o mesmo conjunto de opções de desligamento com suporte pelo método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) no sistema **\_ operacional Win32**, mas também permite que você especifique comentários, um motivo para o desligamento ou um tempo limite.<br/> |



 

### <a name="properties"></a>Propriedades

A classe de sistema **\_ operacional Win32** tem essas propriedades.

<dl> <dt>

**BootDevice**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| informações de mapa de unidade \_ \_ \| btInt13Unit")
</dt> </dl>

Nome da unidade de disco da qual o sistema operacional Windows é iniciado.

Exemplo: " \\ \\ Device \\ Harddisk0"

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")
</dt> </dl>

Número de Build de um sistema operacional. Ele pode ser usado para obter informações de versão mais precisas do que os números de versão de lançamento do produto.

Exemplo: "1381"

</dd> <dt>

**BuildType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| CurrentType")
</dt> </dl>

Tipo de compilação usado para um sistema operacional.

Exemplos: "" Build de varejo "", "" compilação verificada ""

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrição do objeto — uma cadeia de caracteres de uma linha. A cadeia de caracteres inclui a versão do sistema operacional. Por exemplo, "Microsoft Windows 7 Enterprise". Essa propriedade pode ser localizada.

**Windows Vista e Windows 7:** Esta propriedade pode conter caracteres à direita. Por exemplo, a cadeia de caracteres "Microsoft Windows 7 Enterprise" (espaço à direita incluído) pode ser necessária para recuperar informações usando essa propriedade.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Código de**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| localidade \_ IDEFAULTANSICODEPAGE")
</dt> </dl>

Valor da página de código que um sistema operacional usa. Uma página de código contém uma tabela de caracteres que um sistema operacional usa para converter as cadeias para diferentes idiomas. O American National Standards Institute (ANSI) lista os valores que representam as páginas de código definidas. Se um sistema operacional não usar uma página de código ANSI, esse membro será definido como 0 (zero). A cadeia de **código** pode usar, no máximo, seis caracteres para definir o valor da página de código.

Exemplo: "1255"

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de suporte do idioma nacional win32api \| [](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| \_ ICOUNTRY")
</dt> </dl>

Código para o país/região que um sistema operacional usa. Os valores são baseados em prefixos de discagem telefônica internacional — também conhecidos como códigos de país/região da IBM. Essa propriedade pode usar um máximo de seis caracteres para definir o valor de código de país/região.

Exemplo: "1" (Estados Unidos)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância. Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da classe de criação do sistema de computador de escopo.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**CSDVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")
</dt> </dl>

Cadeia de caracteres terminada em **nulo** que indica as Service Pack mais recentes instaladas em um computador. Se nenhum service pack estiver instalado, a cadeia de caracteres será **nula**.

Exemplo: "Service Pack 3"

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome do sistema de computador de escopo.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")
</dt> </dl>

Número, em minutos, um sistema operacional é deslocado de Greenwich Mean Time (GMT). O número é positivo, negativo ou zero.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**DataExecutionPrevention \_ 32BitApplications**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Quando o recurso de hardware de prevenção de execução de dados estiver disponível, essa propriedade indicará que o recurso está definido para funcionar para aplicativos de 32 bits, se **for verdadeiro**. Em computadores de 64 bits, o recurso de prevenção de execução de dados é configurado no repositório [BCD (dados de configuração da inicialização)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) e as propriedades no sistema **\_ operacional Win32** são definidas de acordo.

</dd> <dt>

**DataExecutionPrevention \_ disponível**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

A prevenção de execução de dados é um recurso de hardware para evitar ataques de saturação de buffer, interrompendo a execução do código em páginas de memória do tipo de dados. Se for **true**, esse recurso estará disponível. Em computadores de 64 bits, o recurso de prevenção de execução de dados é configurado no repositório BCD e as propriedades no sistema **\_ operacional do Win32** são definidas de acordo.

</dd> <dt>

**\_Drivers DataExecutionPrevention**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Quando o recurso de hardware de prevenção de execução de dados estiver disponível, essa propriedade indicará que o recurso está definido para funcionar para drivers se **for verdadeiro**. Em computadores de 64 bits, o recurso de prevenção de execução de dados é configurado no repositório BCD e as propriedades no sistema **\_ operacional do Win32** são definidas de acordo.

</dd> <dt>

**DataExecutionPrevention \_ SupportPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Indica qual configuração de DEP (prevenção de execução de dados) é aplicada. A configuração de DEP especifica a extensão à qual a DEP se aplica a aplicativos de 32 bits no sistema. O DEP sempre é aplicado ao kernel do Windows.

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Sempre desativado** (0)


</dt> <dd>

A DEP é desativada para todos os aplicativos de 32 bits no computador sem exceções. Essa configuração não está disponível para a interface do usuário.

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)


</dt> <dd>

O DEP está habilitado para todos os aplicativos de 32 bits no computador. Essa configuração não está disponível para a interface do usuário.

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Aceitar** (2)


</dt> <dd>

O DEP é habilitado para um número limitado de binários, o kernel e todos os serviços baseados no Windows. No entanto, ela está desativada por padrão para todos os aplicativos de 32 bits. Um usuário ou administrador deve escolher explicitamente o **Always on** ou a configuração de **recusa** antes que a DEP possa ser aplicada a aplicativos de 32 bits.

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Recusar** (3)


</dt> <dd>

O DEP é habilitado por padrão para todos os aplicativos de 32 bits. Um usuário ou administrador pode remover explicitamente o suporte para um aplicativo de 32 bits adicionando o aplicativo a uma lista de exceções.

</dd> </dl>

</dd> <dt>

**Depurar**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ debug")
</dt> </dl>

O sistema operacional é uma compilação marcada (depuração). Se for **true**, a versão de depuração será instalada. As compilações verificadas fornecem verificação de erros, verificação de argumentos e código de depuração do sistema. O código adicional em um binário marcado gera uma mensagem de erro do depurador de kernel e quebra o depurador. Isso ajuda a determinar imediatamente a causa e o local do erro. O desempenho pode ser afetado em uma compilação verificada devido ao código adicional que é executado.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Descrição"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Descrição do sistema operacional Windows. Algumas interfaces do usuário, por exemplo, aquelas que permitem a edição dessa descrição, limitam seu comprimento a 48 caracteres.

</dd> <dt>

**Fornecido**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o sistema operacional será distribuído entre vários nós de sistema de computador. Nesse caso, esses nós devem ser agrupados como um cluster.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**EncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nível de criptografia para transações seguras: 40 bits, 128 bits ou *n* bits.

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

**40** bits (0)


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

**128** bits (1)


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

**n** bits (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ForegroundApplicationBoost**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

O aumento na prioridade é fornecido ao aplicativo em primeiro plano. O aumento do aplicativo é implementado fornecendo a um aplicativo mais frações de tempo de execução (comprimentos do Quantum).

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (0)


</dt> <dd>

O sistema aumenta o comprimento do Quantum em 6.

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Mínimo** (1)


</dt> <dd>

O sistema aumenta o comprimento do Quantum em 12.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (2)


</dt> <dd>

O sistema aumenta o comprimento do Quantum em 18.

</dd> </dl>

</dd> <dt>

**FreePhysicalMemory**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Número, em kilobytes, da memória física atualmente não utilizada e disponível.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**FreeSpaceInPagingFiles**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Configurações de memória do sistema DMTF \| 1,4 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" quilobytes ")
</dt> </dl>

Número, em kilobytes, que pode ser mapeado para os arquivos de paginação do sistema operacional sem fazer com que nenhuma outra página seja trocada.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**FreeVirtualMemory**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Número, em kilobytes, de memória virtual atualmente não utilizado e disponível.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

O objeto de data foi instalado. Essa propriedade não requer um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LargeSystemCache**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propriedade é obsoleta e não tem suporte.

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Otimizar para aplicativos** (0)


</dt> <dd>

Otimize a memória para aplicativos.

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Otimizar para desempenho do sistema** (1)


</dt> <dd>

Otimize a memória para o desempenho do sistema.

</dd> </dl>

</dd> <dt>

**LastBootUpTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora em que o sistema operacional foi reiniciado pela última vez.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**LocalDateTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemDate "," MIF. \|Informações gerais do DMTF \| 1,6 ")
</dt> </dl>

Versão do sistema operacional da data e hora local.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**Localidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de suporte do idioma nacional win32api \| [](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| \_ ILANGUAGE")
</dt> </dl>

Identificador de idioma usado pelo sistema operacional. Um identificador de idioma é uma abreviação numérica internacional padrão para um país/região. Cada idioma tem um identificador de idioma exclusivo (LANGid), um valor de 16 bits que consiste em um identificador de idioma primário e um identificador de idioma secundário.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Nome do fabricante do sistema operacional. Para sistemas baseados no Windows, esse valor é "Microsoft Corporation".

</dd> <dt>

**MaxNumberOfProcesses**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemMaxProcesses ")
</dt> </dl>

Número máximo de contextos de processo aos quais o sistema operacional pode dar suporte. O valor padrão definido pelo provedor é 4294967295 (0xFFFFFFFF). Se não houver um máximo fixo, o valor deverá ser 0 (zero). Em sistemas que têm um máximo fixo, esse objeto pode ajudar a diagnosticar falhas que ocorrem quando o máximo é atingido — se for desconhecido, insira 4294967295 (0xFFFFFFFF).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**MaxProcessMemorySize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Número máximo, em quilobytes, de memória que pode ser alocado a um processo. Para sistemas operacionais sem memória virtual, normalmente esse valor é igual à quantidade total de memória física menos a memória usada pelo BIOS e pelo sistema operacional. Para alguns sistemas operacionais, esse valor pode ser infinito; nesse caso, 0 (zero) deve ser inserido. Em outros casos, esse valor pode ser uma constante, por exemplo, 2G ou 4G.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**MUILanguages**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Idiomas Multilingual User Interface Pack (MUI Pack) instalados no computador. Por exemplo, "en-US". Os idiomas MUI Pack são arquivos de recursos que podem ser instalados na versão em inglês do sistema operacional. Quando um MUI Pack é instalado, você pode alterar o idioma da interface do usuário para um dos idiomas com suporte 33.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Instância do sistema operacional em um sistema de computador.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfLicensedUsers**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de licenças de usuário para o sistema operacional. Se for ilimitado, insira 0 (zero). Se for desconhecido, digite-1.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfProcesses**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemProcesses ")
</dt> </dl>

Número de contextos de processo atualmente carregados ou em execução no sistema operacional.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfUsers**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrSystemNumUsers ")
</dt> </dl>

Número de sessões de usuário para as quais o sistema operacional está armazenando informações de estado no momento.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**OperatingSystemSKU**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Número de SKU (unidade de manutenção de estoque) do sistema operacional. Esses valores são os mesmos que o **Product \_ \** _ Constants definido em Winnt. h, que são usados com a função [_ *GetProductInfo* *](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .

A lista a seguir lista os possíveis valores de SKU.

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Produto \_ Indefinido** (0)


</dt> <dd>

Indefinido

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Produto \_ ULTIMATE** (1)


</dt> <dd>

Ultimate Edition, por exemplo, Windows Vista Ultimate.

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Produto \_ INÍCIO \_ básico** (2)


</dt> <dd>

Home Basic Edition

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Produto \_ HOME \_ Premium** (3)


</dt> <dd>

Home Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Produto \_ ENTERPRISE** (4)


</dt> <dd>

Enterprise Edition

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Produto \_ NEGÓCIOS** (6)


</dt> <dd>

Business Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Produto \_ \_Servidor Standard** (7)


</dt> <dd>

Windows Server Standard Edition (instalação da experiência desktop)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Produto \_ \_Servidor do datacenter** (8)


</dt> <dd>

Windows Server Datacenter Edition (instalação da experiência desktop)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Produto \_ \_Servidor do SMALLBUSINESS** (9)


</dt> <dd>

Edição do Small Business Server

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Produto \_ \_Servidor corporativo** (10)


</dt> <dd>

Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Produto \_ INÍCIO** (11)


</dt> <dd>

 Starter Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Produto \_ Datacenter \_ Server \_ Core** (12)


</dt> <dd>

Datacenter Server Core Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Produto \_ STANDARD \_ Server \_ Core** (13)


</dt> <dd>

Standard Server Core Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Produto \_ ENTERPRISE \_ Server \_ Core** (14)


</dt> <dd>

Enterprise Server Core Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Produto \_ \_Servidor Web** (17)


</dt> <dd>

Edição do servidor Web

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Produto \_ \_Servidor inicial** (19)


</dt> <dd>

Home Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Produto \_ \_ \_ Servidor do Storage Express** (20)


</dt> <dd>

Storage Express Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Produto \_ \_ \_ Servidor padrão de armazenamento** (21)


</dt> <dd>

Windows Storage Server Standard Edition (instalação da experiência desktop)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Produto \_ \_ \_ Servidor de grupo de trabalho de armazenamento** (22)


</dt> <dd>

Windows Storage Server Workgroup Edition (instalação da experiência desktop)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Produto \_ \_ \_ Servidor corporativo de armazenamento** (23)


</dt> <dd>

Armazenamento Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Produto \_ SERVIDOR \_ para o \_ SMALLBUSINESS** (24)


</dt> <dd>

Servidor para Small Business Edition

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Produto \_ \_Servidor do SMALLBUSINESS \_ Premium** (25)


</dt> <dd>

Small Business Server Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Produto \_ ENTERPRISE \_ N** (27)


</dt> <dd>

Windows Enterprise Edition

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Produto \_ ULTIMATE \_ N** (28)


</dt> <dd>

Windows Ultimate Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Produto \_ \_ \_ Núcleo do servidor Web** (29)


</dt> <dd>

Windows Server Web Server Edition (instalação Server Core)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Produto \_ STANDARD \_ Server \_ V** (36)


</dt> <dd>

Windows Server Standard Edition sem Hyper-V

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Produto \_ \_Servidor do datacenter \_ V** (37)


</dt> <dd>

Windows Server Datacenter Edition sem Hyper-V (instalação completa)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Produto \_ ENTERPRISE \_ Server \_ V** (38)


</dt> <dd>

Windows Server Enterprise Edition sem Hyper-V (instalação completa)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Produto \_ Datacenter \_ Server \_ Core \_ V** (39)


</dt> <dd>

Windows Server Datacenter Edition sem Hyper-V (instalação do Server Core)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Produto \_ STANDARD \_ Server \_ Core \_ V** (40)


</dt> <dd>

Windows Server Standard Edition sem Hyper-V (instalação Server Core)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Produto \_ ENTERPRISE \_ Server \_ Core \_ V** (41)


</dt> <dd>

Windows Server Enterprise Edition sem Hyper-V (instalação Server Core)

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Produto \_ HYPERV** (42)


</dt> <dd>

Microsoft Hyper-V Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Produto \_ STORAGE \_ Express \_ Server \_ Core** (43)


</dt> <dd>

Storage Server Express Edition (instalação Server Core)

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Produto \_ \_ \_ Server \_ Core do STORAGE Standard** (44)


</dt> <dd>

Storage Server Standard Edition (instalação Server Core)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Produto \_ \_ \_ \_ Núcleo do servidor de grupo de trabalho de armazenamento** (45)


</dt> <dd>

Storage Server Workgroup Edition (instalação Server Core)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Produto \_ ARMAZENAMENTO \_ Enterprise \_ Server \_ Core** (46)


</dt> <dd>

Storage Server Workgroup Edition (instalação Server Core)

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Produto \_ PROFESSIONAL** (48)


</dt> <dd>

Windows Professional

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Produto \_ \_ \_ Servidor da solução SB** (50)


</dt> <dd>

Windows Server Essentials (instalação da experiência desktop)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Produto \_ \_Servidor do SMALLBUSINESS \_ Premium \_ Core** (63)


</dt> <dd>

Small Business Server Premium (instalação do Server Core)

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Produto \_ Servidor de CLUSTER \_ \_ V** (64)


</dt> <dd>

Windows Compute Cluster Server sem Hyper-V

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Produto \_ \_ARM principal** (97)


</dt> <dd>

Windows RT

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>**Produto \_ NÚCLEO** (101)


</dt> <dd>

Página inicial do Windows

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Produto \_ \_WMC profissional** (103)


</dt> <dd>

Windows Professional com Media Center

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Produto \_ MOBILE \_ Core** (104)


</dt> <dd>

Windows Mobile

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Produto \_ IOTUAP** (123)


</dt> <dd>

Windows IoT (Internet das Coisas) Core

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Produto \_ Datacenter \_ nano \_ SERVER** (143)


</dt> <dd>

Windows Server Datacenter Edition (instalação do nano Server)

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Produto \_ \_ \_ Servidor nano STANDARD** (144)


</dt> <dd>

Windows Server Standard Edition (instalação do nano Server)

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Produto \_ Datacenter \_ WS \_ Server \_ Core** (147)


</dt> <dd>

Windows Server Datacenter Edition (instalação Server Core)

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Produto \_ STANDARD \_ WS \_ Server \_ Core** (148)


</dt> <dd>

Windows Server Standard Edition (instalação Server Core)

</dd> </dl>

</dd> <dt>

**Organização**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")
</dt> </dl>

Nome da empresa para o usuário registrado do sistema operacional.

Exemplo: "Microsoft Corporation"

</dd> <dt>

**OSArchitecture**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Arquitetura do sistema operacional, em vez do processador. Essa propriedade pode ser localizada.

Exemplo: 32 bits

</dd> <dt>

**OSLanguage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| localidade do painel de controle padrão do Win32Registry \\ \\ \\ \\ \| ")
</dt> </dl>

Versão de idioma do sistema operacional instalado. A lista a seguir lista os valores possíveis. Exemplo: 0x0807 (alemão, Suíça).

<dt>

1 (0x1)
</dt> <dd>

Árabe

</dd> <dt>

4 (0x4)
</dt> <dd>

Chinês (simplificado) – China

</dd> <dt>

9 (0x9)
</dt> <dd>

Inglês

</dd> <dt>

1025 (0x401)
</dt> <dd>

Árabe – Arábia Saudita

</dd> <dt>

1026 (0x402)
</dt> <dd>

Búlgaro

</dd> <dt>

1027 (0x403)
</dt> <dd>

Catalão

</dd> <dt>

1028 (0x404)
</dt> <dd>

Chinês (tradicional) – Taiwan

</dd> <dt>

1029 (0x405)
</dt> <dd>

Tcheco

</dd> <dt>

1030 (0x406)
</dt> <dd>

Dinamarquês

</dd> <dt>

1031 (0x407)
</dt> <dd>

Alemão – Alemanha

</dd> <dt>

1032 (0x408)
</dt> <dd>

Grego

</dd> <dt>

1033 (0x409)
</dt> <dd>

Inglês – Estados Unidos

</dd> <dt>

1034 (0x40A)
</dt> <dd>

Espanhol – classificação tradicional

</dd> <dt>

1035 (0x40B)
</dt> <dd>

Finlandês

</dd> <dt>

1036 (0x40C)
</dt> <dd>

Francês – França

</dd> <dt>

1037 (0x40D)
</dt> <dd>

Hebraico

</dd> <dt>

1038 (0x40E)
</dt> <dd>

Húngaro

</dd> <dt>

1039 (0x40F)
</dt> <dd>

Islandês

</dd> <dt>

1040 (0x410)
</dt> <dd>

Italiano – Itália

</dd> <dt>

1041 (0x411)
</dt> <dd>

Japonês

</dd> <dt>

1042 (0x412)
</dt> <dd>

Coreano

</dd> <dt>

1043 (0x413)
</dt> <dd>

Holandês – Holanda

</dd> <dt>

1044 (0x414)
</dt> <dd>

Norueguês – Bokmal

</dd> <dt>

1045 (0x415)
</dt> <dd>

Polonês

</dd> <dt>

1046 (0x416)
</dt> <dd>

Português – Brasil

</dd> <dt>

1047 (0x417)
</dt> <dd>

Rhaeto-Romanic

</dd> <dt>

1048 (0x418)
</dt> <dd>

Romeno

</dd> <dt>

1049 (0x419)
</dt> <dd>

Russo

</dd> <dt>

1050 (0x41A)
</dt> <dd>

Croata

</dd> <dt>

1051 (0x41B)
</dt> <dd>

Eslovaco

</dd> <dt>

1052 (0x41C)
</dt> <dd>

Albanês

</dd> <dt>

1053 (0x41D)
</dt> <dd>

Sueco

</dd> <dt>

1054 (0x41E)
</dt> <dd>

Tailandês

</dd> <dt>

1055 (0x41F)
</dt> <dd>

Turco

</dd> <dt>

1056 (0x420)
</dt> <dd>

Urdu

</dd> <dt>

1057 (0x421)
</dt> <dd>

Indonésio

</dd> <dt>

1058 (0x422)
</dt> <dd>

Ucraniano

</dd> <dt>

1059 (0x423)
</dt> <dd>

Bielorrusso

</dd> <dt>

1060 (0x424)
</dt> <dd>

Esloveno

</dd> <dt>

1061 (0x425)
</dt> <dd>

Estoniano

</dd> <dt>

1062 (0x426)
</dt> <dd>

Letão

</dd> <dt>

1063 (0x427)
</dt> <dd>

Lituano

</dd> <dt>

1065 (0x429)
</dt> <dd>

Persa

</dd> <dt>

1066 (0x42A)
</dt> <dd>

Vietnamita

</dd> <dt>

1069 (0x42D)
</dt> <dd>

Basco (País Basco)

</dd> <dt>

1070 (0x42E)
</dt> <dd>

Sérvio

</dd> <dt>

1071 (0x42F)
</dt> <dd>

Macedônio (nordeste da Macedônia)

</dd> <dt>

1072 (0x430)
</dt> <dd>

Sutu

</dd> <dt>

1073 (0x431)
</dt> <dd>

Xitsonga

</dd> <dt>

1074 (0x432)
</dt> <dd>

Tswana

</dd> <dt>

1076 (0x434)
</dt> <dd>

Xhosa

</dd> <dt>

1077 (0x435)
</dt> <dd>

Zulu

</dd> <dt>

1078 (0x436)
</dt> <dd>

Africâner

</dd> <dt>

1080 (0x438)
</dt> <dd>

Faroês

</dd> <dt>

1081 (0x439)
</dt> <dd>

Híndi

</dd> <dt>

1082 (0x43A)
</dt> <dd>

Maltês

</dd> <dt>

1084 (0x43C)
</dt> <dd>

Gaélico escocês (Reino Unido)

</dd> <dt>

1085 (0x43D)
</dt> <dd>

Iídiche

</dd> <dt>

1086 (0x43E)
</dt> <dd>

Malaio – Malásia

</dd> <dt>

2049 (0x801)
</dt> <dd>

Árabe – Iraque

</dd> <dt>

2052 (0x804)
</dt> <dd>

Chinês (simplificado) – PRC

</dd> <dt>

2055 (0x807)
</dt> <dd>

Alemão – Suíça

</dd> <dt>

2057 (0x809)
</dt> <dd>

Inglês – Reino Unido

</dd> <dt>

2058 (0x80A)
</dt> <dd>

Espanhol – México

</dd> <dt>

2060 (0x80C)
</dt> <dd>

Francês – Bélgica

</dd> <dt>

2064 (0x810)
</dt> <dd>

Italiano – Suíça

</dd> <dt>

2067 (0x813)
</dt> <dd>

Holandês – Bélgica

</dd> <dt>

2068 (0x814)
</dt> <dd>

Norueguês – Nynorsk

</dd> <dt>

2070 (0x816)
</dt> <dd>

Português – Portugal

</dd> <dt>

2072 (0x818)
</dt> <dd>

Romeno – Moldova

</dd> <dt>

2073 (0x819)
</dt> <dd>

Russo – Moldova

</dd> <dt>

2074 (0x81A)
</dt> <dd>

Sérvio – latino

</dd> <dt>

2077 (0x81D)
</dt> <dd>

Sueco – Finlândia

</dd> <dt>

3073 (0xC01)
</dt> <dd>

Árabe – Egito

</dd> <dt>

3076 (0xC04)
</dt> <dd>

Chinês (tradicional) – RAE de Hong Kong

</dd> <dt>

3079 (0xC07)
</dt> <dd>

Alemão – Áustria

</dd> <dt>

3081 (0xC09)
</dt> <dd>

Inglês – Austrália

</dd> <dt>

3082 (0xC0A)
</dt> <dd>

Espanhol – classificação internacional

</dd> <dt>

3084 (0xC0C)
</dt> <dd>

Francês – Canadá

</dd> <dt>

3098 (0xC1A)
</dt> <dd>

Sérvio – cirílico

</dd> <dt>

4097 (0x1001)
</dt> <dd>

Árabe – Líbia

</dd> <dt>

4100 (0x1004)
</dt> <dd>

Chinês (simplificado) – Cingapura

</dd> <dt>

4103 (0x1007)
</dt> <dd>

Alemão – Luxemburgo

</dd> <dt>

4105 (0x1009)
</dt> <dd>

Inglês – Canadá

</dd> <dt>

4106 (0x100A)
</dt> <dd>

Espanhol – Guatemala

</dd> <dt>

4108 (0x100C)
</dt> <dd>

Francês – Suíça

</dd> <dt>

5121 (0x1401)
</dt> <dd>

Árabe – Argélia

</dd> <dt>

5127 (0x1407)
</dt> <dd>

Alemão – Liechtenstein

</dd> <dt>

5129 (0x1409)
</dt> <dd>

Inglês – Nova Zelândia

</dd> <dt>

5130 (0x140A)
</dt> <dd>

Espanhol – Costa Rica

</dd> <dt>

5132 (0x140C)
</dt> <dd>

Francês – Luxemburgo

</dd> <dt>

6145 (0x1801)
</dt> <dd>

Árabe – Marrocos

</dd> <dt>

6153 (0x1809)
</dt> <dd>

Inglês – Irlanda

</dd> <dt>

6154 (0x180A)
</dt> <dd>

Espanhol – Panamá

</dd> <dt>

7169 (0x1C01)
</dt> <dd>

Árabe – Tunísia

</dd> <dt>

7177 (0x1C09)
</dt> <dd>

Inglês – África do Sul

</dd> <dt>

7178 (0x1C0A)
</dt> <dd>

Espanhol – República Dominicana

</dd> <dt>

8193 (0x2001)
</dt> <dd>

Árabe – Omã

</dd> <dt>

8201 (0x2009)
</dt> <dd>

Inglês – Jamaica

</dd> <dt>

8202 (0x200A)
</dt> <dd>

Espanhol – Venezuela

</dd> <dt>

9217 (0x2401)
</dt> <dd>

Árabe – Iêmen

</dd> <dt>

9226 (0x240A)
</dt> <dd>

Espanhol – Colômbia

</dd> <dt>

10241 (0x2801)
</dt> <dd>

Árabe – Síria

</dd> <dt>

10249 (0x2809)
</dt> <dd>

Inglês – Belize

</dd> <dt>

10250 (0x280A)
</dt> <dd>

Espanhol – Peru

</dd> <dt>

11265 (0x2C01)
</dt> <dd>

Árabe – Jordânia

</dd> <dt>

11273 (0x2C09)
</dt> <dd>

Inglês – Trinidad

</dd> <dt>

11274 (0x2C0A)
</dt> <dd>

Espanhol – Argentina

</dd> <dt>

12289 (0x3001)
</dt> <dd>

Árabe – Líbano

</dd> <dt>

12298 (0x300A)
</dt> <dd>

Espanhol – Equador

</dd> <dt>

13313 (0x3401)
</dt> <dd>

Árabe – Kuwait

</dd> <dt>

13322 (0x340A)
</dt> <dd>

Espanhol – Chile

</dd> <dt>

14337 (0x3801)
</dt> <dd>

Árabe – E.A.U.

</dd> <dt>

14346 (0x380A)
</dt> <dd>

Espanhol – Uruguai

</dd> <dt>

15361 (0x3C01)
</dt> <dd>

Árabe – Bahrein

</dd> <dt>

15370 (0x3C0A)
</dt> <dd>

Espanhol – Paraguai

</dd> <dt>

16385 (0x4001)
</dt> <dd>

Árabe – Catar

</dd> <dt>

16394 (0x400A)
</dt> <dd>

Espanhol – Bolívia

</dd> <dt>

17418 (0x440A)
</dt> <dd>

Espanhol – El Salvador

</dd> <dt>

18442 (0x480A)
</dt> <dd>

Espanhol – Honduras

</dd> <dt>

19466 (0x4C0A)
</dt> <dd>

Espanhol – Nicarágua

</dd> <dt>

20490 (0x500A)
</dt> <dd>

Espanhol – Porto Rico

</dd> </dl>

</dd> <dt>

**OSProductSuite**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ controloptions do \\ \\ \| ProductSuite"), [**bitvalues**](../wmisdk/standard-qualifiers.md) ("pequenas empresas", "Enterprise", "backoffice", "servidor de comunicação", "Terminal Server", "pequenas empresas (restritos)", "NT embutido", "Data Center")
</dt> </dl>

Inclusões de produto do sistema instaladas e licenciadas para o sistema operacional. Por exemplo, o valor de 146 (0x92) para **OSProductSuite** indica Enterprise, serviços de terminal e Data Center (bits um, quatro e sete conjuntos). A lista a seguir lista os possíveis valores.

<dt>

1 (0x1)
</dt> <dd>

O Microsoft Small Business Server já foi instalado, mas pode ter sido atualizado para outra versão do Windows.

</dd> <dt>

2 (0x2)
</dt> <dd>

O Windows Server 2008 Enterprise está instalado.

</dd> <dt>

4 (0x4)
</dt> <dd>

Os componentes do Windows backoffice estão instalados.

</dd> <dt>

8 (0x8)
</dt> <dd>

O servidor de comunicação está instalado.

</dd> <dt>

16 (0x10)
</dt> <dd>

Os serviços de terminal estão instalados.

</dd> <dt>

32 (0x20)
</dt> <dd>

O Microsoft Small Business Server é instalado com a licença de cliente restritiva.

</dd> <dt>

64 (0x40)
</dt> <dd>

O Windows Embedded está instalado.

</dd> <dt>

128 (0x80)
</dt> <dd>

Uma edição do datacenter está instalada.

</dd> <dt>

256 (0x100)
</dt> <dd>

Os serviços de terminal estão instalados, mas há suporte para apenas uma sessão interativa.

</dd> <dt>

512 (0x200)
</dt> <dd>

O Windows Home Edition está instalado.

</dd> <dt>

1024 (0x400)
</dt> <dd>

A edição do servidor Web está instalada.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

O Storage Server Edition está instalado.

</dd> <dt>

16384 (0x4000)
</dt> <dd>

O Compute Cluster Edition está instalado.

</dd> </dl>

</dd> <dt>

**OSType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**OtherTypeDescription**")
</dt> </dl>

Tipo do sistema operacional. A lista a seguir identifica os valores possíveis.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span id="MACOS"></span><span id="macos"></span>**MACOS** (2)


</dt> <dd>

MACROS

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>HP **(8** )


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span id="AIX"></span><span id="aix"></span>**AIX** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span id="MVS"></span><span id="mvs"></span>**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span id="OS400"></span><span id="os400"></span>**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**Win95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**Win98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WinCE** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span id="OSF"></span><span id="osf"></span>**Uso** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span id="IRIX"></span><span id="irix"></span>**IRIX** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)


</dt> <dd>

Solaris

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span id="LINUX"></span><span id="linux"></span>**Linux** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span id="OS9"></span><span id="os9"></span>**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span id="QNX"></span><span id="qnx"></span>**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span id="OS_390"></span><span id="os_390"></span>**Os/390** (60)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (61)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**TPF** (62)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Descrição adicional para a versão atual do sistema operacional.

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**PAEEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, as extensões de endereço físico (PAE) serão habilitadas pelo sistema operacional em execução nos processadores Intel. O PAE permite que os aplicativos resolvam mais de 4 GB de memória física. Quando o PAE está habilitado, o sistema operacional usa a conversão de endereços linear de três níveis em vez de dois níveis. Fornecer mais memória física a um aplicativo reduz a necessidade de trocar memória para o arquivo de paginação e aumenta o desempenho. Para habilitar, PAE, use a opção "/PAE" no arquivo de Boot.ini. Para obter mais informações sobre o recurso de extensão de endereço físico, consulte <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .

</dd> <dt>

**PlusProductID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus! ProductId ")
</dt> </dl>

Não há suporte.

</dd> <dt>

**PlusVersionNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus! VersionNumber ")
</dt> </dl>

Não há suporte.

</dd> <dt>

**PortableOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o sistema operacional foi inicializado a partir de um dispositivo USB externo. Se for true, o sistema operacional detectou que está inicializando em um dispositivo de armazenamento conectado localmente com suporte.

**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 8 e do Windows Server 2012.

</dd> <dt>

**Primário**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Especifica se este é o sistema operacional primário.

</dd> <dt>

**ProductType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Informações adicionais do sistema.

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

**Estação de trabalho** (1)


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

**Controlador de domínio** (2)


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Servidor** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumLength**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

Sem suporte

* * Windows Server 2008 e Windows Vista: * *

A propriedade **QuantumLength** define o número de tiques de relógio por Quantum. Um Quantum é uma unidade de tempo de execução que o Agendador tem permissão para fornecer a um aplicativo antes de alternar para outros aplicativos. Quando um thread executa um Quantum, o kernel o captura e o move para o final de uma fila para aplicativos com prioridades iguais. O comprimento real do quantum de um thread varia em diferentes plataformas do Windows. Somente para Windows NT/Windows 2000.

Os valores possíveis são.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

**Uma marca** (1)


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

**Duas tiques** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Quantumtype**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Sem suporte

* * Windows Server 2008 e Windows Vista: * *

A propriedade **quantumtype** especifica uma Quantum de comprimento fixo ou variável. O padrão do Windows é a Quantum de comprimento variável em que o aplicativo em primeiro plano tem uma Quantum mais longa do que os aplicativos em segundo plano. O padrão do Windows Server é a Quantum de comprimento fixo. Um Quantum é uma unidade de tempo de execução que o Agendador tem permissão para fornecer a um aplicativo antes de alternar para outro aplicativo. Quando um thread executa um Quantum, o kernel o captura e o move para o final de uma fila para aplicativos com prioridades iguais. O comprimento real do quantum de um thread varia em diferentes plataformas do Windows.

Os valores possíveis são.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Fixo** (1)


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

**Variável** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**RegisteredUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| RegisteredOwner")
</dt> </dl>

Nome do usuário registrado do sistema operacional.

Exemplo: "Ben Smith"

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")
</dt> </dl>

Número de identificação de série do produto do sistema operacional.

Exemplo: "10497-OEM-0031416-71674"

</dd> <dt>

**ServicePackMajorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")
</dt> </dl>

Número de versão principal do service pack instalado no sistema de computador. Se nenhum service pack tiver sido instalado, o valor será 0 (zero).

</dd> <dt>

**ServicePackMinorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")
</dt> </dl>

Número de versão secundária do service pack instalado no sistema de computador. Se nenhum service pack tiver sido instalado, o valor será 0 (zero).

</dd> <dt>

**SizeStoredInPagingFiles**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Configurações de memória do sistema DMTF \| 1,3 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" quilobytes ")
</dt> </dl>

O número total de quilobytes que podem ser armazenados nos arquivos de paginação do sistema operacional – 0 (zero) indica que não há arquivos de paginação. Lembre-se de que esse número não representa o tamanho físico real do arquivo de paginação no disco.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitada para inteligente, pode funcionar corretamente, mas prevê uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O status do serviço se aplica ao trabalho administrativo, como espelhamento de espelho de um disco, recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**SuiteMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**bitvalues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, backoffice Edition", "Windows Server, Communications Edition", "serviços de terminal da Microsoft", "Windows Server, Small Business Edition restrito", "Windows Embedded", "Windows Server, Datacenter Edition", "usuário único", "Windows Home Edition", "Windows Server, Web Edition")
</dt> </dl>

Sinalizadores de bits que identificam os pacotes de produtos disponíveis no sistema.

Por exemplo, para especificar pessoal e BackOffice, defina **SuiteMask** como `4 | 512` ou `516` .

<dt>

1
</dt> <dd>

Pequenas empresas

</dd> <dt>

2
</dt> <dd>

Enterprise

</dd> <dt>

4
</dt> <dd>

BackOffice

</dd> <dt>

8
</dt> <dd>

Comunicações

</dd> <dt>

16
</dt> <dd>

Serviços de Terminal

</dd> <dt>

32
</dt> <dd>

Pequena empresa restrita

</dd> <dt>

64
</dt> <dd>

Edição inserida

</dd> <dt>

128
</dt> <dd>

Datacenter Edition

</dd> <dt>

256
</dt> <dd>

Usuário único

</dd> <dt>

512
</dt> <dd>

Home Edition

</dd> <dt>

1024
</dt> <dd>

Edição do servidor Web

</dd> </dl>

</dd> <dt>

**SystemDevice**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de registro win32api \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| caminhos \| TargetDevice")
</dt> </dl>

Partição do disco físico na qual o sistema operacional está instalado.

</dd> <dt>

**SystemDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de informações do sistema win32api [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))
</dt> </dl>

Diretório do sistema operacional.

Exemplo: "C: \\ Windows \\ System32"

</dd> <dt>

**SystemDrive**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Letra da unidade de disco na qual o sistema operacional reside. Exemplo: "C:"

</dd> <dt>

**TotalSwapSpaceSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Espaço total de permuta em quilobytes. Esse valor pode ser **NULL** (não especificado) se o espaço de permuta não for diferenciado dos arquivos de paginação. No entanto, alguns sistemas operacionais distinguem esses conceitos. Por exemplo, no UNIX, processos inteiros podem ser trocados quando a lista de páginas gratuita cai e permanece abaixo de uma quantidade especificada.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**TotalVirtualMemorySize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Número, em kilobytes, de memória virtual. Por exemplo, isso pode ser calculado adicionando a quantidade de RAM total à quantidade de espaço de paginação, ou seja, adicionando a quantidade de memória ou agregada pelo sistema de computador à propriedade, **SizeStoredInPagingFiles**.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**TotalVisibleMemorySize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Quantidade total, em kilobytes, da memória física disponível para o sistema operacional. Esse valor não indica necessariamente a quantidade real de memória física, mas o que é relatado para o sistema operacional como disponível para ele.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).

Essa propriedade é herdada de sistema [**\_ operacional CIM**](cim-operatingsystem.md).

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| estruturas de informações do sistema \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")
</dt> </dl>

Número de versão do sistema operacional.

Exemplo: "4,0"

</dd> <dt>

**WindowsDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| funções de informações do sistema \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")
</dt> </dl>

Diretório do Windows do sistema operacional.

Exemplo: "C: \\ Windows"

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de sistema **\_ operacional Win32** é derivada do [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

Qualquer sistema operacional que pode ser instalado em um computador que possa executar um sistema operacional baseado no Windows é um descendente ou membro dessa classe. **Win32 \_ O OperatingSystem** é uma classe singleton. Para obter a instância única, use "@" para a chave.

Ao contrário da maioria das outras classes WMI geradas pelo MgmtClassGen, o método **OperatingSystem. CreateInstance**() retornará um objeto **OperatingSystem** em branco. Portanto, se você estiver usando C \# com MgmtClassGen, poderá usar o seguinte código:


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a>Exemplos

Você pode encontrar um exemplo de VBScript que obtém os dados do sistema operacional e do processador do [**Win32 \_ ComputerSystem**](win32-computersystem.md), do [**\_ processador Win32**](win32-processor.md)e do **\_ OperatingSystem do Win32** nos exemplos de tópico do [**\_ processador Win32**](win32-processor.md) .

A amostra [gerar relatórios do ambiente do Exchange usando](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) o PowerShell PowerShell na galeria do TechNet usa uma classe do sistema **\_ operacional Win32** como parte de um aplicativo maior para gerar relatórios de ambiente do Exchange.

A amostra [obter tempo de atividade do servidor usando WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) na galeria do TechNet usa a propriedade **LastBootupTime** para determinar quanto tempo o servidor esteve ativo. O exemplo também usa a opção Timeout para garantir que a chamada WMI não pare.

O exemplo de código VBScript do [recuperador de informações do WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) na galeria do TechNet usa a classe **Win32 \_ OperatingSystem** para recuperar informações do sistema operacional de vários computadores remotos.

O script a seguir obtém as instâncias de **\_ OperatingSystem do Win32** no namespace padrão "raiz \\ CIMv2" e, em seguida, exibe informações sobre o sistema operacional.


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



O exemplo de código do PowerShell a seguir exibe todas as informações operacionais sobre o sistema operacional atual.


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sistema \_ operacional CIM**](cim-operatingsystem.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[Tarefas do WMI: sistemas operacionais](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[Tarefas do WMI: hardware do computador](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[Tarefas do WMI: gerenciamento de desktop](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
