---
description: 'Saiba mais sobre: Construtor EsentFragmentationException (cadeia de caracteres, JET_err)'
title: Construtor EsentFragmentationException (cadeia de caracteres, JET_err)
TOCTitle: EsentFragmentationException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101778
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3c6492ac4055b985194b3849090672d471390cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090738"
---
# <a name="esentfragmentationexception-constructor-string-jet_err"></a>Construtor EsentFragmentationException (cadeia de caracteres, JET_err)

Inicializa uma nova instância da classe EsentFragmentationException.

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

Dim instance As New EsentFragmentationException(description, _
    err)
```

``` csharp
protected EsentFragmentationException(
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

[Classe EsentFragmentationException](./esentfragmentationexception-class.md)

[Membros do EsentFragmentationException](./esentfragmentationexception-members.md)

[Sobrecarga de EsentFragmentationException](./esentfragmentationexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
