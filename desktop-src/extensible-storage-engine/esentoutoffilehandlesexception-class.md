---
description: 'Saiba mais sobre: classe EsentOutOfFileHandlesException'
title: Classe EsentOutOfFileHandlesException
TOCTitle: EsentOutOfFileHandlesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutoffilehandlesexception(v=EXCHG.10)
ms:contentKeyID: 55102419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1de85dd0bd4edc6a64b638b095e327ce36859d354bfeca42b1179e6338b83159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118492623"
---
# <a name="esentoutoffilehandlesexception-class"></a>Classe EsentOutOfFileHandlesException

Classe base para JET_err. OutOfFileHandles exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMemoryException](./esentmemoryexception-class.md)  
              Microsoft. ISAM. ESENT. Interop. EsentOutOfFileHandlesException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfFileHandlesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfFileHandlesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfFileHandlesException : EsentMemoryException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentOutOfFileHandlesException](./esentoutoffilehandlesexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
