---
description: 'Saiba mais sobre: classe EsentInvalidLogDataSequenceException'
title: Classe EsentInvalidLogDataSequenceException
TOCTitle: EsentInvalidLogDataSequenceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogdatasequenceexception(v=EXCHG.10)
ms:contentKeyID: 55101973
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a37553555f5c89b191257fa84a7a751b11ad11ffae37ea0bc21ba06f249f5ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982258"
---
# <a name="esentinvalidlogdatasequenceexception-class"></a>Classe EsentInvalidLogDataSequenceException

Classe base para JET_err. InvalidLogDataSequence exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentInvalidLogDataSequenceException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogDataSequenceException _
    Inherits EsentStateException
'Usage
Dim instance As EsentInvalidLogDataSequenceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogDataSequenceException : EsentStateException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentInvalidLogDataSequenceException](./esentinvalidlogdatasequenceexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
