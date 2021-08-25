---
description: 'Saiba mais sobre: classe EsentFragmentationException'
title: Classe EsentFragmentationException
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2db8934cfdbfb58b44d3de14c13c72bc7d5ce5afa4f5b2bdfaec0a05926469af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838716"
---
# <a name="esentfragmentationexception-class"></a>Classe EsentFragmentationException

Classe base para exceções de fragmentação.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentFragmentationException  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentFragmentationException](./esentfragmentationexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. EsentFragmentationException  
            [Microsoft. ISAM. ESENT. Interop. EsentLogSectorSizeMismatchException](./esentlogsectorsizemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogSequenceEndDatabasesConsistentException](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogSequenceEndException](./esentlogsequenceendexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOutOfAutoincrementValuesException](./esentoutofautoincrementvaluesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOutOfDbtimeValuesException](./esentoutofdbtimevaluesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOutOfLongValueIDsException](./esentoutoflongvalueidsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOutOfObjectIDsException](./esentoutofobjectidsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentOutOfSequentialIndexValuesException](./esentoutofsequentialindexvaluesexception-class.md)