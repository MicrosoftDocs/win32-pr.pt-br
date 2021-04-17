---
description: Associa um dispositivo de armazenamento ao controlador de armazenamento que possui o dispositivo.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Classe Msvm_ControlledBy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812944"
---
# <a name="msvm_controlledby-class"></a>\_Classe Msvm ControlledBy

Associa um dispositivo de armazenamento ao controlador de armazenamento que possui o dispositivo. Essa associação é usada com controladores IDE e de disquete.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ControlledBy** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ControlledBy** tem essas propriedades.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A acessibilidade do dispositivo por meio do controlador Antecedent. Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 2 (leitura/gravação).

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A prioridade fornecida para acessar o dispositivo por meio desse controlador. O caminho de prioridade mais alta terá o menor valor. Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 0.

</dd> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o controlador está ativando ou acessando ativamente o dispositivo. Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 1 (ativa).

</dd> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao controlador. Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao dispositivo controlado. Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço do dispositivo associado no contexto do controlador Antecedent. Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada do [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)e é sempre definida como 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada do [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)e é sempre definida como 0.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.

</dd> <dt>

**TimeOfDeviceReset**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ ControlledBy** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[**\_CONTROLLEDBY CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Classes de armazenamento](storage-classes.md)
</dt> </dl>

 

