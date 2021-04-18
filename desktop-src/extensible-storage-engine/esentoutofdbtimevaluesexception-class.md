---
description: 'Saiba mais sobre: classe EsentOutOfDbtimeValuesException'
title: Classe EsentOutOfDbtimeValuesException
TOCTitle: EsentOutOfDbtimeValuesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofdbtimevaluesexception(v=EXCHG.10)
ms:contentKeyID: 55102463
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 154403b4a87533859415d220c9a0d1c0370faf2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793666"
---
# <a name="esentoutofdbtimevaluesexception-class"></a>Classe EsentOutOfDbtimeValuesException

Classe base para JET_err. OutOfDbtimeValues exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentFragmentationException](./esentfragmentationexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentOutOfDbtimeValuesException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfDbtimeValuesException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfDbtimeValuesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfDbtimeValuesException : EsentFragmentationException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentOutOfDbtimeValuesException](./esentoutofdbtimevaluesexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
