---
description: Representa as configurações específicas de virtualização para uma máquina virtual.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Classe Msvm_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fb57c7b96a6e2cd1839f4d830074bb69d742aef688325a37d61b67589d026436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147889"
---
# <a name="msvm_virtualsystemsettingdata-class"></a>\_Classe Msvm VirtualSystemSettingData

Representa as configurações específicas de virtualização para uma máquina virtual.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemSettingData** tem essas propriedades.

<dl> <dt>

**AdditionalRecoveryInformation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Quaisquer informações adicionais fornecidas para a ação de recuperação. O significado dessa propriedade é definido pela ação em **AutomaticRecoveryAction**. Se **AutomaticRecoveryAction** for 0 ("None") ou 1 ("restart"), esse valor será **NULL**. Se **AutomaticRecoveryAction** for 2 ("reverter para instantâneo"), esse será o caminho do objeto para um instantâneo que deve ser aplicado em caso de falha do processo de trabalho da máquina virtual.

</dd> <dt>

**AllowFullSCSICommandSet**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

**True** se os comandos SCSI do sistema operacional convidado forem passados para discos de passagem; caso contrário, **false**. Se **for verdadeiro**, os comandos SCSI emitidos pelo sistema operacional convidado para discos de passagem não serão filtrados. Recomendamos que a filtragem de SCSI permaneça habilitada para implantações de produção.

</dd> <dt>

**AllowReducedFcRedundancy**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se a migração dinâmica de uma máquina virtual configurada com um adaptador de Fibre Channel virtual é permitida para um computador de destino que pode não ter caminhos ou não reduzidos para os dispositivos de Fibre Channel de destino. Essa propriedade deve ser limpa após uma migração ao vivo.



| Valor                                                                            | Significado                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>Falso</dt> </dl> | A máquina virtual não pode ser migrada ao vivo para um computador de destino que pode não ter um ou menos caminhos para os dispositivos de Fibre Channel de destino.<br/>                                                                                                     |
| <dl> <dt>True</dt> </dl>  | A máquina virtual pode ser migrada ao vivo para um computador de destino que pode não ter um ou menos caminhos para os dispositivos de Fibre Channel de destino. O sistema operacional convidado pode perder conectividade com o armazenamento e pode se comportar de maneira imprevisível.<br/> |



 

</dd> <dt>

**Arquitetura**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A arquitetura deste sistema.

> [!Note]  
> adicionado em Windows 10, versão 1709.

 

<dt>

<span id="x64"></span><span id="X64"></span>

**x64** ()


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

**arm64** ()


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Identifica a ação a ser executada na VM, quando ocorre um erro crítico, como o armazenamento desconectado.

> [!Note]  
> adicionado em Windows 10 e Windows Server 2016.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (0)


</dt> <dd>

Nenhuma ação específica será tomada para condições de erro críticas.

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pausar retomar** (1)


</dt> <dd>

Faz com que a VM seja pausada e retomada automaticamente quando a condição de erro crítico for resolvida.

</dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorActionTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**subtipo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Interval")
</dt> </dl>

Identifica a duração máxima para a qual o **AutomaticCriticalErrorAction** será executado para resolver o erro crítico. Isso é aplicável somente quando o valor da propriedade **AutomaticCriticalErrorAction** não é 0 (None). Quando o tempo limite expirar, a VM será desligada. O valor será arredondado para o minuto mais próximo. Um valor de 0 implica que a VM deve ser desligada imediatamente quando encontra uma condição de erro crítica.

> [!Note]  
> adicionado em Windows 10 e Windows Server 2016.

 

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ação a ser tomada para a máquina virtual quando o software executado pela máquina virtual falha. As falhas nesse caso significam uma falha que é detectável pela plataforma de host, como uma condição de estado de espera noninterruptible. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

Isso pode ser um dos valores a seguir.



| Valor                                                                               | Significado                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>2</dt> </dl>        | Nenhum.<br/>               |
| <dl> <dt>3</dt> </dl>        | Reiniciar.<br/>            |
| <dl> <dt>4</dt> </dl>        | Reverter para instantâneo.<br/> |
| <dl> <dt>5.. 32768</dt> </dl> | Reservado.<br/>           |



 

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ação a ser tomada para a máquina virtual quando o host for desligado. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

Isso pode ser um dos valores a seguir.



