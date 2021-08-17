---
description: 'Saiba mais sobre: método Int16ColumnValue. GetValueFromBytes'
title: Método Int16ColumnValue. GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int16ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int16columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103359
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int16ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int16ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8ebbdd0eae4e91c3897a7bed1686f38c5ae234738bb0ae023a6296318fa8e5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362720"
---
# <a name="int16columnvaluegetvaluefrombytes-method"></a>Método Int16ColumnValue. GetValueFromBytes

Dados obtidos recuperados do ESENT, decodifique os dados e defina o valor no objeto Columnvalue.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

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

[Classe Int16ColumnValue](./int16columnvalue-class.md)

[Membros do Int16ColumnValue](./int16columnvalue-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
