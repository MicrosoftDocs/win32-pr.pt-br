---
description: 'Saiba mais sobre: classe EsentTempFileOpenErrorException'
title: Classe EsentTempFileOpenErrorException
TOCTitle: EsentTempFileOpenErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttempfileopenerrorexception(v=EXCHG.10)
ms:contentKeyID: 55103029
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3a27657218fa5f705356945769d28fe6579b6a89fd26c1cf1da1d8e813e2220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118768909"
---
# <a name="esenttempfileopenerrorexception-class"></a>Classe EsentTempFileOpenErrorException

Classe base para JET_err. Exceções TempFileOpenError.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTempFileOpenErrorException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentTempFileOpenErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTempFileOpenErrorException : EsentObsoleteException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentTempFileOpenErrorException](./esenttempfileopenerrorexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
