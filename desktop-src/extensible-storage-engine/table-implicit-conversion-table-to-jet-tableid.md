---
description: 'Saiba mais sobre: conversão implícita de tabela (tabela para JET_TABLEID)'
title: Conversão implícita de tabela (tabela para JET_TABLEID)
TOCTitle: Implicit conversion (Table to JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.op_Implicit(Microsoft.Isam.Esent.Interop.Table)~Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104156
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table.Implicit
- Microsoft.Isam.Esent.Interop.Table.op_Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f5085ee09020730b36269255279836b31562a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772755"
---
# <a name="table-implicit-conversion-table-to-jet_tableid"></a>Conversão implícita de tabela (tabela para JET_TABLEID)

Operador de conversão implícita de uma tabela para um JET_TABLEID. Isso permite que uma tabela seja usada com APIs que esperam um JET_TABLEID.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    table As Table _
) As JET_TABLEID
'Usage
Dim input As Table
Dim output As JET_TABLEID

output = CType(input, JET_TABLEID)
```

``` csharp
public static implicit operator JET_TABLEID (
    Table table
)
```

#### <a name="parameters"></a>Parâmetros

  - table  
    Tipo: [Microsoft. ISAM. ESENT. Interop. Table](./table-class.md)  
    
    A tabela a ser convertida.

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
O JET_TABLEID da tabela.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de tabela](./table-class.md)

[Membros da tabela](./table-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
