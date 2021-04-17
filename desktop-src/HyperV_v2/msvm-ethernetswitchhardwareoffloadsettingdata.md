---
description: Representa as configurações de descarregamento de comutador.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Classe Msvm_EthernetSwitchHardwareOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760853"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a>\_Classe Msvm EthernetSwitchHardwareOffloadSettingData

Representa as configurações de descarregamento de comutador.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetSwitchHardwareOffloadSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetSwitchHardwareOffloadSettingData** tem essas propriedades.

<dl> <dt>

**DefaultQueueVmmqEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica as configurações de VMMQ para a fila padrão do vSwitch.

</dd> <dt>

**DefaultQueueVmmqQueuePairs**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica o número de filas para a fila padrão.

</dd> <dt>

**DefaultQueueVrssEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica as configurações de VRss para a fila padrão do vSwitch.

</dd> <dt>

**DefaultQueueVrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica se a CPU de VMQ primária foi excluída da tabela de indireção VRSS/VMMQ.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**DefaultQueueVrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica se a difusão do VRSS deve ser sempre feita para a fila padrão, independentemente do estado de RSS do vPort externo.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**DefaultQueueVrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica o número mínimo de filas usadas para VRSS/VMMQ.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**DefaultQueueVrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica como as filas VRSS/VMMQ são direcionadas para processadores de host diferentes.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

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

[**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




