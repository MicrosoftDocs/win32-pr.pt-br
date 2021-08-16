---
description: 'Saiba mais sobre: JET_OBJECTINFO.objtyp'
title: JET_OBJECTINFO.objtyp
TOCTitle: 'objtyp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectinfo.objtyp(v=EXCHG.10)
ms:contentKeyID: 55103799
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.set_objtyp
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.get_objtyp
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f2abc54c2419b82ff6dc2469f46658bece41f39d4fe58a513abf5aef384e2eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979786"
---
# <a name="jet_objectinfoobjtyp-property"></a>JET_OBJECTINFO.objtyp

Obtém a JET_OBJTYP da tabela. Atualmente, somente tabelas serão retornadas (ou seja, [Tabela](./jet-objtyp-enumeration.md)).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property objtyp As JET_objtyp
    Get
    Private Set
'Usage
Dim instance As JET_OBJECTINFO
Dim value As JET_objtyp

value = instance.objtyp
```

``` csharp
public JET_objtyp objtyp { get; private set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_OBJECTINFO classe](./jet-objectinfo-class.md)

[JET_OBJECTINFO membros](./jet-objectinfo-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
