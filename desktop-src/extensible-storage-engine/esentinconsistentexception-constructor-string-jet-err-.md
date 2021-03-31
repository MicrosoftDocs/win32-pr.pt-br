---
description: 'Saiba mais sobre: Construtor EsentInconsistentException (cadeia de caracteres, JET_err)'
title: Construtor EsentInconsistentException (cadeia de caracteres, JET_err)
TOCTitle: EsentInconsistentException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInconsistentException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101740
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96d8b7a055d07ae120a23665004712772f67f215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647435"
---
# <a name="esentinconsistentexception-constructor-string-jet_err"></a>Construtor EsentInconsistentException (cadeia de caracteres, JET_err)

Inicializa uma nova instância da classe EsentInconsistentException.

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

Dim instance As New EsentInconsistentException(description, _
    err)
```

``` csharp
protected EsentInconsistentException(
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

[Classe EsentInconsistentException](./esentinconsistentexception-class.md)

[Membros do EsentInconsistentException](./esentinconsistentexception-members.md)

[Sobrecarga de EsentInconsistentException](./esentinconsistentexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
