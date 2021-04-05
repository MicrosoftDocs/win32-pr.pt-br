---
description: A \_ classe CIM ModifySettingAction representa as informações para modificar um arquivo de configuração específico, para uma entrada específica, com um valor específico.
ms.assetid: 6d22bc11-f798-4634-8688-797d4a4a4bee
ms.tgt_platform: multiple
title: Classe CIM_ModifySettingAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction
- CIM_ModifySettingAction.ActionID
- CIM_ModifySettingAction.Caption
- CIM_ModifySettingAction.Description
- CIM_ModifySettingAction.Direction
- CIM_ModifySettingAction.Name
- CIM_ModifySettingAction.SoftwareElementID
- CIM_ModifySettingAction.SoftwareElementState
- CIM_ModifySettingAction.TargetOperatingSystem
- CIM_ModifySettingAction.Version
- CIM_ModifySettingAction.ActionType
- CIM_ModifySettingAction.EntryName
- CIM_ModifySettingAction.EntryValue
- CIM_ModifySettingAction.FileName
- CIM_ModifySettingAction.SectionKey
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 450e73eaa6f405e47d79cbf3840932e0f106a4b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646447"
---
# <a name="cim_modifysettingaction-class"></a>\_Classe CIM ModifySettingAction

A classe **CIM \_ ModifySettingAction** representa as informações para modificar um arquivo de configuração específico, para uma entrada específica, com um valor específico.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{ECDE0B90-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ModifySettingAction : CIM_Action
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
  uint16 ActionType;
  string EntryName;
  string EntryValue;
  string FileName;
  string SectionKey;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ModifySettingAction** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **CIM \_ ModifySettingAction** tem esses métodos.



| Método                                                           | Descrição                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------|
| [**Chame**](invoke-method-in-class-cim-modifysettingaction.md) | Executa uma ação específica. Não implementado pelo WMI.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **CIM \_ ModifySettingAction** tem essas propriedades.

<dl> <dt>

**ActionID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador exclusivo atribuído a uma ação específica para um elemento de software.

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

</dd> <dt>

**ActionType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de ação a ser executada na entrada de configuração especificada. As adições são consideradas diferenciadas entre maiúsculas e minúsculas; no entanto, supõe-se que as remoções não diferenciam maiúsculas de minúsculas.

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Criar** (0)


</dt> <dd>

Cria a entrada especificada.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Excluir** (1)


</dt> <dd>

Exclui a entrada especificada.

</dd> <dt>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Acrescentar** (2)


</dt> <dd>

Anexa ao final da entrada especificada.

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remover** (3)


</dt> <dd>

Remove o valor da entrada especificada.

</dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição textual do objeto.

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do objeto.

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

</dd> <dt>

**Direção**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se um objeto [**de \_ ação CIM**](cim-action.md) específico faz parte de uma sequência de ações para fazer a transição do elemento de software atual para seu próximo estado, como "instalar" ou para remover o elemento de software atual, como "Desinstalar".

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

**Instalar** (0)


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

**Desinstalar** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Entryname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome da entrada a ser modificada.

</dd> <dt>

**Entryvalue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor a adicionar, acrescentar ou substituir a configuração especificada.

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)
</dt> </dl>

Nome do arquivo da entrada do arquivo de configuração a ser modificada.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identifica o elemento de software.

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

</dd> <dt>

**SectionKey**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Chave da seção da entrada de configuração a ser modificada.

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador para o elemento de software.

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Estado de um elemento de software.

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)


</dt> <dd>

Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)


</dt> <dd>

Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)


</dt> <dd>

Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)


</dt> <dd>

Descreve os detalhes necessários para monitorar e operar em um elemento inicial.

</dd> </dl>

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")
</dt> </dl>

Sistema operacional de destino do elemento de software proprietário.

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

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

Mac OS

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


</dt> <dd>

Abrir VMS

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>HP **(8** )


</dt> <dd>

HP-UX

</dd> <dt>

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


</dt> <dd>

VM (máquina virtual) da Microsoft para Java

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)


</dt> <dd>

Windows 3. x

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**Win95** (16)


</dt> <dd>

Windows 95

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**Win98** (17)


</dt> <dd>

Windows 98

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)


</dt> <dd>

Windows NT

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WinCE** (19)


</dt> <dd>

Windows CE

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)


</dt> <dd>

NCR 3000

</dd> <dt>

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


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)


</dt> <dd>

Uma série

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)


</dt> <dd>

NSK tandem

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)


</dt> <dd>

NT em tandem

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)


</dt> <dd>

BS2000/OSD

</dd> <dt>

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


</dt> <dd>

BSD UNIX

</dd> <dt>

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


</dt> <dd>

Mac OS 9

</dd> <dt>

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


</dt> <dd>

Ser so

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)


</dt> <dd>

Sistema operacional Palm

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (60)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**TPF** (61)


</dt> <dd></dd> </dl>

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")
</dt> </dl>

Versão da operação.

A versão da operação deve estar em um dos seguintes formatos:

-   <major>.<minor>.<revision>
-   <major>.<minor><letter><revision>

Esta propriedade é herdada [**da \_ ação CIM**](cim-action.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ ModifySettingAction** é derivada da [**\_ ação CIM**](cim-action.md).

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

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

[**Ação de CIM \_**](cim-action.md)
</dt> </dl>

 

