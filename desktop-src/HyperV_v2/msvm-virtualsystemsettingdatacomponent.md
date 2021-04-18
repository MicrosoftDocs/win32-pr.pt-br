---
description: Uma associação genérica usada para estabelecer parte de relações entre uma instância do CIM \_ VirtualSystemSettingData e uma ou mais instâncias do CIM \_ ResourceAllocationSettingData.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Classe Msvm_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780972"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a>\_Classe Msvm VirtualSystemSettingDataComponent

Uma associação genérica usada para estabelecer a "parte de" relações entre uma instância do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) e uma ou mais instâncias do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemSettingDataComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemSettingDataComponent** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **override**, **min** (1), **Max** (1)
</dt> </dl>

O elemento pai na associação. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O elemento filho na associação. Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ VirtualSystemSettingDataComponent** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](/previous-versions//cc150674(v=vs.85))
</dt> <dt>

[Classes de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

