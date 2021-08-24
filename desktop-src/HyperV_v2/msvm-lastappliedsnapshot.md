---
description: Representa uma associação entre um sistema virtual e os dados de configuração do instantâneo que foi aplicado mais recentemente ao sistema virtual.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Msvm_LastAppliedSnapshot classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e34260e0bfe77b847437e9b3d49794334b3897d8425981fecb2032098e24fa7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521916"
---
# <a name="msvm_lastappliedsnapshot-class"></a>Classe Msvm \_ LastAppliedSnapshot

Representa uma associação entre um sistema virtual e os dados de configuração do instantâneo que foi aplicado mais recentemente ao sistema virtual.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ LastAppliedSnapshot** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ LastAppliedSnapshot** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Substituir**, **Min** ( 0 ), **Máx** . ( 1 )
</dt> </dl>

Referência a uma instância da [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa o instantâneo do sistema virtual que foi aplicado pela última vez ao sistema virtual. Essa propriedade é herdada da **\_ Dependência CIM.**

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ ComputerSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Substituir**, **Min** ( 0 ), **Máx** . ( 1 )
</dt> </dl>

Referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema virtual no qual o instantâneo do sistema virtual representado pela propriedade **Antecedent** foi aplicado mais recentemente. Essa propriedade é herdada da **\_ Dependência CIM.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




