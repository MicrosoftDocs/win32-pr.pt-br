---
description: 'Saiba mais sobre: classe EsentSpaceHintsInvalidException'
title: Classe EsentSpaceHintsInvalidException
TOCTitle: EsentSpaceHintsInvalidException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspacehintsinvalidexception(v=EXCHG.10)
ms:contentKeyID: 55102857
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c24ff741428e7246f6147e87d7325542ee8c1449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297162"
---
# <a name="esentspacehintsinvalidexception-class"></a>Classe EsentSpaceHintsInvalidException

Classe base para JET_err. SpaceHintsInvalid exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentSpaceHintsInvalidException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSpaceHintsInvalidException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSpaceHintsInvalidException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSpaceHintsInvalidException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentSpaceHintsInvalidException](./esentspacehintsinvalidexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
