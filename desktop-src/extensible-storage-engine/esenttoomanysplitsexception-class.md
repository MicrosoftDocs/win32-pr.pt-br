---
description: 'Saiba mais sobre: classe EsentTooManySplitsException'
title: Classe EsentTooManySplitsException
TOCTitle: EsentTooManySplitsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanysplitsexception(v=EXCHG.10)
ms:contentKeyID: 55103177
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fea122e5a5f40dd1a435a82f68d86766dc5518ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922750"
---
# <a name="esenttoomanysplitsexception-class"></a>Classe EsentTooManySplitsException

Classe base para JET_err. TooManySplits exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentTooManySplitsException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManySplitsException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentTooManySplitsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManySplitsException : EsentObsoleteException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentTooManySplitsException](./esenttoomanysplitsexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
