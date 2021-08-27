---
description: Representa uma associação entre uma instância da classe de \_ ComputerSystem do CIM que representa a réplica da máquina virtual e uma instância da \_ classe de COMPUTERSYSTEM do CIM que representa a réplica da máquina virtual de teste.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Classe Msvm_ReplicaSystemDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f6bb3f4879ee0e1c7babaf8f85b8455716ee1b2e61db4e0764d6b28583efefd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130426"
---
# <a name="msvm_replicasystemdependency-class"></a>\_Classe Msvm ReplicaSystemDependency

Representa uma associação entre uma instância da classe [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a réplica da máquina virtual e uma instância da classe de **\_ ComputerSystem do CIM** que representa a réplica da máquina virtual de teste.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ReplicaSystemDependency** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ReplicaSystemDependency** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")
</dt> </dl>

Uma referência a uma instância da classe [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a réplica da máquina virtual. Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")
</dt> </dl>

Uma referência a uma instância da classe [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a réplica da máquina virtual de teste criada pelo método [**Msvm \_ ReplicationService. TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) . Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

