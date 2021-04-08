---
description: Associa o Msvm \_ snapshotcollection aos objetos VirtualSystemCollection do Msvm correspondentes \_ .
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Classe Msvm_SnapshotOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827610"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a>\_Classe Msvm SnapshotOfVirtualSystemCollection

Associa o [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) aos objetos [**\_ VirtualSystemCollection do Msvm**](msvm-virtualsystemcollection.md) correspondentes.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SnapshotOfVirtualSystemCollection** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ SnapshotOfVirtualSystemCollection** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Um [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) que representa o objeto independente nessa associação.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ coleção CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Uma [**\_ coleção CIM**](cim-collection.md) que representa o objeto que é dependente do **Antecedent.**

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

 

