---
description: 'Saiba mais sobre: classe EsentIOException'
title: Classe EsentIOException
TOCTitle: EsentIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102033
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82c10cc71e7621aa5fb338acc8964a3e221af3cc068eafb1d32aab6273182501
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115946"
---
# <a name="esentioexception-class"></a>Classe EsentIOException

Classe base para exceções de E/S.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentIOException  
            [Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException](./esentdeletebackupfilefailexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDiskIOException](./esentdiskioexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException](./esentfileaccessdeniedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogWriteFailException](./esentlogwritefailexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException](./esentmakebackupdirectoryfailexception-class.md)  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentIOException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentIOException
```

``` csharp
[SerializableAttribute]
public abstract class EsentIOException : EsentOperationException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentIOException](./esentioexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
