---
description: 'Saiba mais sobre: Classe EsentLogTornWriteDuringHardRestoreException'
title: Classe EsentLogTornWriteDuringHardRestoreException
TOCTitle: EsentLogTornWriteDuringHardRestoreException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogtornwriteduringhardrestoreexception(v=EXCHG.10)
ms:contentKeyID: 55102166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0121041f2ae0c898358ff2b1d01a86dbf6b00e458ee9c56d02fa89a4086f430f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118080274"
---
# <a name="esentlogtornwriteduringhardrestoreexception-class"></a>Classe EsentLogTornWriteDuringHardRestoreException

Classe base para JET_err. Exceções LogTornWriteDuringHardRestore.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogTornWriteDuringHardRestoreException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogTornWriteDuringHardRestoreException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogTornWriteDuringHardRestoreException : EsentCorruptionException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentLogTornWriteDuringHardRestoreException](./esentlogtornwriteduringhardrestoreexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
