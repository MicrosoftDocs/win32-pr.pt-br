---
description: Representa os dados de configuração do recurso de mapeamento da equipe de porta.
ms.assetid: 7c9a392d-c95e-4b0d-8201-e50adabd21b2
title: Classe Msvm_EthernetSwitchPortTeamMappingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortTeamMappingSettingData
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterName
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterDeviceId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f0d7385499dcdf6e84c361de03950a4e78be0a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755102"
---
# <a name="msvm_ethernetswitchportteammappingsettingdata-class"></a>\_Classe Msvm EthernetSwitchPortTeamMappingSettingData

Representa os dados de configuração do recurso de mapeamento da equipe de porta.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8D45D4BD-8C18-435C-98A7-D632A7C618FF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Team Mapping Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortTeamMappingSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string NetAdapterName = "";
  string NetAdapterDeviceId = "";
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetSwitchPortTeamMappingSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetSwitchPortTeamMappingSettingData** tem essas propriedades.

<dl> <dt>

**NetAdapterDeviceId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

ID do dispositivo do adaptador físico mapeado preferencial.

</dd> <dt>

**Netadaptadorname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Nome do adaptador físico mapeado preferencial.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

