---
description: Representa a configuração atual de um comutador Ethernet virtual.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Classe Msvm_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bbd8cd77a96301187e9b5c9f8544a23b616bf9db78af6560296660b0a3995bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681236"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a>\_Classe Msvm VirtualEthernetSwitchSettingData

Representa a configuração atual de um comutador Ethernet virtual.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
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
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualEthernetSwitchSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualEthernetSwitchSettingData** tem essas propriedades.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de pools de recursos de host a serem associados ou que estão atualmente associados ao comutador Ethernet para fins de alocação de conexões Ethernet entre uma máquina virtual e um comutador Ethernet. Cada valor deve estar em conformidade com o URI WBEM de produção \_ \_ UntypedInstancePath, conforme definido em DSP0207. Essa propriedade é herdada do **CIM \_ VirtualEthernetSwitchSettingData**.

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ação a ser tomada para a máquina virtual quando o software executado pela máquina virtual falha. As falhas nesse caso significam uma falha que é detectável pela plataforma do host, como uma condição de estado de espera não passível de interrupção. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ação a ser tomada para a máquina virtual quando o host for desligado. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ação a ser tomada para a máquina virtual quando o host for iniciado. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tempo de atraso antes que a máquina virtual seja iniciada automaticamente. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um número que indica a sequência relativa de ativação da máquina virtual quando o sistema host é iniciado. Um número mais baixo indica ativação anterior. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**BandwidthReservationMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O modo de reserva de largura de banda.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Padrão** (0)


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**Peso** (1)


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**Absoluto** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "comutador Ethernet Virtual Configurações".

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que as informações sobre a configuração da máquina virtual são armazenadas. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho relativo e o nome de arquivo de um arquivo em que as informações sobre a configuração da máquina virtual são armazenadas. Esse caminho é relativo à propriedade **ConfigurationDataRoot** . Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O identificador exclusivo da configuração da máquina virtual. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que as configurações foram criadas. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações ativas para o comutador Ethernet virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ExtensionOrder**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Uma matriz de instâncias inseridas da classe [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representam as extensões de comutador associadas a essa opção, na ordem em que elas são aplicadas.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) e é sempre definida como "Microsoft:*GUID* \\ *DeviceSpecificData*".

</dd> <dt>

**IOVPreferred**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se SR-IOV (virtualização de e/s de raiz única) é preferencial ou não, se disponível, no adaptador subjacente.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que as informações de log para a máquina virtual são armazenadas. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

especifica o número máximo de endereços mac exclusivos que podem ser aprendidos pelo comutador para dar suporte ao endereço mac Learning, conforme definido no padrão IEEE 802,1. Essa propriedade é herdada do **CIM \_ VirtualEthernetSwitchSettingData**.

</dd> <dt>

**Observações**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Notas fornecidas pelo usuário que estão relacionadas à máquina virtual. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**PacketDirectEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o PacketDirect deve ser usado, se disponível. O valor padrão é **false**.

> [!Note]  
> esta propriedade foi adicionada em Windows 10 e Windows Server 2016.

 

</dd> <dt>

**Recuperação de**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho completo de um arquivo em que as informações relacionadas à recuperação para a máquina virtual são armazenadas. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que as informações sobre os instantâneos de máquina virtual são armazenadas. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que informações sobre as informações relacionadas à suspensão da máquina virtual são armazenadas. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho de um diretório em que os arquivos de permuta para a máquina virtual são armazenados. Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.

</dd> <dt>

**TeamingEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o agrupamento NIC deve ser usado. O valor padrão é **false**.

> [!Note]  
> Essa propriedade foi adicionada a inWindows 10 e Windows Server 2016.

 

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto [**de \_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de dados CIM ao qual esses dados de configuração pertencem. Essa propriedade é uma substituição do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de máquina virtual que os dados de configuração representam. Essa propriedade é herdada do [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de identificadores de VLAN que esse comutador pode acessar. Essa propriedade é herdada do **CIM \_ VirtualEthernetSwitchSettingData**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

