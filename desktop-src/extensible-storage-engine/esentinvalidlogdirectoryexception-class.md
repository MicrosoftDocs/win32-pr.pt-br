---
description: 'Saiba mais sobre: Classe EsentInvalidLogDirectoryException'
title: Classe EsentInvalidLogDirectoryException
TOCTitle: EsentInvalidLogDirectoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogdirectoryexception(v=EXCHG.10)
ms:contentKeyID: 55101985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de0eebb1386a1d2ac7d533d85a2200a3054b4c9569dce6c4fafb9fe9fa4fd551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118265599"
---
# <a name="esentinvalidlogdirectoryexception-class"></a>Classe EsentInvalidLogDirectoryException

Classe base para JET_err. Exceções InvalidLogDirectory.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogDirectoryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidLogDirectoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogDirectoryException : EsentObsoleteException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentInvalidLogDirectoryException](./esentinvalidlogdirectoryexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
