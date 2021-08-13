---
description: 'Saiba mais sobre: Método Int64ColumnValue.GetValueFromBytes'
title: Método Int64ColumnValue.GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103365
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3479b629c3c791edf5d921427b7728d29ac5ffdf7ead02d1fe493fe8b7fa88e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476076"
---
# <a name="int64columnvaluegetvaluefrombytes-method"></a>Método Int64ColumnValue.GetValueFromBytes

Dados recuperados do ESENT, decodificar os dados e definir o valor no objeto ColumnValue.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Parâmetros

  - value  
    Tipo: \[\]  
    
    Uma matriz de bytes.

<!-- end list -->

  - startIndex  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    A posição inicial dentro dos bytes.

<!-- end list -->

  - count  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    O número de bytes a serem decodificados.

<!-- end list -->

  - Err  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    O erro retornado do ESENT.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Int64ColumnValue](./int64columnvalue-class.md)

[Membros Int64ColumnValue](./int64columnvalue-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
