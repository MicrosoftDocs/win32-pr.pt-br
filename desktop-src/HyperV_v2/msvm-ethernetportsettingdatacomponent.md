---
description: Uma associação usada para estabelecer &\# 0034;parte do&0034; relações entre uma instância de \# um Msvm EthernetPortAllocationSettingData e uma ou mais instâncias de \_ um Msvm \_ EthernetSwitchFeatureSettingData.
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Msvm_EthernetPortSettingDataComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 989d734d4c59d710c737c218b22591517347a8f5e434ff99e195887cbb4b6774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524836"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a>Classe Msvm \_ EthernetPortSettingDataComponent

Uma associação usada para estabelecer relações de "parte de" entre uma instância de [**um Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) e uma ou mais instâncias de [**um Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe \_ EthernetPortSettingDataComponent Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ EthernetPortSettingDataComponent Msvm** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ EthernetPortAllocationSettingData Msvm**](msvm-ethernetportallocationsettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Uma referência a uma instância da [**classe \_ EthernetPortAllocationSettingData Msvm**](msvm-ethernetportallocationsettingdata.md) que representa a porta Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ EthernetSwitchPortFeatureSettingData Msvm**](msvm-ethernetswitchportfeaturesettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representa as configurações de recurso aplicadas à porta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

