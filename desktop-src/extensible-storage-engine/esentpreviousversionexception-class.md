---
description: 'Saiba mais sobre: classe EsentPreviousVersionException'
title: Classe EsentPreviousVersionException
TOCTitle: EsentPreviousVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpreviousversionexception(v=EXCHG.10)
ms:contentKeyID: 55102535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 803a019a531caf97888cf6f7067fba665447d8aaafa25e2e6016b219214ae9ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971476"
---
# <a name="esentpreviousversionexception-class"></a>Classe EsentPreviousVersionException

Classe base para JET_err. PreviousVersion exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        Microsoft. ISAM. ESENT. Interop. EsentPreviousVersionException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPreviousVersionException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentPreviousVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPreviousVersionException : EsentErrorException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentPreviousVersionException](./esentpreviousversionexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
