---
description: 'Saiba mais sobre: classe EsentDatabaseInvalidPagesException'
title: Classe EsentDatabaseInvalidPagesException
TOCTitle: EsentDatabaseInvalidPagesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPagesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinvalidpagesexception(v=EXCHG.10)
ms:contentKeyID: 55101388
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPagesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPagesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e7372526f27386b2b83623dbbe721159ce08cffd537ad17888e671727a9e0b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974716"
---
# <a name="esentdatabaseinvalidpagesexception-class"></a>Classe EsentDatabaseInvalidPagesException

Classe base para JET_err. DatabaseInvalidPages exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentDatabaseInvalidPagesException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInvalidPagesException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInvalidPagesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInvalidPagesException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentDatabaseInvalidPagesException](./esentdatabaseinvalidpagesexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
