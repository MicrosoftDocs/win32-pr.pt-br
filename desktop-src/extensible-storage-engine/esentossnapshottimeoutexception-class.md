---
description: 'Saiba mais sobre: Classe EsentOSSnapshotTimeOutException'
title: Classe EsentOSSnapshotTimeOutException
TOCTitle: EsentOSSnapshotTimeOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentossnapshottimeoutexception(v=EXCHG.10)
ms:contentKeyID: 55102393
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b01b85c9b74dcd95bb6317e89011cf07bd3054a5d0192a52e208fbf5fd0d91c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835996"
---
# <a name="esentossnapshottimeoutexception-class"></a>Classe EsentOSSnapshotTimeOutException

Classe base para JET_err. Exceções OSSnapshotTimeOut.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOSSnapshotTimeOutException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentOSSnapshotTimeOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOSSnapshotTimeOutException : EsentOperationException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentOSSnapshotTimeOutException](./esentossnapshottimeoutexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
