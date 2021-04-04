---
description: Associa o Msvm \_ VirtualSystemReferencePoint aos \_ objetos Msvm VirtualSystem correspondentes.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Classe Msvm_ReferencePointOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662287"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a>\_Classe Msvm ReferencePointOfVirtualSystem

Associa o [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) aos objetos [**Msvm \_ VirtualSystem**](msvm-virtualsystemresourcecomponent.md) correspondentes.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ReferencePointOfVirtualSystem** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ReferencePointOfVirtualSystem** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Um [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que representa o objeto independente nessa associação.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ VirtualSystemReferencePoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa o objeto que é dependente do **Antecedent**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

