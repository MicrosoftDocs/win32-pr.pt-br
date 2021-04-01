---
description: 'Saiba mais sobre: Construtor de instância (cadeia de caracteres, Cadeia de caracteres, TermGrbit)'
title: Construtor de instância (cadeia de caracteres, Cadeia de caracteres, TermGrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647600"
---
# <a name="instance-constructor-string-string-termgrbit"></a>Construtor de instância (cadeia de caracteres, Cadeia de caracteres, TermGrbit)

Inicializa uma nova instância da classe de instância. O JET_INSTANCE subjacente é alocado, mas não inicializado.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
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

<!-- end list -->

  - termGrbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. TermGrbit](./termgrbit-enumeration.md)  
    
    O TermGrbit a ser usado em JetTerm hora.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de instância](./instance-class.md)

[Membros da Instância ](./instance-members.md)

[Sobrecarga de instância](./instance-constructor.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
