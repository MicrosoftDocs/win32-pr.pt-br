---
description: Representa o ponto de extremidade da VLAN de uma porta switch.
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Msvm_VLANEndpoint classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: beeecdebe03a443c1da95a75598bc83b9c7e2f0952cd85ceaad1866e2200ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146229"
---
# <a name="msvm_vlanendpoint-class"></a>Classe Msvm \_ VLANEndpoint

Representa o ponto de extremidade da VLAN de uma porta switch. A configuração desse ponto de extremidade mudará a maneira como a porta switch envia pacotes VLAN por meio da opção .

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ VLANEndpoint** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Msvm \_ VLANEndpoint** tem esses métodos.



| Método                                                             | Descrição                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-vlanendpoint-requeststatechange.md) | Solicita uma alteração de estado.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe Msvm \_ VLANEndpoint** tem essas propriedades.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica os valores possíveis para o *parâmetro RequestedState* do [**método RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado. Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada de **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). Essa propriedade poderá ser não nula **se** uma implementação puder anunciar o conjunto de valores possíveis como uma função do estado atual. Essa propriedade será **Null se** uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.

Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Adiar** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reservado** (.. )
</dt> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Ponto de Extremidade VLAN".

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente. Um **valor** Nulo indica que essa propriedade não está implementada. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe ou da subclasse usada na criação de uma instância. Essa propriedade é herdada [**de Cim \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)e sempre é definida como "Msvm \_ VLANEndpoint".

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Ponto de Extremidade da VLAN da Microsoft".

</dd> <dt>

**DesiredEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: somente gravação
</dt> </dl>

O modo de VLAN desejado que é solicitado para uso. O modo atual é dado pela **propriedade OperationalEndpointMode.** Essa propriedade é herdada de [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).



| Valor                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reservado**</dt> <dt>0</dt> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Outros**</dt> <dt>1</dt> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <dt>**Acesso**</dt> <dt>2</dt> </dl>                                                   | Coloca a porta de ponto de extremidade/com opção no modo permanente sem interrupção e negocia para converter o link em um link não seguro. O ponto de extremidade se torna uma interface nãotrunk.<br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <dt>**Dynamic Auto**</dt> <dt>3</dt> </dl>                           | Torna o ponto de extremidade capaz de converter o link em um link do tronco. O ponto de extremidade se tornará uma interface de tronco se a interface vizinho estiver definida como tronco ou modo desejável.<br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <dt>**Dinâmico Desejável**</dt> <dt>4</dt> </dl>       | Faz com que o ponto de extremidade tente converter ativamente o link em um link do tronco. O ponto de extremidade se tornará uma interface de tronco se a interface vizinho estiver definida como tronco, desejável ou modo automático. O modo de porta de opção padrão para todas as interfaces Ethernet é dinâmico desejável.<br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <dt>**Tronco**</dt> <dt>5</dt> </dl>                                                       | Coloca o ponto de extremidade no modo de tronco permanente e negocia para converter o link em um link de tronco. O ponto de extremidade se torna uma interface de tronco mesmo que a interface de vizinho não seja uma interface de tronco.<br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <dt>**Dot1Q Tunnel**</dt> <dt>6</dt> </dl>                           | Configura a interface como um ponto de extremidade/porta de túnel (sem interrupção) a ser conectada em um link assimétrico com uma porta tronco de 802,1Q. O túnel 802.1Q é usado para manter a integridade da VLAN do cliente em uma rede do provedor de serviços.<br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reservado**</dt> <dt>7 32767</dt> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fornecedor Reservado**</dt> <dt>32768 65535</dt> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

**DesiredVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de encapsulamento de VLAN solicitado para uso. O encapsulamento atualmente em uso é dado pela propriedade **OperationalVLANTrunkEncapsulation.** Essa propriedade só é aplicável quando o ponto de extremidade está operando em um modo de tronco (consulte a propriedade **OperationalEndpointMode** para obter detalhes adicionais). Essa propriedade é 2 (Não Aplicável) (ou seja, o ponto de extremidade nunca será colocado em um modo de tronco), um tipo específico (802,1Q ou Cisco ISL) ou 5 (Negotiate) (ou seja, o resultado da negociação entre essa interface e seu vizinho). O valor 5 (Negotiate) não é permitido se o ponto de extremidade não dá suporte à negociação. Essa funcionalidade depende do hardware e do fornecedor. Essa propriedade é herdada de [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

<dl> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (2)
</dt> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)
</dt> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)
</dt> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negociar** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (6 32767)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (32768 65535)
</dt> </dl>

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento. Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e é sempre definida como 2 (habilitado).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os Estados habilitado e desabilitado deste elemento. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (não aplicável).

</dd> <dt>

**GVRPStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o GVRP (protocolo de registro de VLAN GARP) está habilitado ou desabilitado no ponto de extremidade/porta do tronco. Essa propriedade é 2 (não aplicável), a menos que GVRP seja suportado pelo ponto de extremidade. Essa propriedade é aplicável somente quando o ponto de extremidade está operando no modo de entroncamento (consulte a propriedade **OperationalEndpointMode** para obter detalhes adicionais). Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (2)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)
</dt> <dt>

<span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Desabilitado** (4)
</dt> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A integridade atual do elemento. Essa propriedade expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes. Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que o objeto foi instalado. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e não é usada.

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O rótulo pelo qual o objeto é conhecido. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A heurística de nomenclatura selecionada para garantir que o valor da propriedade **Name** seja exclusivo. Essa propriedade é herdada de [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) e não é usada.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** . Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O modo de configuração para o ponto de extremidade de VLAN. Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).



