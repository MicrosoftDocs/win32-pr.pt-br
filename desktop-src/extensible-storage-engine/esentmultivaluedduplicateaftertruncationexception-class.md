---
description: 'Saiba mais sobre: Classe EsentMultiValuedDuplicateAfterTruncationException'
title: Classe EsentMultiValuedDuplicateAfterTruncationException
TOCTitle: EsentMultiValuedDuplicateAfterTruncationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedduplicateaftertruncationexception(v=EXCHG.10)
ms:contentKeyID: 55102259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05d00de435a7f8be2c860b73b4d58445bb7a22288fd4d27cc071c3f1ddb5c618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118264624"
---
# <a name="esentmultivaluedduplicateaftertruncationexception-class"></a>Classe EsentMultiValuedDuplicateAfterTruncationException

Classe base para JET_err. Exceções MultiValuedDuplicateAfterTruncation.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedDuplicateAfterTruncationException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMultiValuedDuplicateAfterTruncationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedDuplicateAfterTruncationException : EsentStateException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentMultiValuedDuplicateAfterTruncationException](./esentmultivaluedduplicateaftertruncationexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
