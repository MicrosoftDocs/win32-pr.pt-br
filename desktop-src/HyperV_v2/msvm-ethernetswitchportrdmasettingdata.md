---
description: Representa os dados de configuração do recurso RDMA da porta.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Classe Msvm_EthernetSwitchPortRdmaSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837516"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a>\_Classe Msvm EthernetSwitchPortRdmaSettingData

Representa os dados de configuração do recurso RDMA da porta.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetSwitchPortRdmaSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetSwitchPortRdmaSettingData** tem essas propriedades.

<dl> <dt>

**RdmaOffloadWeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

O peso atribuído a essa porta para RDMA de convidado. O peso é a importância relativa ao atribuir recursos RDMA. Definir a propriedade **RdmaOffloadWeight** como 0 DESABILITA o RDMA na porta. O padrão é 0.

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

 

 




