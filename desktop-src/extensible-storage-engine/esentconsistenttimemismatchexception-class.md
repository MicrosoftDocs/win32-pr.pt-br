---
description: 'Saiba mais sobre: Classe EsentConsistentTimeMismatchException'
title: Classe EsentConsistentTimeMismatchException
TOCTitle: EsentConsistentTimeMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentconsistenttimemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101416
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e8980648eba45a2640ef90e899efe858cac803986db407d59a88823dfbb5590
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736666"
---
# <a name="esentconsistenttimemismatchexception-class"></a>Classe EsentConsistentTimeMismatchException

Classe base para JET_err. Exceções ConsistentTimeMismatch.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentConsistentTimeMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentConsistentTimeMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentConsistentTimeMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentConsistentTimeMismatchException](./esentconsistenttimemismatchexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
