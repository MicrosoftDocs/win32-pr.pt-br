---
description: Associa o Msvm \_ ReferencePointCollection aos objetos \_ VirtualSystemReferencePoint contidos no Msvm.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Msvm_CollectedReferencePoints classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e68c0eb64bd1550966963d9913fd734a7672cbef051bd21281e61e7777ca4857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149286"
---
# <a name="msvm_collectedreferencepoints-class"></a>Classe Msvm \_ CollectedReferencePoints

Associa o [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) aos objetos [**\_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) contidos no Msvm.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ CollectedReferencePoints** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ CollectedReferencePoints** tem essas propriedades.

<dl> <dt>

**Coleção**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ ReferencePointCollection**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Agregar**](/windows/desktop/WmiSdk/standard-qualifiers), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Coleção")
</dt> </dl>

Um [**objeto Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) ou 'bag' que representa a coleção.

</dd> <dt>

**Membro**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ VirtualSystemReferencePoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Membro")
</dt> </dl>

Um [**\_ VirtualSystemReferencePoint Msvm**](msvm-virtualsystemreferencepoint.md) que contém os membros da coleção.

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

 

