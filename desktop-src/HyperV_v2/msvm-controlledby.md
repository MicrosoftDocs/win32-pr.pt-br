---
description: Associa um dispositivo de armazenamento ao controlador de armazenamento que possui o dispositivo.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Msvm_ControlledBy classe
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
ms.openlocfilehash: b08cf97c54363009e839ea78fe139c6c8a1bdd81cac07182d019d3d00857dee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130596"
---
# <a name="msvm_controlledby-class"></a>Classe Msvm \_ ControlledBy

Associa um dispositivo de armazenamento ao controlador de armazenamento que possui o dispositivo. Essa associação é usada com controladores IDE e disquete.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe Msvm \_ ControlledBy** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ ControlledBy** tem essas propriedades.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A acessibilidade do dispositivo por meio do controlador antecessor. Essa propriedade é herdada [**de CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 2 (leitura/gravação).

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A prioridade dada aos acessos do dispositivo por meio desse controlador. O caminho de prioridade mais alta terá o valor mais baixo. Essa propriedade é herdada [**de CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 0.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o controlador está ativamente no comando ou acessando o dispositivo. Essa propriedade é herdada [**de CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 1 (Ativa).

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Controlador CIM \_**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao controlador. Essa propriedade é herdada de [**CIM \_ ControlledBy.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao dispositivo controlado. Essa propriedade é herdada de [**CIM \_ ControlledBy.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço do dispositivo associado no contexto do controlador antecessor. Essa propriedade é herdada de [**CIM \_ ControlledBy.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada de [**\_ DeviceConnection cim**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)e é sempre definida como 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada de [**\_ DeviceConnection cim**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)e é sempre definida como 0.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada [**de CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada [**de CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.

</dd> <dt>

**TimeOfDeviceReset**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada [**de CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe Msvm \_ ControlledBy** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Armazenamento Classes](storage-classes.md)
</dt> </dl>

 

