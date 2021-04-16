---
description: 'Saiba mais sobre: classe EsentRollbackErrorException'
title: Classe EsentRollbackErrorException
TOCTitle: EsentRollbackErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackerrorexception(v=EXCHG.10)
ms:contentKeyID: 55102663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e56e3e829b8c44ff6325ed877606fb44471f6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765141"
---
# <a name="esentrollbackerrorexception-class"></a>Classe EsentRollbackErrorException

Classe base para JET_err. RollbackError exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentFatalException](./esentfatalexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentRollbackErrorException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackErrorException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentRollbackErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackErrorException : EsentFatalException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentRollbackErrorException](./esentrollbackerrorexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
