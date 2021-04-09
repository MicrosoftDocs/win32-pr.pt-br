---
description: Representa uma porta de Fibre Channel sintética.
ms.assetid: 6ca827b5-3ea0-4967-ba1f-b41e84c84009
title: Classe Msvm_SyntheticFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPort
- Msvm_SyntheticFcPort.SetPowerState
- Msvm_SyntheticFcPort.EnableDevice
- Msvm_SyntheticFcPort.OnlineDevice
- Msvm_SyntheticFcPort.QuiesceDevice
- Msvm_SyntheticFcPort.SaveProperties
- Msvm_SyntheticFcPort.RestoreProperties
- Msvm_SyntheticFcPort.InstanceID
- Msvm_SyntheticFcPort.Caption
- Msvm_SyntheticFcPort.Description
- Msvm_SyntheticFcPort.ElementName
- Msvm_SyntheticFcPort.InstallDate
- Msvm_SyntheticFcPort.Name
- Msvm_SyntheticFcPort.OperationalStatus
- Msvm_SyntheticFcPort.StatusDescriptions
- Msvm_SyntheticFcPort.Status
- Msvm_SyntheticFcPort.HealthState
- Msvm_SyntheticFcPort.CommunicationStatus
- Msvm_SyntheticFcPort.DetailedStatus
- Msvm_SyntheticFcPort.OperatingStatus
- Msvm_SyntheticFcPort.PrimaryStatus
- Msvm_SyntheticFcPort.EnabledState
- Msvm_SyntheticFcPort.OtherEnabledState
- Msvm_SyntheticFcPort.RequestedState
- Msvm_SyntheticFcPort.EnabledDefault
- Msvm_SyntheticFcPort.TimeOfLastStateChange
- Msvm_SyntheticFcPort.AvailableRequestedStates
- Msvm_SyntheticFcPort.TransitioningToState
- Msvm_SyntheticFcPort.SystemCreationClassName
- Msvm_SyntheticFcPort.SystemName
- Msvm_SyntheticFcPort.CreationClassName
- Msvm_SyntheticFcPort.DeviceID
- Msvm_SyntheticFcPort.PowerManagementSupported
- Msvm_SyntheticFcPort.PowerManagementCapabilities
- Msvm_SyntheticFcPort.Availability
- Msvm_SyntheticFcPort.StatusInfo
- Msvm_SyntheticFcPort.LastErrorCode
- Msvm_SyntheticFcPort.ErrorDescription
- Msvm_SyntheticFcPort.ErrorCleared
- Msvm_SyntheticFcPort.OtherIdentifyingInfo
- Msvm_SyntheticFcPort.PowerOnHours
- Msvm_SyntheticFcPort.TotalPowerOnHours
- Msvm_SyntheticFcPort.IdentifyingDescriptions
- Msvm_SyntheticFcPort.AdditionalAvailability
- Msvm_SyntheticFcPort.MaxQuiesceTime
- Msvm_SyntheticFcPort.Speed
- Msvm_SyntheticFcPort.MaxSpeed
- Msvm_SyntheticFcPort.RequestedSpeed
- Msvm_SyntheticFcPort.UsageRestriction
- Msvm_SyntheticFcPort.PortType
- Msvm_SyntheticFcPort.OtherPortType
- Msvm_SyntheticFcPort.OtherNetworkPortType
- Msvm_SyntheticFcPort.PortNumber
- Msvm_SyntheticFcPort.LinkTechnology
- Msvm_SyntheticFcPort.OtherLinkTechnology
- Msvm_SyntheticFcPort.PermanentAddress
- Msvm_SyntheticFcPort.NetworkAddresses
- Msvm_SyntheticFcPort.FullDuplex
- Msvm_SyntheticFcPort.AutoSense
- Msvm_SyntheticFcPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticFcPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticFcPort.SupportedCOS
- Msvm_SyntheticFcPort.ActiveCOS
- Msvm_SyntheticFcPort.SupportedFC4Types
- Msvm_SyntheticFcPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f28614a7c885c0cfc03d546219518cda240219a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090010"
---
# <a name="msvm_syntheticfcport-class"></a>\_Classe Msvm SyntheticFcPort

> [!NOTE]
> Este artigo contém referências ao termo "servidor subordinado", um termo que a Microsoft não usa mais. Quando o termo for removido do software, também o removeremos deste artigo.

Representa uma porta de Fibre Channel sintética.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPort : CIM_FCPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 4;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SyntheticFcPort** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Msvm \_ SyntheticFcPort** tem esses métodos.