| Valor                                                                               | Significado                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <dt>2</dt> </dl>        | Desativar.<br/>   |
| <dl> <dt>3</dt> </dl>        | Salvar estado.<br/> |
| <dl> <dt>4</dt> </dl>        | Desligar.<br/>   |
| <dl> <dt>5.. 32768</dt> </dl> | Reservado.<br/>   |



 

</dd> <dt>

**AutomaticSnapshotsEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se esta máquina virtual deve ter instantâneos automáticos habilitados.

> [!Note]  
> adicionado em Windows 10, versão 1709.

 

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ação a ser tomada para a máquina virtual quando o host for iniciado. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

Isso pode ser um dos valores a seguir.



| Valor                                                                               | Significado                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>2</dt> </dl>        | Nenhum.<br/>                         |
| <dl> <dt>3</dt> </dl>        | Reinicie o se estiver ativo anteriormente.<br/> |
| <dl> <dt>4</dt> </dl>        | Sempre iniciar.<br/>                 |
| <dl> <dt>5.. 32768</dt> </dl> | Reservado.<br/>                     |



 

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tempo de atraso antes que a máquina virtual seja iniciada automaticamente. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um número que indica a sequência relativa de ativação da máquina virtual quando o sistema host é iniciado. Um número mais baixo indica ativação anterior. Se uma ou mais configurações mostrarem o mesmo valor, a sequência será dependente da implementação. Um valor de 0 indica que a sequência é dependente de implementação. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O número de série da placa base para a máquina virtual.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O identificador global exclusivo para o BIOS da máquina virtual.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

**True** se a tecla num lock for definida como on pelo BIOS; **False** se a tecla num lock estiver definida como off pelo BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O número de série do BIOS para a máquina virtual.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

A ordem de inicialização definida no BIOS da máquina virtual. Essa propriedade é uma matriz de valores, **BootOrder** \[ 0 \] a **BootOrder** \[ 3 \] , inclusive, em que cada valor indica um dispositivo para inicializar. Cada um dos quatro valores na matriz deve ser definido e não deve ser o mesmo que outro valor na matriz. A máquina virtual tentará primeiro inicializar do dispositivo indicado pelo primeiro valor dentro da matriz. Se esse dispositivo não contiver um setor de inicialização, a máquina virtual tentará inicializar a partir do próximo dispositivo especificado pela propriedade **BootOrder** e assim por diante. Se nenhum dispositivo especificado no **BootOrder** contiver um setor de inicialização, a máquina virtual falhará ao ser inicializada. O valor padrão de uma máquina virtual é \[ 0, 1, 2, 3 \] .

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Disquete** (0)


</dt> <dd>

A máquina virtual tentará inicializar a partir do disquete dentro da unidade de disquete.

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)


</dt> <dd>

A máquina virtual tentará inicializar a partir do primeiro disco de CD ou DVD encontrado com um setor de inicialização.

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Disco rígido IDE** (2)


</dt> <dd>

A máquina virtual tentará inicializar a partir da primeira unidade de disco rígido encontrada com um setor de inicialização.

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Inicialização PXE** (3)


</dt> <dd>

A máquina virtual tentará inicializar o PXE a partir da rede.

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Disco rígido SCSI** (4)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (5.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootSourceOrder**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A ordem de origem da inicialização para a máquina virtual.

**Windows 8.1:** não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A marca de ativo do chassi para a máquina virtual.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O número de série do chassi para a máquina virtual.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que as informações sobre a configuração da máquina virtual são armazenadas. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho relativo e o nome de arquivo de um arquivo em que as informações sobre a configuração da máquina virtual são armazenadas. Esse caminho é relativo à propriedade **ConfigurationDataRoot** . Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O identificador exclusivo da configuração da máquina virtual. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConsoleMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Identifica o Modo de Console para a VM.

> [!Note]  
> Essa propriedade foi adicionada em Windows 10 e Windows Server 2016.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Padrão** (0)


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

**COM1** (1)


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

**COM2** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que as configurações da máquina virtual foram criadas. Se esse objeto representa as configurações atuais para a máquina virtual, esse valor seria a hora em que o sistema foi criado. Se esse objeto representa as configurações de instantâneo para a máquina virtual, esse valor seria a hora em que o instantâneo foi tirado. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**DebugChannelId**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O identificador de canal usado para depurar a máquina virtual usando o depurador unificado.

</dd> <dt>

**DepurarPort**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A porta TCP/IP usada para depurar a máquina virtual usando a depuração sintética.

</dd> <dt>

**DebugPortEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica se a máquina virtual está usando a depuração sintética. Esse pode ser um dos valores a seguir.

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0)


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)


