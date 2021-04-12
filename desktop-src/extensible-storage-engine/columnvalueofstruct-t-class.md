---
description: 'Saiba mais sobre: <T> classe ColumnValueOfStruct'
title: Classe ColumnValueOfStruct(T)
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297867"
---
# <a name="columnvalueofstructt-class"></a>\<T\>Classe ColumnValueOfStruct

Defina uma coluna de um tipo de struct (por exemplo, Int32/GUID).

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. ESENT. Interop. Columnvalue](./columnvalue-class.md)  
    Microsoft. ISAM. ESENT. Interop. ColumnValueOfStruct\<T\>  
      

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a>Parâmetros de tipo

  - T  
    Digite para definir.

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do ColumnValueOfStruct \<T\>](./columnvalueofstruct-t-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. ESENT. Interop. Columnvalue](./columnvalue-class.md)  
    Microsoft. ISAM. ESENT. Interop. ColumnValueOfStruct\<T\>  
      [Microsoft. ISAM. ESENT. Interop. BoolColumnValue](./boolcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. ByteColumnValue](./bytecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. DateTimeColumnValue](./datetimecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. DoubleColumnValue](./doublecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. FloatColumnValue](./floatcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. GuidColumnValue](./guidcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int16ColumnValue](./int16columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int32ColumnValue](./int32columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int64ColumnValue](./int64columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt16ColumnValue](./uint16columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt32ColumnValue](./uint32columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt64ColumnValue](./uint64columnvalue-class.md)