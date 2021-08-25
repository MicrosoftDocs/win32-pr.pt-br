---
description: 'Saiba mais sobre: Classe EsentReadPgnoVerifyFailureException'
title: Classe EsentReadPgnoVerifyFailureException
TOCTitle: EsentReadPgnoVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadpgnoverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102553
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9bca310e9eae421bc930efc4616d6252f2612450ff6094071ce3b71b42b8b250
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835956"
---
# <a name="esentreadpgnoverifyfailureexception-class"></a>Classe EsentReadPgnoVerifyFailureException

Classe base para JET_err. Exceções ReadPgnoVerifyFailure.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadPgnoVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadPgnoVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadPgnoVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentReadPgnoVerifyFailureException](./esentreadpgnoverifyfailureexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
