---
description: 'Saiba mais sobre: classe EsentFixedDDLException'
title: Classe EsentFixedDDLException
TOCTitle: EsentFixedDDLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFixedDDLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfixedddlexception(v=EXCHG.10)
ms:contentKeyID: 55101723
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFixedDDLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFixedDDLException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 181c8ba1786202290d9efa32f811f7ad92b6ad2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813534"
---
# <a name="esentfixedddlexception-class"></a>Classe EsentFixedDDLException

Classe base para JET_err. FixedDDL exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentFixedDDLException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFixedDDLException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFixedDDLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFixedDDLException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentFixedDDLException](./esentfixedddlexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
