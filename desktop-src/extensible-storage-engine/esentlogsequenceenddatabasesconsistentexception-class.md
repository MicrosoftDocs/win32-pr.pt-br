---
description: 'Saiba mais sobre: Classe EsentLogSequenceEndDatabasesConsistentException'
title: Classe EsentLogSequenceEndDatabasesConsistentException
TOCTitle: EsentLogSequenceEndDatabasesConsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogsequenceenddatabasesconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55102212
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a818654c1acfa17c8e9af61987880e7d79dceaaffe305ba98df2d1d57cc39c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019326"
---
# <a name="esentlogsequenceenddatabasesconsistentexception-class"></a>Classe EsentLogSequenceEndDatabasesConsistentException

Classe base para JET_err. Exceções LogSequenceEndDatabasesConsistent.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentFragmentationException](./esentfragmentationexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogSequenceEndDatabasesConsistentException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentLogSequenceEndDatabasesConsistentException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogSequenceEndDatabasesConsistentException : EsentFragmentationException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentLogSequenceEndDatabasesConsistentException](./esentlogsequenceenddatabasesconsistentexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
