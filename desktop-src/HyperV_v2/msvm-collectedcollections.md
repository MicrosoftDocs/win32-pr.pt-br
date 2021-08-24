---
description: Msvm_CollectedCollections classe - associa a Msvm \_ VirtualSystemCollection aos objetos do ComputerSystem do Msvm \_ contidos.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c645bc4c6dbf7cf6f7b3fb43cc229af3ef744b264b088356d192e4ad58e68a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790176"
---
# <a name="msvm_collectedcollections-class"></a>Classe Msvm \_ CollectedCollections

Associa o [**\_ VirtualSystemCollection do Msvm**](msvm-virtualsystemcollection.md) aos objetos [**do Msvm \_ ComputerSystem**](msvm-computersystem.md) contidos.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ CollectedCollections** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ CollectedCollections** tem essas propriedades.

<dl> <dt>

**Coleção**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ ManagementCollection**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Agregar**](/windows/desktop/WmiSdk/standard-qualifiers), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Coleção")
</dt> </dl>

Um [**objeto Msvm \_ ManagementCollection**](msvm-managementcollection.md) ou 'bag' que representa a coleção.

</dd> <dt>

**Membro**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Coleção CIMOfMSEs**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Membro")
</dt> </dl>

Uma [**Coleção \_ CIMOfMSEs**](cim-collectionofmses.md) que contém os membros da coleção.

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

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> </dl>

 

