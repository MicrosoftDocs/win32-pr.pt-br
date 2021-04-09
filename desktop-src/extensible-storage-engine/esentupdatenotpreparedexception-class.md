---
description: 'Saiba mais sobre: classe EsentUpdateNotPreparedException'
title: Classe EsentUpdateNotPreparedException
TOCTitle: EsentUpdateNotPreparedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUpdateNotPreparedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentupdatenotpreparedexception(v=EXCHG.10)
ms:contentKeyID: 55107339
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUpdateNotPreparedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUpdateNotPreparedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f952c6448ddbd1eae30d92f5a482392b5d83f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922854"
---
# <a name="esentupdatenotpreparedexception-class"></a>Classe EsentUpdateNotPreparedException

Classe base para JET_err. UpdateNotPrepared exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentUpdateNotPreparedException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUpdateNotPreparedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentUpdateNotPreparedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUpdateNotPreparedException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentUpdateNotPreparedException](./esentupdatenotpreparedexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
