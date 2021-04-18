---
description: 'Saiba mais sobre: Construtor EsentMemoryException (cadeia de caracteres, JET_err)'
title: Construtor EsentMemoryException (cadeia de caracteres, JET_err)
TOCTitle: EsentMemoryException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60cdb6fda03695a4afb41d82e83aaeeb9415f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783679"
---
# <a name="esentmemoryexception-constructor-string-jet_err"></a>Construtor EsentMemoryException (cadeia de caracteres, JET_err)

Inicializa uma nova instância da classe EsentMemoryException.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentMemoryException(description, _
    err)
```

``` csharp
protected EsentMemoryException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Parâmetros

  - descrição  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    A descrição do erro.

<!-- end list -->

  - erra  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  
    
    O código de erro da exceção.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe EsentMemoryException](./esentmemoryexception-class.md)

[Membros do EsentMemoryException](./esentmemoryexception-members.md)

[Sobrecarga de EsentMemoryException](./esentmemoryexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