</dt> <dd>

Atribuído automaticamente

</dd> </dl>

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada [**de \_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como um dos valores a seguir.



| Valor                                                                                                                  | Significado                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>"Configurações ativas para a máquina virtual"</dt> </dl>   | Essa instância refere-se a uma máquina virtual.<br/> |
| <dl> <dt>"Configurações de instantâneo para a máquina virtual"</dt> </dl> | Essa instância refere-se a um instantâneo.<br/>        |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto . Essa propriedade é herdada [**de CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e sempre é definida como o nome de exibição do computador. Esse nome pode não exceder 100 caracteres de comprimento.

</dd> <dt>

**EnhancedSessionTransportType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica o tipo de transporte a ser usado ao se conectar a uma sessão aprimorada.

> [!Note]  
> Essa propriedade foi adicionada no Windows 10, versão 1803.

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

**Pipe VMBus** (0)


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

**Soquete do Hyper-V** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestControlledCacheTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se o convidado pode controlar tipos de cache.

> [!Note]  
> Adicionado em Windows 10 e Windows Server 2016.

 

</dd> <dt>

**GuestStateDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do arquivo de um diretório em que as informações sobre o estado do runtime de convidado são armazenadas.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**GuestStateFile**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do arquivo de um arquivo em que as informações sobre o estado de runtime do convidado são armazenadas. Um caminho relativo é anexado ao valor da **propriedade GuestStateDataRoot.**

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**HighMmioGapSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tamanho da lacuna de E/S alta (acima de 4 GB) Memory-Mapped E/S em MB

> [!Note]  
> Essa propriedade foi adicionada no Windows 10, versão 1703.

 

</dd> <dt>

**IncrementalBackupEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se o vss writer do Hyper-V dá suporte à tomada de backups incrementais dessa máquina virtual.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**IsAutomaticSnapshot**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se esse é um instantâneo criado automaticamente para o usuário.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**IsSaved**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se a configuração tiver uma referência a um arquivo de estado salvo; caso contrário, **False.** Isso não indica a presença desse arquivo, apenas que a configuração especifica um.

</dd> <dt>

**LockOnDisconnect**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Bloqueie o console ao desconectar do vmconnect.

> [!Note]  
> adicionado em Windows 10 e Windows Server 2016.

 

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que as informações de log para a máquina virtual são armazenadas. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**LowMmioGapSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Configura o tamanho, em megabytes, da primeira lacuna de MMIO para uma VM (máquina virtual).

**Windows 8.1:** não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

Intervalo: 128 3584

</dd> <dt>

**NetworkBootPreferredProtocol**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Determina se o protocolo preferencial para inicialização PXE é IPv4 ou IPv6.

**Windows 8.1:** não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> </dl>

</dd> <dt>

**Observações**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Notas fornecidas pelo usuário que estão relacionadas à máquina virtual. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Pai**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se essa instância não representar um sistema baseado em um instantâneo de uma máquina virtual, essa propriedade será **nula**. Caso contrário, a propriedade contém o caminho do objeto do objeto **Msvm \_ VirtualSystemSettingData** no qual essa instância se baseia. Ao criar uma hierarquia de árvore de instantâneo para a máquina virtual, essa propriedade faz referência ao objeto do qual a instância atual é derivada (a instância atual é o nó filho e o objeto referenciado nessa propriedade é o nó pai).

</dd> <dt>

**ParentPackage**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se esse sistema for um contêiner, o caminho para o Msvm \_ ContainerPackage do qual esse sistema se baseia.

> [!Note]  
> Adicionado no Windows 10; removido no Windows 10, versão 1703.

 

</dd> <dt>

**PauseAfterBootFailure**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o BIOS pausa após cada falha na entrada de inicialização aguardando que o usuário pressione uma tecla. **True** se o BIOS pausar; caso contrário, **false**.

**Windows 8.1:** não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**Recuperação de**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho completo de um arquivo em que as informações relacionadas à recuperação para a máquina virtual são armazenadas. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SecureBootEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se a inicialização segura está habilitada para a VM (máquina virtual). **Verdadeiro** se habilitado; caso contrário, **false**.

> [!Note]  
> A inicialização segura só pode ser habilitada para VMs de geração 2.

 

**Windows 8.1:** não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**SecureBootTemplateId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O identificador global exclusivo do modelo de valores iniciales de variáveis relacionadas à inicialização segura de UEFI.

Esta é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

> [!Note]  
> adicionado em Windows 10 e Windows Server 2016.

 

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que as informações sobre os instantâneos de máquina virtual são armazenadas. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que informações sobre as informações relacionadas à suspensão da máquina virtual são armazenadas. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que os arquivos de permuta para a máquina virtual são armazenados. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Userinstantâneotype**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica o tipo de instantâneo definido pelo usuário.

> [!Note]  
> adicionado em Windows 10 e Windows Server 2016.

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** (2)


</dt> <dd>

Desabilite a criação de qualquer instantâneo.

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)


</dt> <dd>

Instantâneo consistente de dados para uso no ambiente de produção. Executa um instantâneo com o estado do aplicativo quando a capacidade de criar um instantâneo consistente de dados não está disponível.

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)


