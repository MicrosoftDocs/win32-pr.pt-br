---
description: 'Saiba mais sobre: Construtor de instância (cadeia de caracteres, Cadeia de caracteres)'
title: Construtor de instância (cadeia de caracteres, Cadeia de caracteres)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296495"
---
# <a name="instance-constructor-string-string"></a>Construtor de instância (cadeia de caracteres, Cadeia de caracteres)

Inicializa uma nova instância da classe de instância. O JET_INSTANCE subjacente é alocado, mas não inicializado.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a>Parâmetros

  - name  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O nome da instância. Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.

<!-- end list -->

  - displayName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Um nome de exibição para a instância. Isso será usado em entradas do EventLog.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de instância](./instance-class.md)

[Membros da Instância ](./instance-members.md)

[Sobrecarga de instância](./instance-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
