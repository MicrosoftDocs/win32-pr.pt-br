---
description: Representa os dados de configuração do recurso de segurança.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Msvm_EthernetSwitchPortSecuritySettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 214a86513462e70025f0bcb6403faecc3b6663463dbef8c4cb9d1ea60a9c8f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681436"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a>Classe Msvm \_ EthernetSwitchPortSecuritySettingData

Representa os dados de configuração do recurso de segurança.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ EthernetSwitchPortSecuritySettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ EthernetSwitchPortSecuritySettingData** tem essas propriedades.

<dl> <dt>

**AllowIeeePriorityTag**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica se o tráfego de/para a porta retém informações 802.1P. Conterá **True** se o tráfego de/para a porta reter informações 802.1P ou **False** caso contrário. O valor padrão é **Falso**.

</dd> <dt>

**AllowMacSpoofing**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica se a porta permitirá a spoofing do MAC. Se essa propriedade for **True**, a porta permitirá que os endereços MAC sejam falsos. Todos os valores de endereço MAC unicast válidos são permitidos. Se essa propriedade for **False**, a porta permitirá que apenas os endereços MAC configurados no gerenciamento do Hyper-V sejam usados. O valor padrão é **Falso**.

</dd> <dt>

**AllowTeaming**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica se as NICs conectadas à porta podem fazer parte de uma equipe. Isso se aplica somente a NICs conectadas a máquinas virtuais. Conterá **True se** o teaming NIC for permitido ou **False caso** contrário. O valor padrão é **Falso**.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Segurança de Porta do Comutamento Ethernet Configurações".

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Representa os dados de configuração do recurso de segurança".

</dd> <dt>

**DynamicIPAddressLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Define o limite para o número de endereços IP dinâmicos aprendidos. O padrão é nenhum.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Segurança de Porta do Comutamento Ethernet Configurações".

</dd> <dt>

**EnableDhcpGuard**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica se as ofertas DHCP estão bloqueadas da porta. Conterá **True** se as ofertas DHCP são bloqueadas da porta ou **False caso** contrário. O valor padrão é **Falso**.

</dd> <dt>

**EnableFixSpeed10G**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Definido como TRUE se a Velocidade Fixa 10G estiver habilitada, caso afirmando FALSE. O valor padrão é FALSE.

> [!Note]  
> Propriedade adicionada em Windows 10.

 

</dd> <dt>

**EnableRouterGuard**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica se anúncios de roteador e redirecionamentos de roteador são bloqueados da porta. Conterá **True se** anúncios de roteador e redirecionamentos de roteador são bloqueados da porta ou **False caso** contrário. O valor padrão é **Falso**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**\_ ManagedElement do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MonitorMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Isso indica o modo de monitor da porta.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (0)


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

**Destino** (1)


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

**Origem** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**MonitorSession**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica o identificador da sessão de monitor à que essa porta pertence.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sem valor"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Reservado

> [!Note]  
> Propriedade adicionada em Windows 10.

 

</dd> <dt>

**StormLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Define o limite de pacotes por segundo para o tráfego de difusão e multicast. O padrão é nenhum.

</dd> <dt>

**TeamName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Reservado para uso futuro.

</dd> <dt>

**TeamNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Reservado para uso futuro.

</dd> <dt>

**VirtualSubnetId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)
</dt> </dl>

Especifica o identificador da sub-rede virtual da qual a porta é membro. O padrão é none.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

