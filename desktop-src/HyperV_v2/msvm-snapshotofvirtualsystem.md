---
description: Associa um sistema virtual a um instantâneo que foi capturado do sistema virtual.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Msvm_SnapshotOfVirtualSystem classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc1971c1123ab30fb88da9278b1d4f142e35785a393a75e1bf8a3ec69771f98a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950295"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a>Classe Msvm \_ SnapshotOfVirtualSystem

Associa um sistema virtual a um instantâneo que foi capturado do sistema virtual.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ SnapshotOfVirtualSystem** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ SnapshotOfVirtualSystem** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema virtual. Essa propriedade é derivada da Dependência [**CIM. \_**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência a uma instância da [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa o instantâneo. Essa propriedade é derivada da Dependência [**CIM. \_**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> </dl>

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

[**CIM \_ SnapshotOfVirtualSystem**](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[**CreateSnapshot**](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

