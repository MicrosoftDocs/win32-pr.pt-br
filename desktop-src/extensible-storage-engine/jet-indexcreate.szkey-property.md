---
description: 'Saiba mais sobre a propriedade: JET_INDEXCREATE. szKey'
title: Propriedade JET_INDEXCREATE. szKey
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86ade65ee28eef6314d31653772b0c22657476d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297409"
---
# <a name="jet_indexcreateszkey-property"></a>Propriedade JET_INDEXCREATE. szKey

Obtém ou define a descrição da chave de índice. Essa é uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo. Cada token tem o formato de \[ nome de coluna-especificador de direção \] \[ \] , em que a especificação de direção é "+" ou "-". por exemplo, um szKey de "+ ABC \\ 0-Def \\ 0 + GHI \\ 0" irá indexar as três colunas "ABC" (em ordem crescente), "def" (em ordem decrescente) e "GHI" (em ordem crescente).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Membros do JET_INDEXCREATE](./jet-indexcreate-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
