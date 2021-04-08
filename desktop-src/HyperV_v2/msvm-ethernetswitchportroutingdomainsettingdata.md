---
description: Representa os dados de configuração de domínio de roteamento.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Classe Msvm_EthernetSwitchPortRoutingDomainSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837515"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a>\_Classe Msvm EthernetSwitchPortRoutingDomainSettingData

Representa os dados de configuração de domínio de roteamento.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetSwitchPortRoutingDomainSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetSwitchPortRoutingDomainSettingData** tem essas propriedades.

<dl> <dt>

**IsolationIdList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (3), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

As IDs de VirtualSubnetId ou VLAN para os domínios de roteamento.

</dd> <dt>

**IsolationIdNameList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (4), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

A matriz de nome amigável VirtualSubnetId ou VLAN.

</dd> <dt>

**RoutingDomainGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

O GUID do domínio de roteamento.

</dd> <dt>

**RoutingDomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

O nome amigável do domínio de roteamento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

