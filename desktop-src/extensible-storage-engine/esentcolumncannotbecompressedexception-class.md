---
description: 'Saiba mais sobre: Classe EsentColumnCannotBeCompressedException'
title: Classe EsentColumnCannotBeCompressedException
TOCTitle: EsentColumnCannotBeCompressedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumncannotbecompressedexception(v=EXCHG.10)
ms:contentKeyID: 55101403
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ee18ecc9df34524dceba5dce4ef542048ab92e4fb4437c4b433871be284a248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736976"
---
# <a name="esentcolumncannotbecompressedexception-class"></a>Classe EsentColumnCannotBeCompressedException

Classe base para JET_err. Exceções ColumnCannotBeCompressed.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnCannotBeCompressedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnCannotBeCompressedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnCannotBeCompressedException : EsentUsageException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros EsentColumnCannotBeCompressedException](./esentcolumncannotbecompressedexception-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
