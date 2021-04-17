---
description: 'Saiba mais sobre: classe EsentKeyNotMadeException'
title: Classe EsentKeyNotMadeException
TOCTitle: EsentKeyNotMadeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeynotmadeexception(v=EXCHG.10)
ms:contentKeyID: 55102115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e77be995e6f06aaa7058455f9e0f64bd9721f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763098"
---
# <a name="esentkeynotmadeexception-class"></a>Classe EsentKeyNotMadeException

Classe base para JET_err. KeyNotMade exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentKeyNotMadeException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyNotMadeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentKeyNotMadeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyNotMadeException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentKeyNotMadeException](./esentkeynotmadeexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
