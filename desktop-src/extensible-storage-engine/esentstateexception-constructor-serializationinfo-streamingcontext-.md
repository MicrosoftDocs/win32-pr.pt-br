---
description: 'Saiba mais sobre: Construtor EsentStateException (SerializationInfo, StreamingContext)'
title: Construtor EsentStateException (SerializationInfo, StreamingContext)
TOCTitle: EsentStateException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102710
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458efcde030559122085824a99660c3d5d7fc4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297088"
---
# <a name="esentstateexception-constructor-serializationinfo-streamingcontext"></a>Construtor EsentStateException (SerializationInfo, StreamingContext)

Inicializa uma nova instância da classe EsentStateException. Esse construtor é usado para desserializar uma exceção serializada.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

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

Dim instance As New EsentStateException(info, context)
```

``` csharp
protected EsentStateException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parâmetros

  - informações  
    Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Os dados necessários para desserializar o objeto.

<!-- end list -->

  - contexto  
    Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    O contexto de desserialização.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe EsentStateException](./esentstateexception-class.md)

[Membros do EsentStateException](./esentstateexception-members.md)

[Sobrecarga de EsentStateException](./esentstateexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
