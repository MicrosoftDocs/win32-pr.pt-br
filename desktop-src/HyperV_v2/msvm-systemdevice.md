---
description: Associa um dispositivo lógico ao sistema pai.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Msvm_SystemDevice classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67c538d82657d1ac07246f21dc2688f968ce969d1bf20238b20eeb4eea6f71cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746566"
---
# <a name="msvm_systemdevice-class"></a>Classe SystemDevice Msvm \_

Os dispositivos lógicos podem ser agregados por um sistema. Essa relação é explicitada pela associação de dispositivo do sistema.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe \_ SystemDevice Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SystemDevice Msvm** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Máx**](/windows/desktop/WmiSdk/standard-qualifiers) . ( 1 )
</dt> </dl>

O sistema pai na associação. Essa propriedade é herdada do [**componente CIM \_**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O dispositivo lógico que é um elemento de um sistema. Essa propriedade é herdada do [**componente CIM \_**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe \_ SystemDevice do Msvm** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ SystemDevice**](cim-systemdevice.md)
</dt> <dt>

[**CIM \_ SystemDevice**](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[Classes do sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

