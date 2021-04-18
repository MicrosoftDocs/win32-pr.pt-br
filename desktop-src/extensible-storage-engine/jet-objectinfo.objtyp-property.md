---
description: 'Saiba mais sobre a propriedade: JET_OBJECTINFO. objtyp'
title: Propriedade JET_OBJECTINFO. objtyp
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
ms.openlocfilehash: 541a9b3561c43a9b339c731a1b93302e6c8c46a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798227"
---
# <a name="jet_objectinfoobjtyp-property"></a>Propriedade JET_OBJECTINFO. objtyp

Obtém a JET_OBJTYP da tabela. No momento, apenas tabelas serão retornadas (ou seja, [tabela](./jet-objtyp-enumeration.md)).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_objtyp](./jet-objtyp-enumeration.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_OBJECTINFO](./jet-objectinfo-class.md)

[Membros do JET_OBJECTINFO](./jet-objectinfo-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
