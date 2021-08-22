---
description: 'Saiba mais sobre: Classe EsentMakeBackupDirectoryFailException'
title: Classe EsentMakeBackupDirectoryFailException
TOCTitle: EsentMakeBackupDirectoryFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmakebackupdirectoryfailexception(v=EXCHG.10)
ms:contentKeyID: 55102252
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 218edf2d8af8b2a3d712b4142a6e37604736ed7dd3746c7b0e6947b1e415248b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119479436"
---
# <a name="esentmakebackupdirectoryfailexception-class"></a>Classe EsentMakeBackupDirectoryFailException

Classe base para JET_err. Exceções MakeBackupDirectoryFail.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentIOException](./esentioexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMakeBackupDirectoryFailException _
    Inherits EsentIOException
'Usage
Dim instance As EsentMakeBackupDirectoryFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMakeBackupDirectoryFailException : EsentIOException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentMakeBackupDirectoryFailException](./esentmakebackupdirectoryfailexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
