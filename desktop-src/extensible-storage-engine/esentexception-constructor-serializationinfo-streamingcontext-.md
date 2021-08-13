---
description: 'Saiba mais sobre: Construtor EsentException (SerializationInfo, StreamingContext)'
title: Construtor EsentException (SerializationInfo, StreamingContext) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f190f4a77d13cb4bc1e8a123dd1ec0f0b07498f2821a07d93a00372ecfaf32cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118778988"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a>Construtor EsentException (SerializationInfo, StreamingContext)

Inicializa uma nova instância da classe EsentException. Esse construtor é usado para desserializar uma exceção serializada.

**Namespace:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)  
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

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
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

[Classe EsentException](./esentexception-class.md)

[Membros do EsentException](./esentexception-members.md)

[Sobrecarga de EsentException](./esentexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)
