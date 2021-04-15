---
description: 'Saiba mais sobre: Construtor EsentApiException (SerializationInfo, StreamingContext)'
title: Construtor EsentApiException (SerializationInfo, StreamingContext)
TOCTitle: EsentApiException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101059
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a00204c254378956521a1ae5fe02480dd879c832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461348"
---
# <a name="esentapiexception-constructor-serializationinfo-streamingcontext"></a>Construtor EsentApiException (SerializationInfo, StreamingContext)

Inicializa uma nova instância da classe EsentApiException. Esse construtor é usado para desserializar uma exceção serializada.

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

Dim instance As New EsentApiException(info, context)
```

``` csharp
protected EsentApiException(
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

[Classe EsentApiException](./esentapiexception-class.md)

[Membros do EsentApiException](./esentapiexception-members.md)

[Sobrecarga de EsentApiException](./esentapiexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
