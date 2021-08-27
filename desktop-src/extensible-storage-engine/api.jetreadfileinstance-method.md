---
description: 'Saiba mais sobre: Método Api.JetReadFileInstance'
title: Método Api.JetReadFileInstance
TOCTitle: 'JetReadFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetreadfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100781
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ea64b78f36ac8dc29df7c98fa3f8c8ade484017d07dbc833b9809c766892b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977896"
---
# <a name="apijetreadfileinstance-method"></a>Método Api.JetReadFileInstance

Recupera o conteúdo de um arquivo aberto com [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetReadFileInstance ( _
    instance As JET_INSTANCE, _
    file As JET_HANDLE, _
    buffer As Byte(), _
    bufferSize As Integer, _
    <OutAttribute> ByRef bytesRead As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As JET_HANDLE
Dim buffer As Byte()
Dim bufferSize As Integer
Dim bytesRead As IntegerApi.JetReadFileInstance(instance, _
    file, buffer, bufferSize, bytesRead)
```

``` csharp
public static void JetReadFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE file,
    byte[] buffer,
    int bufferSize,
    out int bytesRead
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância a ser usada.

<!-- end list -->

  - file  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    O arquivo do o que ler.

<!-- end list -->

  - Buffer  
    Tipo: \[\]  
    
    O buffer no que ler.

<!-- end list -->

  - Buffersize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    O tamanho do buffer.

<!-- end list -->

  - Bytesread  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Retorna a quantidade de dados lidos no buffer.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