| Método                                                                | Descrição                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                      | Não há suporte para o método.<br/> |
| **OnlineDevice**                                                      | Não há suporte para o método.<br/> |
| **QuiesceDevice**                                                     | Não há suporte para o método.<br/> |
| [**RequestStateChange**](msvm-syntheticfcport-requeststatechange.md) | Solicita uma alteração de estado.<br/>      |
| [**Redefinir**](msvm-syntheticfcport-reset.md)                           | Redefine o dispositivo virtual.<br/>    |
| **Restaurarproperties**                                                 | Não há suporte para o método.<br/> |
| **Salvarproperties**                                                    | Não há suporte para o método.<br/> |
| **SetPowerState**                                                     | Não há suporte para o método.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Msvm \_ SyntheticFcPort** tem essas propriedades.

<dl> <dt>

**ActiveCOS**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de inteiros que indica as classes de serviço que estão ativas. O COS com suporte é especificado pela propriedade **SupportedCOS** . Essa propriedade é herdada do **CIM \_ FCPort**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="1"></span>**1** (1)
</dt> <dt>

<span id="2"></span>**2** (2)
</dt> <dt>

<span id="3"></span>**3** (3)
</dt> <dt>

<span id="4"></span>**4** (4)
</dt> <dt>

<span id="5"></span>**5** (5)
</dt> <dt>

<span id="6"></span>**6** (6)
</dt> <dt>

<span id="F"></span><span id="f"></span>**F** (7)
</dt> </dl>

</dd> <dt>

**ActiveFC4Types**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de inteiros que indica o Fibre Channel protocolos FC-4 em execução no momento. Uma lista de todos os protocolos com suporte é especificada pela propriedade **SupportedFC4Types** . Essa propriedade é herdada do **CIM \_ FCPort**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)
</dt> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sobre FC** (5)
</dt> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)
</dt> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)
</dt> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 mestre** (17)
</dt> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 escravo** (18)
</dt> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 par** (19)
</dt> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)
</dt> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 escravo** (22)
</dt> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 par** (23)
</dt> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)
</dt> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidade de controle SBCCS** (26)
</dt> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)
</dt> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidade de controle FC-SB-2** (28)
</dt> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Serviços de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)
</dt> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)
</dt> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)
</dt> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)
</dt> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controle bbl** (80)
</dt> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada bbl FDDI** (81)
</dt> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)
</dt> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)
</dt> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)
</dt> <dt>

<span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Exclusivo do fornecedor** (255)
</dt> </dl>

</dd> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **unidades** ("bytes")
</dt> </dl>

A unidade de transmissão máxima (MTU) do negociada ou ativa que pode ter suporte, em bytes. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Qualquer disponibilidade e status adicionais do dispositivo. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**Autodetecção**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a porta é capaz de determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Disponibilidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A disponibilidade e o status principais do dispositivo. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** . Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.

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

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000.. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe de criação do sistema de escopo. Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

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

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000.. )
</dt> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico. Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os Estados habilitado e desabilitado de um elemento. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e será um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt></dt> <dt>0</dt> desconhecido </dl>                                                 | Não foi possível determinar o estado do elemento.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Outros**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Habilitado**</dt> <dt>2</dt> </dl>                                                 | O elemento está em execução.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Desabilitado**</dt> <dt>3</dt> </dl>                                             | O elemento está desativado.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Desligando**</dt> <dt>4</dt> </dl>                         | O elemento está no processo de ir para um estado desabilitado.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Não aplicável**</dt> <dt>5</dt> </dl>                     | O elemento não dá suporte a ser habilitado ou desabilitado.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Habilitado, mas offline**</dt> <dt>6</dt> </dl> | O elemento pode estar concluindo comandos e removerá todas as novas solicitações.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**No teste**</dt> <dt>7</dt> </dl>                                                 | O elemento está em um estado de teste.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Adiado**</dt> <dt>8</dt> </dl>                                             | O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Desativar**</dt> <dt>9</dt> </dl>                                                 | O elemento está habilitado, mas em um modo restrito. O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos. Todas as outras solicitações são enfileiradas.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Iniciando**</dt> em <dt>10</dt> </dl>                                            | O elemento está no processo de ir para um estado habilitado (2). Novas solicitações são enfileiradas.<br/>                                                                                                             |



 

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o erro relatado em **LastErrorCode** agora está limpo. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

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

A integridade atual do elemento. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** . Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

O último código de erro relatado pelo dispositivo lógico. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de tecnologia de link para a porta. Quando definido como 1 (outro), a propriedade **OtherLinkTechnology** contém uma descrição de cadeia de caracteres do tipo de link. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).



