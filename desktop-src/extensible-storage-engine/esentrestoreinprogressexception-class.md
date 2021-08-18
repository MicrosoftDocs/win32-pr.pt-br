---
description: 'Saiba mais sobre: classe EsentRestoreInProgressException'
title: Classe EsentRestoreInProgressException
TOCTitle: EsentRestoreInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrestoreinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55102631
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73f5e51f4ec88d19b55d799761bd23c3620417903a1fd912490c24467ec36a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115166"
---
# <a name="esentrestoreinprogressexception-class"></a>Classe EsentRestoreInProgressException

Classe base para JET_err. RestoreInProgress exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentRestoreInProgressException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRestoreInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRestoreInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRestoreInProgressException : EsentStateException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentRestoreInProgressException](./esentrestoreinprogressexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
