---
description: 'Saiba mais sobre: Classe EsentInvalidDatabaseVersionException'
title: Classe EsentInvalidDatabaseVersionException
TOCTitle: EsentInvalidDatabaseVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvaliddatabaseversionexception(v=EXCHG.10)
ms:contentKeyID: 55101922
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4823b4135a0be6a20c6f7d73043b9ad7aaa120fb2813701c6e7686bdf8e5f777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837416"
---
# <a name="esentinvaliddatabaseversionexception-class"></a>Classe EsentInvalidDatabaseVersionException

Classe base para JET_err. Exceções InvalidDatabaseVersion.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidDatabaseVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentInvalidDatabaseVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidDatabaseVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentInvalidDatabaseVersionException](./esentinvaliddatabaseversionexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
