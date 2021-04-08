---
description: 'Saiba mais sobre: classe EsentMemoryException'
title: Classe EsentMemoryException
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103837567"
---
# <a name="esentmemoryexception-class"></a>Classe EsentMemoryException

Classe base para exceções de memória.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentResourceException](./esentresourceexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentMemoryException  
              

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentMemoryException](./esentmemoryexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentResourceException](./esentresourceexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentMemoryException  
              [Microsoft. ISAM. ESENT. Interop. EsentOutOfBuffersException](./esentoutofbuffersexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. EsentOutOfCursorsException](./esentoutofcursorsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. EsentOutOfFileHandlesException](./esentoutoffilehandlesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. EsentOutOfMemoryException](./esentoutofmemoryexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. EsentOutOfSessionsException](./esentoutofsessionsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. EsentOutOfThreadsException](./esentoutofthreadsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. EsentTooManyMempoolEntriesException](./esenttoomanymempoolentriesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. EsentTooManyOpenIndexesException](./esenttoomanyopenindexesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. EsentTooManySortsException](./esenttoomanysortsexception-class.md)