---
description: 'Saiba mais sobre: Método ColumnStream.Read'
title: Método ColumnStream.Read
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 34c2bd13a2cc436ea192433e4f70098e328d1658a484c5dca9b092fe18f99a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976616"
---
# <a name="columnstreamread-method"></a>Método ColumnStream.Read

Lê uma sequência de bytes do fluxo atual e avança a posição no fluxo até o número de bytes lidos.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>Parâmetros

  - Buffer  
    Tipo: \[\]  
    
    O buffer no que ler.

<!-- end list -->

  - deslocamento  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    O deslocamento no buffer para o que ler.

<!-- end list -->

  - count  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    O número de bytes a serem lidos.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.Int32](/dotnet/api/system.int32)  
O número de bytes lidos no buffer.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe ColumnStream](./columnstream-class.md)

[Membros de ColumnStream](./columnstream-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