| Valor                                                                                                                                                                              | Significado                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC"></span><span id="fc"></span><dl> <dt>**FC**</dt> <dt>4</dt> </dl> | Fibre Channel<br/> |



 

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade foi substituída. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **unidades** ("bits por segundo")
</dt> </dl>

A largura de banda máxima da porta, em bits por segundo. Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O rótulo pelo qual o objeto é conhecido. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

Uma matriz de cadeias de caracteres que contêm os endereços MAC para a porta. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** . Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os status atuais do objeto. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro). Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um valor de cadeia de caracteres que descreve **LinkTechnology** quando é definido como 1, (outro). Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O uso dessa propriedade é preterido no lugar da propriedade **PortType** . Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve o tipo de módulo, quando **PortType** é definido como 1 (outro). Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

O endereço de rede embutido em uma porta. Esse endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software. Quando essa alteração é feita, o campo deve ser atualizado ao mesmo tempo. Essa propriedade deverá ser **nula** se não existir nenhum endereço codificado para o adaptador de rede. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número da porta. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O modo específico que está habilitado no momento para a porta. Quando definido como 1 (outro), a propriedade **OtherPortType** relacionada contém uma descrição de cadeia de caracteres do tipo de porta. Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>+ **/50 10BaseT de cobre** (50)
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

<span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)
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

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (16000.. 65535)
</dt> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os recursos de gerenciamento de energia do dispositivo. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o dispositivo pode ser gerenciado por energia. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status de alto nível. Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000.. )
</dt> </dl>

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: somente gravação
</dt> <dt>

Qualificadores: **unidades** ("bits por segundo")
</dt> </dl>

A largura de banda solicitada da porta, em bits por segundo. A largura de banda real é relatada na propriedade **Speed** . Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O último estado solicitado ou desejado para o elemento. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).

</dd> <dt>

**Velocidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **unidades** ("bits por segundo")
</dt> </dl>

A largura de banda da porta, em bits por segundo. Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

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

Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** . Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado atual do dispositivo lógico. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**SupportedCOS**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de inteiros que indica o Fibre Channel classes de serviço (COS) que têm suporte. O COS ativo é especificado pela propriedade **ActiveCOS** . Essa propriedade é herdada do **CIM \_ FCPort**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="1"></span>**1** (1)
</dt> <dt>

<span id="2"></span>**2** (2)
</dt> <dt>

<span id="3"></span>**3** (3)
</dt> <dt>

<span id="4"></span>**4** (4)
</dt> <dt>

<span id="5"></span>**5** (5)
</dt> <dt>

<span id="6"></span>**6** (6)
</dt> <dt>

<span id="F_"></span><span id="f_"></span>**F** (7)
</dt> </dl>

</dd> <dt>

**SupportedFC4Types**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de inteiros que indica o Fibre Channel protocolos FC-4 com suporte. Os protocolos que estão ativos e em execução são especificados pela propriedade **ActiveFC4Types** . Essa propriedade é herdada do **CIM \_ FCPort**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)
</dt> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP sobre FC** (5)
</dt> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)
</dt> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)
</dt> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 mestre** (17)
</dt> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 escravo** (18)
</dt> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 par** (19)
</dt> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)
</dt> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 escravo** (22)
</dt> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 par** (23)
</dt> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)
</dt> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidade de controle SBCCS** (26)
</dt> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)
</dt> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidade de controle FC-SB-2** (28)
</dt> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Serviços de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)
</dt> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)
</dt> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)
</dt> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)
</dt> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controle bbl** (80)
</dt> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada bbl FDDI** (81)
</dt> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)
</dt> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)
</dt> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)
</dt> <dt>

<span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Exclusivo do fornecedor** (255)
</dt> </dl>

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **unidades** ("bytes")
</dt> </dl>

A MTU (unidade máxima de transmissão) que pode ter suporte, em bytes. Essa propriedade é herdada do [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe de criação do sistema de escopo. Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

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

A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número total de horas em que este dispositivo foi ligado. Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o estado de destino para o qual a instância está em transição. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.

</dd> <dt>

**UsageRestriction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Em algumas circunstâncias, uma porta lógica pode ser identificável como uma porta de front-end ou de back-end. Um exemplo dessa situação seria uma matriz de armazenamento que pode ter portas de back-end para se comunicar com unidades de disco e portas de front-end para se comunicar com os hosts. Se não houver nenhuma restrição sobre o uso da porta, o valor deverá ser definido como 4 (não restrito). Essa propriedade é herdada do [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Somente front-end** (2)
</dt> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Somente back-end** (3)
</dt> <dt>

<span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Não restrito** (4)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

