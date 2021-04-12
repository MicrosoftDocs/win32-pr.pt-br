---
description: 'Saiba mais sobre: Construtor EsentFragmentationException (SerializationInfo, StreamingContext)'
title: Construtor EsentFragmentationException (SerializationInfo, StreamingContext)
TOCTitle: EsentFragmentationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101633
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 251e4beaacb1e895c1da1d501b38cf03f211dd99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297753"
---
# <a name="esentfragmentationexception-constructor-serializationinfo-streamingcontext"></a>Construtor EsentFragmentationException (SerializationInfo, StreamingContext)

Inicializa uma nova instância da classe EsentFragmentationException. Esse construtor é usado para desserializar uma exceção serializada.

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

Dim instance As New EsentFragmentationException(info, context)
```

``` csharp
protected EsentFragmentationException(
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

[Classe EsentFragmentationException](./esentfragmentationexception-class.md)

[Membros do EsentFragmentationException](./esentfragmentationexception-members.md)

[Sobrecarga de EsentFragmentationException](./esentfragmentationexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
