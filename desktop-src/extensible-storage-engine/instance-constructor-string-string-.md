---
description: 'Saiba mais sobre: Construtor de instância (cadeia de caracteres, cadeia de caracteres)'
title: Construtor de instância (cadeia de caracteres, cadeia de caracteres)
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
ms.openlocfilehash: 2d93a5799a646a90688261bdd55bc9dfe929ef6bd074a51e15cabdcee768ffa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116436"
---
# <a name="instance-constructor-string-string"></a>Construtor de instância (cadeia de caracteres, cadeia de caracteres)

Inicializa uma nova instância da classe Instance. O valor JET_INSTANCE subjacente é alocado, mas não inicializado.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [System.String](/dotnet/api/system.string)  
    
    O nome da instância. Essa cadeia de caracteres deve ser exclusiva dentro de um determinado processo que hospeda o mecanismo de banco de dados.

<!-- end list -->

  - displayName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Um nome de exibição para a instância. Isso será usado em entradas de eventlog.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de instância](./instance-class.md)

[Membros da Instância ](./instance-members.md)

[Sobrecarga de instância](./instance-constructor.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
