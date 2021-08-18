---
description: 'Saiba mais sobre: método Columnvalue. GetValueFromBytes'
title: Método columnvalue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101191
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eacd4b6468490e1d93f0d34fa5a941faa16d2d01607b85c3fc55cd668e21a2dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982636"
---
# <a name="columnvaluegetvaluefrombytes-method"></a>Método columnvalue. GetValueFromBytes

Dados obtidos recuperados do ESENT, decodifique os dados e defina o valor no objeto Columnvalue.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected MustOverride Sub GetValueFromBytes ( _
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
protected abstract void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Parâmetros

  - valor  
    Escreva \[\]  
    
    Uma matriz de bytes.

<!-- end list -->

  - startIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    A posição inicial dentro dos bytes.

<!-- end list -->

  - count  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O número de bytes a serem decodificados.

<!-- end list -->

  - erra  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O erro retornado de ESENT.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe columnvalue](./columnvalue-class.md)

[Membros de columnvalue](./columnvalue-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
