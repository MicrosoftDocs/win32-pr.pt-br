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
# <a name="win32_computersystem-class"></a>Classe de ComputerSystem do Win32 \_

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ ComputerSystem do Win32** representa um sistema de computador executando o Windows.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe **Win32 \_ ComputerSystem** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ ComputerSystem** tem esses métodos.



| Método                                                                                          | Descrição                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | Adiciona um sistema de computador a um domínio ou grupo de trabalho.<br/>                                                                                                                                                                                   |
| [**Renomear**](rename-method-in-class-win32-computersystem.md)                                   | Renomeia um computador local.<br/>                                                                                                                                                                                                          |
| **SetPowerState**                                                                               | Não implementado. Para obter mais informações sobre como implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).<br/> |
| [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | Remove um sistema de computador de um domínio ou grupo de trabalho.<br/>                                                                                                                                                                              |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ComputerSystem** tem essas propriedades.

<dl> <dt>

**AdminPasswordStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| configurações de segurança de hardware \| AdminPasswordStatus")
</dt> </dl>

Configurações de segurança de hardware do sistema para status da senha do administrador.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Não implementado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticManagedPagefile**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Se **for true**, o sistema gerenciará o arquivo de paginação.

</dd> <dt>

**AutomaticResetBootOption**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| reboot")
</dt> </dl>

Se for **true**, a opção de redefinição automática será habilitada.

</dd> <dt>

**AutomaticResetCapability**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Se for **true**, a redefinição automática será habilitada.

</dd> <dt>

**BootOptionOnLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| opção SMBIOS tipo 23 \| recursos \| de inicialização no limite")
</dt> </dl>

O limite da opção de inicialização está ativado. Identifica a ação do sistema quando o valor de **ResetLimit** é atingido.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Sistema operacional** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Utilitários do sistema** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**Não reinicializar** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootOptionOnWatchDog**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("opção de inicialização de recursos do SMBIOS \| tipo 23 \| \| ")
</dt> </dl>

O tipo de ação de reinicialização após a hora no temporizador do Watchdog é decorrido.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Sistema operacional** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Utilitários do sistema** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**Não reinicializar** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootROMSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Se for **true**, indicará se há suporte para uma ROM de inicialização.

</dd> <dt>

**BootStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 32 \| status de inicialização das informações de inicialização do sistema \| ")
</dt> </dl>

Status e campos de dados adicionais que identificam o status de inicialização.

Esse valor é proveniente do membro **status de inicialização** da estrutura de informações de inicialização do **sistema** nas informações do SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.

</dd> <dt>

**Inicializaçãostate**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT")
</dt> </dl>

O sistema foi iniciado. A inicialização segura de falhas ignora os arquivos de inicialização do usuário também chamados de inicialização segura.

A lista a seguir contém os valores necessários:

<dl> <dd>"Inicialização normal"</dd> <dd>"Inicialização segura de falhas"</dd> <dd>"Prova de falhas com inicialização de rede"</dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

**Inicialização normal** ("inicialização normal")


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

**Inicialização segura** ("inicialização com falha segura")


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

**À prova de falhas com inicialização de rede** ("segurança-segura com inicialização de rede")


</dt> <dd></dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrição do objeto de uma cadeia de caracteres de uma linha.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ChassisBootupState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("estado de inicialização do SMBIOS \| tipo 3 \| ")
</dt> </dl>

Inicialize o estado do chassi.

Esse valor é proveniente do membro de **estado de inicialização** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Seguro** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Aviso** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**Não recuperável** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**ChassisSKUNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| número de SKU do chassi do tipo SMBIOS 3 \| \| ")
</dt> </dl>

O número de SKU do gabinete ou compartimento como uma cadeia de caracteres.

Esse valor é proveniente do membro **número da SKU** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome da primeira classe concreta na cadeia de herança de uma instância. Você pode usar essa propriedade com outras propriedades da classe para identificar todas as instâncias da classe e suas subclasses.

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de tempo win32api diferença de \| [**\_ \_ informações de fuso horário**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")
</dt> </dl>

Quantidade de tempo que o sistema de computador unitário é deslocado do UTC (tempo Universal Coordenado).

</dd> <dt>

**DaylightInEffect**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")
</dt> </dl>

Se for **true**, o modo de economia de verão será on.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| GetComputerNameEx devia \| ComputerNameDnsHostname")
</dt> </dl>

Nome do computador local de acordo com o DNS (servidor de nomes de domínio).

</dd> <dt>

**Domínio**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de gerenciamento de rede Win32API \| [**WKSTA \_ info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ langroup")
</dt> </dl>

Nome do domínio ao qual um computador pertence.

> [!Note]  
> Se o computador não fizer parte de um domínio, o nome do grupo de trabalho será retornado.

 

</dd> <dt>

**DomainRole**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Directory Service (DS) estruturas \| [**DSROLE \_ Primary \_ Domain \_ info \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ Machine \_ role**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| MachineRole")
</dt> </dl>

Função de um computador em um grupo de trabalho de domínio atribuído. Um grupo de trabalho de domínio é uma coleção de computadores na mesma rede. Por exemplo, uma propriedade **DomainRole** pode mostrar que um computador é uma estação de trabalho membro.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

**Estação de trabalho autônoma** (0)


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

**Estação de trabalho membro** (1)


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

**Servidor autônomo** (2)


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

**Servidor membro** (3)


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

**Controlador de domínio de backup** (4)


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

**Controlador de domínio primário** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**EnableDaylightSavingsTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Habilita o horário de Verão (DST) em um computador. Um valor **true** indica que a hora do sistema muda para uma hora à frente ou atrás quando o DST inicia ou termina. Um valor **false** indica que a hora do sistema não muda para uma hora à frente ou atrás quando o DST inicia ou termina. Um valor **NULL** indica que o status do DST é desconhecido em um sistema.

</dd> <dt>

**FrontPanelResetStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| configurações de segurança de hardware \| FrontPanelResetStatus")
</dt> </dl>

A tabela a seguir lista as configurações de segurança de hardware para o botão redefinir em um computador.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Não implementado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HypervisorPresent**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Se for **true**, um hipervisor estará presente.

**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 8 e do Windows Server 2012.

</dd> <dt>

**InfraredSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Se **for true**, uma porta de infravermelho (ir) existirá em um sistema de computador.

</dd> <dt>

**InitialLoadInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados necessários para localizar o dispositivo de carregamento inicial ou o serviço de inicialização para solicitar que o sistema operacional seja inicializado.

Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

**Windows Server 2008 R2:** Essa propriedade está disponível, mas vazia.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")
</dt> </dl>

O objeto está instalado. Um objeto não precisa de um valor para indicar que ele está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**KeyboardPasswordStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| configurações de segurança de hardware \| KeyboardPasswordStatus")
</dt> </dl>

Configurações de segurança de hardware do sistema para status da senha do teclado.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Não implementado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastLoadInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Entrada de matriz da propriedade **InitialLoadInfo** que contém os dados para iniciar o sistema operacional carregado.

Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("fabricante de informações do sistema do SMBIOS \| tipo 1 \| \| ")
</dt> </dl>

Nome do fabricante de um computador.

Exemplo: Adventure Works

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 1 \| nome do produto informações do sistema \| ")
</dt> </dl>

Nome do produto que um fabricante fornece a um computador. Essa propriedade deve ter um valor.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Chave de uma instância do [**\_ sistema CIM**](cim-system.md) em um ambiente corporativo.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor do **nome** do sistema de computador que é gerado automaticamente. O objeto [**CIM \_ ComputerSystem**](cim-computersystem.md) e seus derivados são objetos de nível superior do modelo CIM (CIM). Eles fornecem o escopo para vários componentes. São necessárias chaves de [**\_ sistema CIM**](cim-system.md) exclusivas, mas você pode definir uma heurística para criar o nome de sistema de sistemas **CIM \_** que gera o mesmo nome e é independente do protocolo de descoberta. Isso impede problemas de inventário e gerenciamento quando o mesmo ativo ou entidade é descoberto várias vezes, mas não pode ser resolvido para um objeto. É recomendável usar um heurístico, mas não obrigatório.

A heurística é descrita na especificação de modelo comum do CIM V2 e pressupõe que as regras documentadas sejam usadas para determinar e atribuir um nome. A lista de valores **NameFormat** define o pedido para atribuir um nome de sistema de computador. Várias regras são mapeadas para o mesmo valor.

O valor do [**\_ nome de sistema CIM**](cim-computersystem.md) que é calculado usando o heurístico é o valor de chave do sistema. No entanto, use aliases para atribuir um nome diferente para o **CIM \_ ComputerSystem**, que pode ser mais exclusivo para sua empresa.

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

Os valores incluem o seguinte:

<dt>

<span id="IP"></span><span id="ip"></span>

**IP** ("IP")


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

**Discar** ("discar")


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

**HID** ("HID")


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

**NWA** ("NWA")


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

**Hwa** ("Hwa")


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** ("X25")


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**ISDN** ("ISDN")


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** ("IPX")


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

**DCC** ("DCC")


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

**ICD** ("ICD")


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

**E. 164** ("E. 164")


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** ("SNA")


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**OID/OSI** ("OID/OSI")


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** ("outro")


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkServerModeEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management estruturas \| [**Server \_ info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ Type \| VA \_ Type \_ Server")
</dt> </dl>

Se for **true**, o modo de servidor de rede será habilitado.

</dd> <dt>

**NumberOfLogicalProcessors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Número de processadores lógicos disponíveis no computador.

Você pode usar **NumberOfLogicalProcessors** e **NumberOfProcessors** para determinar se o computador está hyperthreading. Para obter mais informações, consulte Comentários.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| informações do sistema de estruturas de informação do sistema \| [**\_**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors")
</dt> </dl>

Número de processadores físicos atualmente disponíveis em um sistema. Este é o número de processadores habilitados para um sistema, que não inclui os processadores desabilitados. Se um sistema de computador tiver dois processadores físicos contendo dois processadores lógicos, o valor de **NumberOfProcessors** será 2 e **NumberOfLogicalProcessors** será 4. Os processadores podem ser de vários núcleos ou podem ser processadores hyperthreading. Para obter mais informações, consulte Comentários.

</dd> <dt>

**OEMLogoBitmap**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Lista de dados para um bitmap criado pelo OEM (fabricante original do equipamento).

</dd> <dt>

**OEMStringArray**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 11 \| OEM Strings")
</dt> </dl>

Lista de cadeias de caracteres de forma livre que um OEM define. Por exemplo, um OEM define os números de peça para documentos de referência do sistema, informações de contato do fabricante e assim por diante.

</dd> <dt>

**PartOfDomain**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Se for **true**, o computador será parte de um domínio. Se o valor for **NULL**, o computador não está em um domínio ou o status é desconhecido. Se você remover o computador de um domínio, o valor se tornará **falso**.

</dd> <dt>

**PauseAfterReset**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 23 \| timeout"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")
</dt> </dl>

Tempo de espera antes que uma reinicialização seja iniciada em milissegundos. Ele é usado após um ciclo de energia do sistema, redefinição do sistema local ou remoto e redefinição automática do sistema. Um valor de 1 (menos um) indica que o valor de pausa é desconhecido.

**Windows Vista:** Esta propriedade pode retornar um número desconhecido.

</dd> <dt>

**PCSystemType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Tipo de computador em uso, como laptop, desktop ou Tablet.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Não especificado** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Área de trabalho** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Móvel** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Estação de trabalho** (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Servidor corporativo** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Servidor Soho** (5)


</dt> <dd>

Servidor de pequena empresa e escritório doméstico (SOHO)

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**PC de dispositivo** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Servidor de desempenho** (7)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**PCSystemTypeEx**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Tipo de computador em uso, como laptop, desktop ou Tablet.

**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não tem suporte antes do Windows 8.1 e do Windows Server 2012 R2.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

**Não especificado** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Área de trabalho** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

**Móvel** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

**Estação de trabalho** (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

**Servidor corporativo** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

**Servidor Soho** (5)


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

**PC de dispositivo** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

**Servidor de desempenho** (7)


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

**Slate** (8)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Máximo** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controles de energia do sistema DMTF \| 1,2 ")
</dt> </dl>

Matriz de recursos específicos relacionados à energia de um dispositivo lógico.

Essa propriedade é herdada **de \_ LogicalDevice CIM**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)


</dt> <dd>

Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)


</dt> <dd>

O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)


</dt> <dd>

Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) . Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado. Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)


</dt> <dd>

O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)


</dt> <dd>

Tempo Power-On com suporte

O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o dispositivo poderá ser gerenciado por energia, por exemplo, um dispositivo pode ser colocado no modo de suspensão e assim por diante. Essa propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, mas indica que o dispositivo lógico é capaz de gerenciamento de energia.

Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

</dd> <dt>

**PowerOnPasswordStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| configurações de segurança de hardware \| PowerOnPasswordStatus")
</dt> </dl>

Configurações de segurança de hardware do sistema para Power-On status da senha.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Não implementado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado de energia atual de um computador e seu sistema operacional associado. Os Estados de economia de energia têm os seguintes valores: valor 4 (desconhecido) indica que o sistema é conhecido em um modo de economia de energia, mas seu status exato nesse modo é desconhecido; 2 (o modo de baixa energia) indica que o sistema está em um estado de economia de energia, mas ainda funcionando e pode exibir o desempenho degradado; 3 (em espera) indica que o sistema não está funcionando, mas pode ser levado a uma potência completa rapidamente; e 7 (aviso) indica que o sistema de computador está em um estado de aviso e um modo de economia de energia.

Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Energia completa** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (6** )


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (7)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save-hibernar** (8)


</dt> <dd>

Power Save Hibernate.

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Economia **de energia – soft off** (9)


</dt> <dd>

Power Save soft off.

</dd> </dl>

</dd> <dt>

**PowerSupplyState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("compartimento do sistema do SMBIOS \| tipo 3 \| ou \| estado da fonte de energia do chassi")
</dt> </dl>

Estado da fonte de energia ou suprimentos quando a última inicialização.

Esse valor é proveniente do membro do **estado da fonte de energia** do compartimento do **sistema ou** da estrutura do chassi nas informações do SMBIOS.

A lista a seguir identifica os valores para essa propriedade.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Seguro** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Não recuperável** (6)


</dt> <dd>

Não recuperável

</dd> </dl>

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Informações de contato do proprietário do sistema primário, por exemplo, número de telefone, endereço de email e assim por diante.

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome do proprietário do sistema primário.

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Segurança de hardware do sistema DMTF \| 1,4 ")
</dt> </dl>

Se habilitado, o valor é 4 e o sistema de computador unitário pode ser redefinido usando os botões potência e redefinição. Se desabilitado, o valor será 3 e uma redefinição não será permitida.

Essa propriedade é herdada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Não implementado** (5)


</dt> <dd>

Não recuperável

</dd> </dl>

</dd> <dt>

**ResetCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| redefinetion Count redefinence \| ")
</dt> </dl>

Número de redefinições automáticas desde a última redefinição. Um valor de 1 (menos um) indica que a contagem é desconhecida.

</dd> <dt>

**ResetLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 23 limite de redefinição do \| sistema \| ")
</dt> </dl>

Número de vezes consecutivas em que uma reinicialização do sistema é tentada. Um valor de 1 (menos um) indica que o limite é desconhecido.

</dd> <dt>

**Funções**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Lista que especifica as funções de um sistema no ambiente de tecnologia da informação.

Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Status atual de um objeto.

Por Win32_ComputerSystem, o status é sempre "OK".

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dl>

</dd> <dt>

**SupportContactDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| support Information")
</dt> </dl>

Lista das informações de contato de suporte para o sistema operacional Windows.

</dd> <dt>

**SystemFamily**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| família de informações do sistema SMBIOS tipo 1 \| \| ")
</dt> </dl>

A família à qual pertence um computador específico. Uma família refere-se a um conjunto de computadores que são semelhantes, mas não idênticos, de um ponto de vista de hardware ou software.

Esse valor é proveniente do membro da **família** da estrutura de **informações do sistema** nas informações do SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.

</dd> <dt>

**SystemSKUNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 1 \| número de SKU de informações do sistema \| ")
</dt> </dl>

Identifica uma configuração de computador específica para venda. Às vezes, ele também é chamado de ID do produto ou número da ordem de compra.

Esse valor é proveniente do membro **número da SKU** da estrutura de informações do **sistema** nas informações do SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.

</dd> <dt>

**SystemStartupDelay**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilégios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| tempo limite do carregador de inicialização \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")
</dt> </dl>

O **SystemStartupDelay** não está mais disponível para uso porque Boot.ini não é usado para configurar a inicialização do sistema. Em vez disso, use as [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornecidas pelo provedor WMI de dados de configuração da inicialização (BCD) ou o comando **bcdedit** .

</dd> <dt>

**SystemStartupOptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilégios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| Operating Systems")
</dt> </dl>

O **SystemStartupOptions** não está mais disponível para uso porque Boot.ini não é usado para configurar a inicialização do sistema. Em vez disso, use as [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornecidas pelo provedor WMI de dados de configuração da inicialização (BCD) ou o comando **bcdedit** .

</dd> <dt>

**SystemStartupSetting**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilégios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

O **SystemStartupSetting** não está mais disponível para uso porque Boot.ini não é usado para configurar a inicialização do sistema. Em vez disso, use as [classes BCD](/previous-versions/windows/desktop/bcd/bcd-classes) fornecidas pelo provedor WMI de dados de configuração da inicialização (BCD) ou o comando **bcdedit** .

</dd> <dt>

**SystemType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| informações do sistema de estruturas de informação do sistema \| [**\_**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture")
</dt> </dl>

Sistema em execução no computador baseado no Windows. Essa propriedade deve ter um valor.

A lista a seguir identifica alguns dos valores possíveis para essa propriedade.

<dl> <dd>"PC baseado em x64"</dd> <dd>"PC baseado em x86"</dd> <dd>"PC baseado em MIPS"</dd> <dd>"PC baseado em Alpha"</dd> <dd>"Power PC"</dd> <dd>"SH-x PC"</dd> <dd>"PC StrongARM"</dd> <dd>"PC Intel de 64 bits"</dd> <dd>"PC Alpha de 64 bits"</dd> <dd>Conhecidos</dd> <dd>"Computador x86-Nec98"</dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

**PC baseado em x86** ("PC baseado em x86")


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

**PC baseado em MIPS** ("PC baseado em MIPS")


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

**PC baseado em Alpha** ("PC baseado em Alpha")


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

**Power PC** ("Power PC")


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

**Sh-x PC** ("sh-x PC")


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

**STRONGARM PC** ("StrongARM PC")


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

**PC Intel de 64 bits** ("PC intel de 64 bits")


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

**PC baseado em x64** ("PC baseado em x64")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

**Computador x86-Nec98** ("x86-Nec98 PC")


</dt> <dd></dd> </dl>

</dd> <dt>

**Termalstate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("compartimento do sistema do SMBIOS \| tipo 3 \| ou \| estado térmico do chassi")
</dt> </dl>

Estado térmico do sistema quando a última inicialização.

Esse valor é proveniente do membro de **estado térmico** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Seguro** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Aviso** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**Não recuperável** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**TotalPhysicalMemory**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de gerenciamento de memória win32api \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamanho total da memória física. Lembre-se de que, em algumas circunstâncias, essa propriedade pode não retornar um valor preciso para a memória física. Por exemplo, não será preciso se o BIOS estiver usando parte da memória física. Para um valor preciso, use a propriedade **Capacity** no [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) em vez disso.

Exemplo: 67108864

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| funções de informações do sistema \ \| [**username**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")
</dt> </dl>

Nome de um usuário que está conectado no momento. Essa propriedade deve ter um valor. Em uma sessão de serviços de terminal, **username** retorna o nome do usuário que fez logon no console, não o usuário conectado durante a sessão de serviço de terminal.

Exemplo: jeffsmith

</dd> <dt>

**Ativartype**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| tipo de ativação de informações do sistema SMBIOS tipo 1 \| ")
</dt> </dl>

Evento que faz com que o sistema ligue.

Esse valor é proveniente do membro do **tipo de ativação** da estrutura de **informações do sistema** nas informações do SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

**Temporizador APM** (3)


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

**Modem Ring** (4)


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

**LAN remota** (5)


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

**Botão de energia** (6)


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

**PME \# de PCI** 7


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

**Energia CA restaurada** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Grupo de trabalho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Nome do grupo de trabalho deste computador. Se o valor da propriedade **PartOfDomain** for **false**, o nome do grupo de trabalho será retornado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para determinar o número total de instâncias de processador associadas a um objeto de sistema de computador, use a classe de associação [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md) .

Uma instância de **\_ ComputerSystem do Win32** que tem vários processadores físicos tem várias instâncias de [**\_ processador Win32**](win32-processor.md) associadas a ele. Se o valor de **NumberOfLogicalProcessors** for maior que o valor de **NumberOfProcessors** , o sistema de computador será um sistema de vários núcleos ou terá um ou mais processadores habilitados para hyperthreading. Para obter mais informações, consulte a seção Propriedades e comentários do **NumberOfLogicalProcessors** e do **NumberOfCores** no **\_ processador Win32**.

A classe de **\_ ComputerSystem do Win32** é derivada do [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

## <a name="examples"></a>Exemplos

O [exemplo de código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) do centro de scripts a seguir usa o **\_ sistema** de computadores Win32 para recuperar informações de vários sistemas de computador e EXIBI-los em uma GUI.

Você pode encontrar um exemplo de script que obtém os dados do sistema operacional e do processador do **Win32 \_ ComputerSystem**, do [**\_ processador Win32**](win32-processor.md)e do [**\_ OperatingSystem do Win32**](win32-operatingsystem.md) nos exemplos de tópico do [**\_ processador Win32**](win32-processor.md) .

O exemplo de VBScript a seguir descreve como recuperar o nome de domínio do computador local de instâncias do **Win32 \_ ComputerSystem**.


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



O exemplo do Perl a seguir descreve como recuperar o nome do computador local de instâncias do **Win32 \_ ComputerSystem**.


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



O exemplo do Perl a seguir descreve como recuperar o nome de domínio DNS do computador local de instâncias do **Win32 \_ ComputerSystem**.


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

[**\_UNITARYCOMPUTERSYSTEM CIM**](cim-unitarycomputersystem.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Tarefas do WMI: contas e domínios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Tarefas do WMI: hardware do computador](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[Tarefas do WMI: gerenciamento de desktop](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

