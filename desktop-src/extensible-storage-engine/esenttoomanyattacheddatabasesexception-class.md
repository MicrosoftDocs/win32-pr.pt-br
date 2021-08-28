---
description: 'Saiba mais sobre: Classe EsentTooManyAttachedDatabasesException'
title: Classe EsentTooManyAttachedDatabasesException
TOCTitle: EsentTooManyAttachedDatabasesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyattacheddatabasesexception(v=EXCHG.10)
ms:contentKeyID: 55103075
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 567e8d138c2a145b15b9632ebe65602a49fa19d41a6c5b653ea5bf5b701b093d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668576"
---
# <a name="esenttoomanyattacheddatabasesexception-class"></a>Classe EsentTooManyAttachedDatabasesException

Classe base para JET_err. Exceções TooManyAttachedDatabases.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyAttachedDatabasesException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyAttachedDatabasesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyAttachedDatabasesException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentTooManyAttachedDatabasesException](./esenttoomanyattacheddatabasesexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
