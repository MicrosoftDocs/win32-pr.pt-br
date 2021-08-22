---
description: Uma associação usada para estabelecer relações entre uma instância de um Msvm \_ EmulatedEthernetPortSettingData e uma ou mais instâncias de um Msvm \_ EthernetSwitchFeatureSettingData.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Msvm_EthernetPortFailoverSettingDataComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00653b19cffabeb658e7727332b7e6fe1b2e23be7ff0c4eba298ef198404234c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531516"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a>Classe Msvm \_ EthernetPortFailoverSettingDataComponent

Uma associação usada para estabelecer relações entre uma instância de [**um Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) e uma ou mais instâncias de [**um Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe \_ EthernetPortFailoverSettingDataComponent Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ EthernetPortFailoverSettingDataComponent Msvm** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) ou [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) que representa a porta Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) que representa a configuração do adaptador de rede convidado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

