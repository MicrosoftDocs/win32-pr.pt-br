---
description: 'Saiba mais sobre: classe EsentMissingCurrentLogFilesException'
title: Classe EsentMissingCurrentLogFilesException
TOCTitle: EsentMissingCurrentLogFilesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingcurrentlogfilesexception(v=EXCHG.10)
ms:contentKeyID: 55102260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c00bec8ba2dee02bf0240bda78f29b3b8f4eafa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770054"
---
# <a name="esentmissingcurrentlogfilesexception-class"></a>Classe EsentMissingCurrentLogFilesException

Classe base para JET_err. MissingCurrentLogFiles exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentMissingCurrentLogFilesException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingCurrentLogFilesException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingCurrentLogFilesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingCurrentLogFilesException : EsentInconsistentException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentMissingCurrentLogFilesException](./esentmissingcurrentlogfilesexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
