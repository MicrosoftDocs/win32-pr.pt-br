---
description: Associa o Msvm \_ SnapshotCollection aos objetos VirtualSystemCollection da Msvm \_ correspondentes.
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Msvm_SnapshotOfVirtualSystemCollection classe
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
ms.openlocfilehash: 151a54c99376cdf7d9e5f2e14fa0fd3c903d3659c12310212304a1a2b2f2e339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950245"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a>Classe Msvm \_ SnapshotOfVirtualSystemCollection

Associa o [**Msvm \_ SnapshotCollection aos**](msvm-snapshotcollection.md) objetos [**\_ VirtualSystemCollection da Msvm**](msvm-virtualsystemcollection.md) correspondentes.

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

A **classe Msvm \_ SnapshotOfVirtualSystemCollection** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ SnapshotOfVirtualSystemCollection** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Coleção CIMOfMSEs**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecessor")
</dt> </dl>

Uma [**Coleção \_ CIMOfMSEs**](cim-collectionofmses.md) que representa o objeto independente nessa associação.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Coleção CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Uma [**Coleção CIM \_**](cim-collection.md) que representa o objeto que depende do **Antecessor.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

