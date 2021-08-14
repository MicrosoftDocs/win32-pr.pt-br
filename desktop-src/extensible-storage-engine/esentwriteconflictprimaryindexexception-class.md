---
description: 'Saiba mais sobre: Classe EsentWriteConflictPrimaryIndexException'
title: Classe EsentWriteConflictPrimaryIndexException
TOCTitle: EsentWriteConflictPrimaryIndexException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentwriteconflictprimaryindexexception(v=EXCHG.10)
ms:contentKeyID: 55107366
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1cbe1c5cadcc0a19354d6eec9f19f78c996cd333763029f5ce6f911d0a9263
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119233986"
---
# <a name="esentwriteconflictprimaryindexexception-class"></a>Classe EsentWriteConflictPrimaryIndexException

Classe base para JET_err. Exceções WriteConflictPrimaryIndex.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentWriteConflictPrimaryIndexException _
    Inherits EsentStateException
'Usage
Dim instance As EsentWriteConflictPrimaryIndexException
```

``` csharp
[SerializableAttribute]
public sealed class EsentWriteConflictPrimaryIndexException : EsentStateException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentWriteConflictPrimaryIndexException](./esentwriteconflictprimaryindexexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
