---
description: 'Saiba mais sobre: classe EsentBadItagSequenceException'
title: Classe EsentBadItagSequenceException
TOCTitle: EsentBadItagSequenceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbaditagsequenceexception(v=EXCHG.10)
ms:contentKeyID: 55107257
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f640aea27e0ddb3620b88c8d3c77acc0060c68eae9469f5e87e4f6d58586b980
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117166"
---
# <a name="esentbaditagsequenceexception-class"></a>Classe EsentBadItagSequenceException

Classe base para JET_err. BadItagSequence exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentBadItagSequenceException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadItagSequenceException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBadItagSequenceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadItagSequenceException : EsentStateException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentBadItagSequenceException](./esentbaditagsequenceexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