| Valor                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>0</dt> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Outros**</dt> <dt>1</dt> </dl>                                                       | O ponto de extremidade não reconhece VLAN.<br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <dt>**Acesso**</dt> <dt>2</dt> </dl>                                                   | Coloca o ponto de extremidade em modo de não entroncamento permanente e negocia para converter o link em um link não tronco. O ponto de extremidade se torna uma interface de não tronco.<br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <dt>**Auto 3 dinâmicos**</dt> <dt></dt> </dl>                           | Torna o ponto de extremidade capaz de converter o link para um link de tronco. O ponto de extremidade se tornará uma interface de tronco se a interface vizinha estiver definida para o modo trunk ou desejável.<br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <dt>**Dinâmicos desejáveis**</dt> <dt>4</dt> </dl>       | Torna o ponto de extremidade uma tentativa ativa de converter o link para um link de tronco. O ponto de extremidade se tornará uma interface de tronco se a interface vizinha estiver definida para o modo Trunk, desejável ou auto. Esse é o modo padrão de porta de comutador para todas as interfaces Ethernet.<br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <dt>**Tronco**</dt> <dt>5</dt> </dl>                                                       | Coloca o ponto de extremidade no modo de entroncamento permanente e negocia para converter o link em um link de tronco. O ponto de extremidade se torna uma interface de tronco, mesmo se a interface vizinha não for uma interface de tronco.<br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <dt>**Dot1Q Tunnel**</dt> <dt>6</dt> </dl>                           | Configura a interface como um ponto de extremidade/porta de túnel (sem tronco) a ser conectado em um link assimétrico com uma porta de tronco 802.1 Q. o túnel 802.1 q é usado para manter a integridade da VLAN do cliente em uma rede do provedor de serviços.<br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>7 32767</dt> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fornecedor reservado**</dt> <dt>32768 65535</dt> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os status atuais do objeto. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento de matriz é sempre definido como 2 (OK).

</dd> <dt>

**OperationalVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de encapsulamento de VLAN em uso em um ponto de extremidade/porta do tronco. Essa propriedade é 2 (Não Aplicável) (ou seja, o ponto de extremidade não está operando no modo de tronco), um tipo específico (3 - 802.1Q ou 4 - Cisco ISL), 5 (Negotiate) (ou seja, os pontos de extremidade estão negociando o tipo de encapsulamento). Essa propriedade só é aplicável quando o ponto de extremidade está operando em um modo de tronco (consulte a propriedade **OperationalEndpointMode** para obter detalhes adicionais). Essa propriedade é herdada de [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (2)
</dt> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)
</dt> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)
</dt> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negociação** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (6 32767)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor Reservado** (32768 65535)
</dt> </dl>

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **EnabledState** é definida como 1 ("Outro"). Essa propriedade deve ser definida como **Null quando** **EnabledState** for qualquer valor diferente de 1. Essa propriedade é herdada [**de CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **Null.**

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de modelo de ponto de extremidade VLAN com suporte por esse ponto de extremidade VLAN, quando o valor da propriedade **OperationalEndpointMode** é definido como 1 (Outro). Essa propriedade deve ser definida como **Null quando** a **propriedade OperationalEndpointMode** for qualquer valor diferente de 1. Essa propriedade é herdada de [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

</dd> <dt>

**OtherTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de encapsulamento de VLAN que é suportado por esse ponto de extremidade de VLAN, quando o valor da propriedade **OperationalVLANTrunkEncapsulation** é definido como 1 (Outro). Essa propriedade deve ser definida como **Null quando** a propriedade de encapsulamento desejada for qualquer valor diferente de 1. Essa propriedade é herdada de [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de ponto de extremidade de protocolo quando a propriedade **Type** dessa classe (ou qualquer uma de suas subclasses) é definida como 1 (Outro). Essa propriedade é herdada do [**Protocolo \_ CIMEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)e sempre é definida como "Ethernet Virtual".

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status de alto nível. Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de saúde detalhadas e de alto nível para o elemento e seus subcomponentes. Um **valor** Nulo indica que essa propriedade não está implementada. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O [IANA ifType MIB.](https://www.iana.org/assignments/ianaiftype-mib) Essa propriedade é herdada de [**Cim \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)e é sempre definida como 1 (Outro).

</dd> <dt>

**Protocoltype**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada de [**Cim \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) e não é usada.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O último estado solicitado ou desejado para o serviço de gerenciamento. Essa propriedade é herdada [**de CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sempre é definida como 12 (não aplicável).



| Valor                                                                         | Significado                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Não aplicável.<br/> |



 

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve o status do elemento. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

"OK"

"Erro"

"Degradado"

"Desconhecido"

"Pred Fail"

"Iniciando"

"Parando"

"Serviço"

"Stressed"

"NonRecover"

"Sem contato"

"Comunicação Perdida"

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeias de caracteres que descrevem os **vários valores de matriz OperationalStatus.** Essa propriedade é herdada de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento de matriz é sempre definido como "OK".

</dd> <dt>

**SupportedEndpointModes**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexado")
</dt> </dl>

Os modos de ponto de extremidade com suporte por essa porta.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da classe de criação do sistema de scoping. Essa propriedade é herdada [**do Serviço \_ CIMAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)e sempre é definida como "Msvm \_ VirtualSwitch"

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do sistema de scoping. Essa propriedade é herdada de [**Cim \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que o estado habilitado do elemento foi alterado pela última vez. Essa propriedade é herdada [**de CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não tem suporte.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o estado de destino para o qual a instância está em transição. Essa propriedade é herdada [**de CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe Msvm \_ VLANEndpoint** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

Consulte [Consultando objetos de rede](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md)
</dt> <dt>

[**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

