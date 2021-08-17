---
description: Representa uma associação entre uma instância do Msvm ComputerSystem que representa a máquina virtual e uma instância do \_ Msvm ReplicationRelationship que representa uma relação de replicação da \_ máquina virtual.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Msvm_SystemReplicationRelationship classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86040e6dc5676f6cd40b223f0a3cbd31864965722de957fda6ff1d140ad94b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810594"
---
# <a name="msvm_systemreplicationrelationship-class"></a>Classe \_ SystemReplicationRelationship Msvm

Representa uma associação entre uma instância do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual e uma instância do [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que representa uma relação de replicação da máquina virtual. Essa classe deriva da classe [**de \_ Dependência CIM.**](/windows/desktop/CIMWin32Prov/cim-dependency)

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe \_ SystemReplicationRelationship Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SystemReplicationRelationship Msvm** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Referência à instância da classe [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que representa a máquina virtual.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ ReplicationRelationship**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("DEPENDÊNCIA \_ CIM.Dependent")
</dt> </dl>

Referência à instância da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que representa a relação de replicação de um sistema virtual.

</dd> </dl>

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

[**Dependência cim \_**](cim-dependency.md)
</dt> <dt>

[**Dependência cim \_**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

