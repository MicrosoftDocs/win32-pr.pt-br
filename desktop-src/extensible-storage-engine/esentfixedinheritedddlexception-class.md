---
description: 'Saiba mais sobre: classe EsentFixedInheritedDDLException'
title: Classe EsentFixedInheritedDDLException
TOCTitle: EsentFixedInheritedDDLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfixedinheritedddlexception(v=EXCHG.10)
ms:contentKeyID: 55101724
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f8638b396848503819635860b7472a8af684c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797607"
---
# <a name="esentfixedinheritedddlexception-class"></a>Classe EsentFixedInheritedDDLException

Classe base para JET_err. FixedInheritedDDL exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentFixedInheritedDDLException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFixedInheritedDDLException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFixedInheritedDDLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFixedInheritedDDLException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentFixedInheritedDDLException](./esentfixedinheritedddlexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
