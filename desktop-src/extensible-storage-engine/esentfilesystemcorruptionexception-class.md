---
description: 'Saiba mais sobre: classe EsentFileSystemCorruptionException'
title: Classe EsentFileSystemCorruptionException
TOCTitle: EsentFileSystemCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilesystemcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101716
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 863766b5b4b768546ade161abf8c30659db1d720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662899"
---
# <a name="esentfilesystemcorruptionexception-class"></a>Classe EsentFileSystemCorruptionException

Classe base para JET_err. FileSystemCorruption exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentFileSystemCorruptionException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileSystemCorruptionException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentFileSystemCorruptionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileSystemCorruptionException : EsentCorruptionException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentFileSystemCorruptionException](./esentfilesystemcorruptionexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
