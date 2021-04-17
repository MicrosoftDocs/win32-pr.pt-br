---
description: Representa os dados de status do recurso de largura de banda da porta.
ms.assetid: 1f7be0dd-3d2f-49ef-aff0-cb162389194a
title: Classe Msvm_EthernetSwitchPortBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthData
- Msvm_EthernetSwitchPortBandwidthData.InstanceID
- Msvm_EthernetSwitchPortBandwidthData.Caption
- Msvm_EthernetSwitchPortBandwidthData.Description
- Msvm_EthernetSwitchPortBandwidthData.ElementName
- Msvm_EthernetSwitchPortBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.SystemName
- Msvm_EthernetSwitchPortBandwidthData.DeviceCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.DeviceID
- Msvm_EthernetSwitchPortBandwidthData.CreationClassName
- Msvm_EthernetSwitchPortBandwidthData.Name
- Msvm_EthernetSwitchPortBandwidthData.CurrentBandwidthReservationPercentage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55e8ad735d712bdd388e42b1f4174ee1a78af184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750843"
---
# <a name="msvm_ethernetswitchportbandwidthdata-class"></a>\_Classe Msvm EthernetSwitchPortBandwidthData

Representa os dados de status do recurso de largura de banda da porta.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthData : Msvm_EthernetPortData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Feature Status";
  string Description = "Represents the port bandwidth feature status data.";
  string ElementName = "Ethernet Switch Port Bandwidth Feature Status";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName = "Msvm_EthernetSwitchPortBandwidthData";
  string Name;
  uint32 CurrentBandwidthReservationPercentage = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetSwitchPortBandwidthData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetSwitchPortBandwidthData** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "status do recurso de largura de banda da porta do comutador Ethernet".

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

O nome da subclasse usada na criação desta instância de dados de porta. Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ EthernetSwitchPortBandwidthData".

</dd> <dt>

**CurrentBandwidthReservationPercentage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

A porcentagem atual da largura de banda reservada para esta porta.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "representa os dados de status do recurso de largura de banda da porta.".

</dd> <dt>

**DeviceCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

O nome da classe de criação do sistema de escopo. Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ EthernetSwitchPort".

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (64)
</dt> </dl>

A ID do dispositivo da porta que abrange essa instância de dados de porta. Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "status do recurso de largura de banda da porta do comutador Ethernet".

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
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

Uma cadeia de caracteres que identifica exclusivamente essa instância de dados de porta dentro do escopo do comutador e da porta. Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

O nome da classe de criação do sistema de escopo. Essa propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)e é sempre definida como "Msvm \_ VirtualEthernetSwitch".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

O nome do comutador virtual que abrange essa instância de dados de porta. Esta propriedade é herdada de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

