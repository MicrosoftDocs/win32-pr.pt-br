---
description: 'Saiba mais sobre: classe EsentSessionContextNotSetByThisThreadException'
title: Classe EsentSessionContextNotSetByThisThreadException
TOCTitle: EsentSessionContextNotSetByThisThreadException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioncontextnotsetbythisthreadexception(v=EXCHG.10)
ms:contentKeyID: 55102698
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 097712353336a9a412dd4255781a42c74eac1782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749910"
---
# <a name="esentsessioncontextnotsetbythisthreadexception-class"></a>Classe EsentSessionContextNotSetByThisThreadException

Classe base para JET_err. SessionContextNotSetByThisThread exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentSessionContextNotSetByThisThreadException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionContextNotSetByThisThreadException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionContextNotSetByThisThreadException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionContextNotSetByThisThreadException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentSessionContextNotSetByThisThreadException](./esentsessioncontextnotsetbythisthreadexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
