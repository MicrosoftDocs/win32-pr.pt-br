---
description: Associa uma porta serial a um controlador serial.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Msvm_SerialPortOnSerialController classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ddc5a5c006b92945178f89cf5f4df585f96ed3eaef692b04326878cb0d16520
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107436"
---
# <a name="msvm_serialportonserialcontroller-class"></a>Classe Msvm \_ SerialPortOnSerialController

Associa uma porta serial a um controlador serial.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ SerialPortOnSerialController** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ SerialPortOnSerialController** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O controlador serial ao qual a porta está conectada. Essa propriedade é herdada [**de Cim \_ PortOnDevice.**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A porta do controlador serial. Essa propriedade é herdada [**de Cim \_ PortOnDevice.**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe \_ SerialPortOnSerialController do Msvm** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ PortOnDevice**](cim-portondevice.md)
</dt> <dt>

[**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[Classes de dispositivos seriais](serial-devices-classes.md)
</dt> </dl>

 

