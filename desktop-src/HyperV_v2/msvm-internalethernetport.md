---
description: Representa uma porta Ethernet interna (adaptador de rede).
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Classe Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647366"
---
# <a name="msvm_internalethernetport-class"></a>\_Classe Msvm InternalEthernetPort

Representa uma porta Ethernet interna (adaptador de rede). Esse tipo de porta Ethernet dá acesso às máquinas virtuais ao servidor de virtualização que executa o software de rede. Os adaptadores de rede internos permitem que o tráfego de rede das máquinas virtuais seja roteado ou filtrado antes de sair do sistema físico.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_InternalEthernetPort";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ InternalEthernetPort** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Msvm \_ InternalEthernetPort** tem esses métodos.



| Método                                                                     | Descrição                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                           | Não há suporte para o método.<br/> |
| **OnlineDevice**                                                           | Não há suporte para o método.<br/> |
| **QuiesceDevice**                                                          | Não há suporte para o método.<br/> |
| [**RequestStateChange**](msvm-internalethernetport-requeststatechange.md) | Solicita uma alteração de estado.<br/>      |
| [**Redefinir**](msvm-internalethernetport-reset.md)                           | Redefine o dispositivo virtual.<br/>    |
| **Restaurarproperties**                                                      | Não há suporte para o método.<br/> |
| **Salvarproperties**                                                         | Não há suporte para o método.<br/> |
| **SetPowerState**                                                          | Não há suporte para o método.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Msvm \_ InternalEthernetPort** tem essas propriedades.

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A unidade de transmissão máxima (MTU) do negociada ou ativa, que pode ter suporte. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** . Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**Autodetecção**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a porta de rede é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Disponibilidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A disponibilidade e o status principais do dispositivo. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado. Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) . Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual. Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.

Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.

</dd> <dt>

**Funcionalidades**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Recursos da porta Ethernet. Se os recursos de failover ou balanceamento de carga estiverem listados, um (failover) [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-sparegroup) ou [**CIM \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (balanceamento de carga) também deverá ser definido para descrever completamente o recurso. Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)
</dt> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)
</dt> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)
</dt> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Balanceamento de carga** (5)
</dt> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos de porta Ethernet que são indicados na matriz **Capabilities** . Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice. Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe ou da subclasse usada na criação de uma instância. Quando usado com as outras propriedades de chave dessa classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente. Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um endereço ou outras informações de identificação usadas para nomear exclusivamente o dispositivo lógico. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID* \\ *específico do dispositivo-dados*".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e é gerada com base na NIC presente no host.

</dd> <dt>

**EnabledCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica quais recursos estão habilitados na lista de todos os que têm suporte, que são definidos na matriz de **recursos** . Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)
</dt> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)
</dt> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)
</dt> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Balanceamento de carga** (5)
</dt> </dl>

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os Estados habilitado e desabilitado de um elemento. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o erro relatado na propriedade **LastErrorCode** agora está apagado. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas. Essa propriedade é herdada da propriedade [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a porta está operando no modo full duplex. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A integridade atual do elemento. Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** . Cada entrada dessa matriz está relacionada à entrada na matriz da propriedade **OtherIdentifyingInfo** que está localizada no mesmo índice. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um valor **DateTime** que indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O último código de erro relatado pelo dispositivo lógico. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os tipos de links. Quando definido como 1 (outro), a propriedade relacionada **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).



| Valor                                                                        | Significado             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <dt>2</dt> </dl> | Ethernet<br/> |



 

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido. Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade foi substituída. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A largura de banda máxima da porta, em bits por segundo. Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os endereços MAC Ethernet/802.3 formatados como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par representando um dos seis octetos do endereço MAC na ordem de bits canônica (o bit de endereço do grupo é encontrado no bit inferior do primeiro caractere da cadeia de caracteres). Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** . Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O status atual do elemento. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherEnabledCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos habilitados que são especificados como 1 (outro). Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro.) Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Todos os dados, além das informações de ID do dispositivo, que podem ser usados para identificar um dispositivo lógico. Por exemplo, você pode usar essa propriedade para armazenar o nome de exibição do sistema operacional para o dispositivo. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um valor de cadeia de caracteres que descreve a propriedade **LinkTechnology** quando ela é definida como 1 (outra). Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é preterida. Use a propriedade **PortType** . Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

Descrição preterida: o tipo de módulo, quando a propriedade **PortType** é definida como 1 (outro).

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de módulo, quando a propriedade **PortType** é definida como 1 (outro). Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) .

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço de rede embutido em uma porta. Esse endereço pode ser alterado usando uma atualização de firmware ou uma configuração de software. Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo. Isso deve ser deixado em branco se não existir nenhum endereço codificado para o adaptador de rede. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As portas de rede geralmente são numeradas em relação a um módulo lógico ou um elemento de rede. Esse valor é 1 para NICs emuladas, 0 para todos os outros. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O modo específico que está habilitado no momento para a porta. Quando definido como 1 (outro), a propriedade relacionada **OtherPortType** contém uma descrição de cadeia de caracteres do tipo de porta. Essa propriedade é herdada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>+ **/50 10BaseT de cobre** (50)
</dt> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)
</dt> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)
</dt> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000baseT** (53)
</dt> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)
</dt> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)
</dt> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)
</dt> <dt>

<span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)
</dt> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)
</dt> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)
</dt> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)
</dt> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)
</dt> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-Sr** (105)
</dt> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)
</dt> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)
</dt> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)
</dt> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)
</dt> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)
</dt> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ovo** (111)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (16000 65535)
</dt> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os recursos de gerenciamento de energia do dispositivo. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o dispositivo pode ser gerenciado por energia. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de horas consecutivas em que este dispositivo foi ligado, desde seu último ciclo de energia. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status de alto nível. Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A largura de banda solicitada da porta, em bits por segundo. A largura de banda real é relatada na propriedade **Speed** . Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O último estado solicitado ou desejado para o serviço de gerenciamento. Quando a propriedade **enabledstate** é definida como 5 (não aplicável), essa propriedade não tem significado. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**Velocidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **substituição**, **unidades** ("bits por segundo")
</dt> </dl>

A largura de banda atual da porta em bits por segundo. Para portas que variam de largura de banda ou para aquelas em que não é possível fazer nenhuma estimativa precisa, essa propriedade deve conter a largura de banda nominal. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O status atual do objeto. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** . As entradas nessa matriz são correlacionadas com aquelas no mesmo índice de matriz em **OperationalStatus**. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado do dispositivo lógico. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A MTU (unidade máxima de transmissão) que pode ter suporte. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe de criação do sistema de escopo. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é suportada

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do sistema de escopo. Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data ou a hora em que a propriedade **enabledstate** do elemento foi alterada pela última vez. Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0. Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e não é usada.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número total de horas em que este dispositivo foi ligado. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e não é usada.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o estado de destino para o qual a instância está em transição. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.

</dd> <dt>

**UsageRestriction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end. Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).



| Valor                                                                        | Significado                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>4</dt> </dl> | Não restrito<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ InternalEthernetPort** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

Consulte [consultando objetos de rede](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ETHERNETPORT CIM**](cim-ethernetport.md)
</dt> <dt>

[**\_ETHERNETPORT CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

