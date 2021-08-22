---
description: 'Saiba mais sobre: Construtor EsentMemoryException (SerializationInfo, StreamingContext)'
title: Construtor EsentMemoryException (SerializationInfo, StreamingContext)
TOCTitle: EsentMemoryException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102121
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51ac6b24c2b50e33f7b805705de193140c9b0657ad07390cf534d47bb143aef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115597"
---
# <a name="esentmemoryexception-constructor-serializationinfo-streamingcontext"></a>Construtor EsentMemoryException (SerializationInfo, StreamingContext)

Inicializa uma nova instância da classe EsentMemoryException. Esse construtor é usado para desserlizar uma exceção serializada.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentMemoryException(info, context)
```

``` csharp
protected EsentMemoryException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parâmetros

  - informações  
    Tipo: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Os dados necessários para desterlizar o objeto.

<!-- end list -->

  - contexto  
    Tipo: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    O contexto de desserialização.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe EsentMemoryException](./esentmemoryexception-class.md)

[Membros EsentMemoryException](./esentmemoryexception-members.md)

[Sobrecarga EsentMemoryException](./esentmemoryexception-constructor.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
