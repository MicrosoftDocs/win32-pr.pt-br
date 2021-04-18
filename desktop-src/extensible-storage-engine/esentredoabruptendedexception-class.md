---
description: 'Saiba mais sobre: classe EsentRedoAbruptEndedException'
title: Classe EsentRedoAbruptEndedException
TOCTitle: EsentRedoAbruptEndedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentredoabruptendedexception(v=EXCHG.10)
ms:contentKeyID: 55102536
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 436a03d5775c4d4bec405566c98280a3250e9196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813753"
---
# <a name="esentredoabruptendedexception-class"></a>Classe EsentRedoAbruptEndedException

Classe base para JET_err. RedoAbruptEnded exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentRedoAbruptEndedException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRedoAbruptEndedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRedoAbruptEndedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRedoAbruptEndedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentRedoAbruptEndedException](./esentredoabruptendedexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
