---
description: 'Saiba mais sobre: Construtor EsentException (cadeia de caracteres)'
title: Construtor EsentException (cadeia de caracteres) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796220"
---
# <a name="esentexception-constructor-string"></a>Construtor EsentException (cadeia de caracteres)

Inicializa uma nova instância da classe EsentException com uma mensagem de erro especificada.

**Namespace:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a>Parâmetros

  - message  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    A mensagem que descreve o erro.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe EsentException](./esentexception-class.md)

[Membros do EsentException](./esentexception-members.md)

[Sobrecarga de EsentException](./esentexception-constructor.md)

[Namespace Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)
