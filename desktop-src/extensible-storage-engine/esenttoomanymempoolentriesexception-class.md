---
description: 'Saiba mais sobre: classe EsentTooManyMempoolEntriesException'
title: Classe EsentTooManyMempoolEntriesException
TOCTitle: EsentTooManyMempoolEntriesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanymempoolentriesexception(v=EXCHG.10)
ms:contentKeyID: 55103097
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e134f4b976ee0a2ed7ffe51e71e9a7e2c929180ba1de7e5ac63d44a7793c624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093776"
---
# <a name="esenttoomanymempoolentriesexception-class"></a>Classe EsentTooManyMempoolEntriesException

Classe base para JET_err. TooManyMempoolEntries exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMemoryException](./esentmemoryexception-class.md)  
              Microsoft. ISAM. ESENT. Interop. EsentTooManyMempoolEntriesException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyMempoolEntriesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyMempoolEntriesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyMempoolEntriesException : EsentMemoryException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentTooManyMempoolEntriesException](./esenttoomanymempoolentriesexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
