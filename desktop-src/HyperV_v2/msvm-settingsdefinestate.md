---
description: Associa uma máquina virtual e seus dispositivos a instâncias do CIM \_ SettingData que representam as configurações atuais que se aplicam a esses objetos.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Classe Msvm_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170252"
---
# <a name="msvm_settingsdefinestate-class"></a>\_Classe Msvm SettingsDefineState

Associa uma máquina virtual e seus dispositivos a instâncias do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que representam as configurações atuais que se aplicam a esses objetos. Mais especificamente, ele associa o [**Msvm \_ ComputerSystem**](msvm-computersystem.md) a instâncias [**de Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)e associa **Msvm \_ \** _ derivados de [_ *CIM \_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) com **Msvm \_ \** _ derivados de [_ *CIM \_ ResourceAllocationSettingData*. *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SettingsDefineState** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ SettingsDefineState** tem essas propriedades.

<dl> <dt>

**Managedelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência à máquina virtual.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência às configurações ativas no momento para a máquina virtual.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ SettingsDefineState** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETTINGSDEFINESTATE CIM**](cim-settingsdefinestate.md)
</dt> <dt>

[**\_SETTINGSDEFINESTATE CIM**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Classes de gerenciamento do sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

