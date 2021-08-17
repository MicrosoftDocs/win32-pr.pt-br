---
description: 'Saiba mais sobre: Construtor EsentApiException (cadeia de caracteres, JET_err)'
title: Construtor EsentApiException (cadeia de caracteres, JET_err)
TOCTitle: EsentApiException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101058
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f13858d07b10ff222e58d851ceafa086eaaeeeedcfd83765c8732869a619c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117716125"
---
# <a name="esentapiexception-constructor-string-jet_err"></a>Construtor EsentApiException (cadeia de caracteres, JET_err)

Inicializa uma nova instância da classe EsentApiException.

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

Dim instance As New EsentApiException(description, _
    err)
```

``` csharp
protected EsentApiException(
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

[Classe EsentApiException](./esentapiexception-class.md)

[Membros do EsentApiException](./esentapiexception-members.md)

[Sobrecarga de EsentApiException](./esentapiexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
