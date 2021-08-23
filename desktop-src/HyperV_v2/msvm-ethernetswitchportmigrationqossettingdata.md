---
description: Representa as configurações de QOS VFP.
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Classe Msvm_EthernetSwitchPortMigrationQosSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fef4ef759b406facb5fbbb12d37eceb55a914d46c63a2485982f60fa151ccdaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524036"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a>\_Classe Msvm EthernetSwitchPortMigrationQosSettingData

Representa as configurações de QOS VFP.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetSwitchPortMigrationQosSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetSwitchPortMigrationQosSettingData** tem essas propriedades.

<dl> <dt>

**InboundMaximumMbps**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O valor de limite de largura de banda para o tráfego de entrada.

</dd> <dt>

**OutboundMaximumMbps**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O valor de limite de largura de banda para o tráfego de saída.

</dd> <dt>

**OutboundReservedValue**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O valor de reserva de largura de banda.

</dd> <dt>

**Queueid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

A ID da fila de QOS.

</dd> <dt>

**Alternar \_ Defaultreservation**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O valor de reserva padrão.

</dd> <dt>

**Alternar \_ EnableHardwareLimits**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (5), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Indica se há uma tentativa de descarregamentos de hardware para limites, se disponível.

</dd> <dt>

**Alternar \_ EnableHardwareReservations**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (6), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Indica se há tentativas de descarregamentos de hardware para reservas, se disponíveis.

</dd> <dt>

**Alternar \_ EnableSoftwareReservations**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica se a reserva baseada em software está disponível.

</dd> <dt>

**Alternar \_ LinkSpeedPercentage**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

A porcentagem de velocidade do link a ser usada para reserva.

</dd> <dt>

**Alternar \_ reservamode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O modo de reserva de QOS no comutador.

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**Absoluto** (0)


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**Peso** (1)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

