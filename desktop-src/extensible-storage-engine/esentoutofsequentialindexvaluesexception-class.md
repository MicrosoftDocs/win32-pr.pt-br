---
description: 'Saiba mais sobre: Classe EsentOutOfSequentialIndexValuesException'
title: Classe EsentOutOfSequentialIndexValuesException
TOCTitle: EsentOutOfSequentialIndexValuesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofsequentialindexvaluesexception(v=EXCHG.10)
ms:contentKeyID: 55107300
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 15cae09912da03bef76464ceffef11312788ce16ec81244c168fb09cbcc09ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733096"
---
# <a name="esentoutofsequentialindexvaluesexception-class"></a>Classe EsentOutOfSequentialIndexValuesException

Classe base para JET_err. Exceções OutOfSequentialIndexValues.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentFragmentationException](./esentfragmentationexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfSequentialIndexValuesException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfSequentialIndexValuesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfSequentialIndexValuesException : EsentFragmentationException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentOutOfSequentialIndexValuesException](./esentoutofsequentialindexvaluesexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
