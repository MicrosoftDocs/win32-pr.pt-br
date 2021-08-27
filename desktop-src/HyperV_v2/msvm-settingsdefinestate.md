---
description: Associa uma máquina virtual e seus dispositivos a instâncias de Cim SettingData que representam as configurações atuais que \_ se aplicam a esses objetos.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState classe
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
ms.openlocfilehash: eea8a6cce263ddb3ad00ecd6951c1d5b47c6d98d58e99763b3f28780cb3438b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950455"
---
# <a name="msvm_settingsdefinestate-class"></a>Classe Msvm \_ SettingsDefineState

Associa uma máquina virtual e seus dispositivos a instâncias de [**Cim \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que representam as configurações atuais que se aplicam a esses objetos. Mais especificamente, ele associa [**msvm \_ ComputerSystem**](msvm-computersystem.md) a instâncias de [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)e associa **\_ \* Msvm* _ derivados de [_ CIM *\_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) a **\_ \* Msvm* _ derivados de _ CIM [*\_ ResourceAllocationSettingData* *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe Msvm \_ SettingsDefineState** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ SettingsDefineState** tem essas propriedades.

<dl> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência à máquina virtual.

</dd> <dt>

**Settingdata**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência às configurações ativas no momento para a máquina virtual.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe Msvm \_ SettingsDefineState** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações \_ cimDefineState**](cim-settingsdefinestate.md)
</dt> <dt>

[**Configurações \_ cimDefineState**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Classes de gerenciamento de sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

