---
description: 'Saiba mais sobre: Classe EsentSectorSizeNotSupportedException'
title: Classe EsentSectorSizeNotSupportedException
TOCTitle: EsentSectorSizeNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsectorsizenotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d281083093c52c0aa6119f7790d002e3a4fceb4a008a58f123bf1752319feef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781731"
---
# <a name="esentsectorsizenotsupportedexception-class"></a>Classe EsentSectorSizeNotSupportedException

Classe base para JET_err. Exceções SectorSizeNotSupported.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentFatalException](./esentfatalexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSectorSizeNotSupportedException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentSectorSizeNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSectorSizeNotSupportedException : EsentFatalException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentSectorSizeNotSupportedException](./esentsectorsizenotsupportedexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
