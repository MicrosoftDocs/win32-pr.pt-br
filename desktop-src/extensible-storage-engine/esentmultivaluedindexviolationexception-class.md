---
description: 'Saiba mais sobre: Classe EsentMultiValuedIndexViolationException'
title: Classe EsentMultiValuedIndexViolationException
TOCTitle: EsentMultiValuedIndexViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedindexviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102266
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13a49ebdc4036ec4d263304a918de63c3d4a33a1bc54f94bb58630e49333520c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118264013"
---
# <a name="esentmultivaluedindexviolationexception-class"></a>Classe EsentMultiValuedIndexViolationException

Classe base para JET_err. Exceções MultiValuedIndexViolation.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedIndexViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMultiValuedIndexViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedIndexViolationException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentMultiValuedIndexViolationException](./esentmultivaluedindexviolationexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