</dt> <dd>

Instantâneo consistente de dados para uso no ambiente de produção. Não criará um instantâneo com o estado do aplicativo se não for possível criar um instantâneo de dados consistente.

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (5)


</dt> <dd>

Instantâneo que contém informações de memória e dispositivo para fins de teste e desenvolvimento.

</dd> </dl>

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão da máquina virtual em um formato de "Major. Minor", por exemplo, "2,0".

</dd> <dt>

**VirtualNumaEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**","[**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")
</dt> </dl>

**True** se os nós numa (acesso não uniforme à memória) estiverem projetados na máquina virtual; **False** se a máquina virtual tiver um único nó. Se **for true**, o número de nós numa virtuais projetados na máquina virtual será determinado com os valores das propriedades [**Msvm \_ ProcessorSettingData. MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) e [**Msvm \_ MemorySettingData. MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) .

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData. VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**")
</dt> </dl>

O nome do objeto [**de \_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de dados CIM ao qual esses dados de configuração pertencem. Essa propriedade é uma substituição do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os valores válidos para essa propriedade são Microsoft: Hyper-V: subtipo: 1 e Microsoft: Hyper-V: subtipo: 2. Uma VM de geração 1 é o subtipo 1. Uma VM de geração 2 é o subtipo 2.

**Windows 8.1:** não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-v: subtipo: 1** ("Microsoft: Hyper-v: subtipo: 1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-v: subtipo: 2** ("Microsoft: Hyper-v: subtipo: 2")


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de máquina virtual que os dados de configuração representam. Essa propriedade é herdada da classe [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) . Esse será um dos valores a seguir.



| Valor                                                                                                                                 | Significado                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>"Microsoft: Hyper-V: System: percebido"</dt> </dl>                        | Uma máquina virtual realizada.<br/>               |
| <dl> <dt>"Microsoft: Hyper-V: System: planejado"</dt> </dl>                         | Uma máquina virtual planejada.<br/>                |
| <dl> <dt>"Microsoft: Hyper-V: instantâneo: percebido"</dt> </dl>                      | Um instantâneo de uma máquina virtual realizada.<br/> |
| <dl> <dt>"Microsoft: Hyper-V: snapshot: Recovery"</dt> </dl>                      | Um instantâneo de uma máquina virtual de recuperação.<br/> |
| <dl> <dt>"Microsoft: Hyper-V: snapshot: planejado"</dt> </dl>                       | Um instantâneo de uma máquina virtual planejada.<br/>  |
| <dl> <dt>"Microsoft: Hyper-V: snapshot: ausente"</dt> </dl>                       | Um instantâneo ausente.<br/>                       |
| <dl> <dt>"Microsoft: Hyper-V: snapshot: réplica: Standard"</dt> </dl>              | Um instantâneo de ponto de replicação baseado em tempo.<br/>  |
| <dl> <dt>"Microsoft: Hyper-V: snapshot: Replica: ApplicationConsistent"</dt> </dl> | Um instantâneo de ponto de replicação do VSS.<br/>         |
| <dl> <dt>"Microsoft: Hyper-V: snapshot: Replica: PlannedFailover"</dt> </dl>       | Um instantâneo de replicação planejado.<br/>           |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ VirtualSystemSettingData** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[Classes de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

