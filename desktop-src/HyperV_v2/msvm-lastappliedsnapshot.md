---
description: Representa uma associação entre um sistema virtual e os dados de configuração do instantâneo que foi aplicado mais recentemente ao sistema virtual.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Classe Msvm_LastAppliedSnapshot
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
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783292"
---
# <a name="msvm_lastappliedsnapshot-class"></a>\_Classe Msvm LastAppliedSnapshot

Representa uma associação entre um sistema virtual e os dados de configuração do instantâneo que foi aplicado mais recentemente ao sistema virtual.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

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

A classe **Msvm \_ LastAppliedSnapshot** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ LastAppliedSnapshot** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **override**, **min** (0), **Max** (1)
</dt> </dl>

Referência a uma instância da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa o instantâneo do sistema virtual que foi aplicado pela última vez ao sistema virtual. Essa propriedade é herdada **da \_ dependência CIM**.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **override**, **min** (0), **Max** (1)
</dt> </dl>

Referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema virtual no qual o instantâneo do sistema virtual representado pela propriedade **Antecedent** foi aplicado mais recentemente. Essa propriedade é herdada **da \_ dependência CIM**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




