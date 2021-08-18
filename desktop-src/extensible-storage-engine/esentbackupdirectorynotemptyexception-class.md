---
description: 'Saiba mais sobre: Classe EsentBackupDirectoryNotEmptyException'
title: Classe EsentBackupDirectoryNotEmptyException
TOCTitle: EsentBackupDirectoryNotEmptyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupdirectorynotemptyexception(v=EXCHG.10)
ms:contentKeyID: 55101028
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7147fc0bec897fda4119edc8be5f56c28af9037b413a8d786dd33c0e79542f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737466"
---
# <a name="esentbackupdirectorynotemptyexception-class"></a>Classe EsentBackupDirectoryNotEmptyException

Classe base para JET_err. Exceções BackupDirectoryNotEmpty.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupDirectoryNotEmptyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentBackupDirectoryNotEmptyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupDirectoryNotEmptyException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentBackupDirectoryNotEmptyException](./esentbackupdirectorynotemptyexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
