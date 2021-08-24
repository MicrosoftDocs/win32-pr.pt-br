---
description: 'Saiba mais sobre: JET_INDEXCREATE.szKey'
title: JET_INDEXCREATE.szKey
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
ms.openlocfilehash: 905bc6e72704121617a2fcc2b9b368bee9014f897ce157f473e3f9ced5a92c72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720566"
---
# <a name="jet_indexcreateszkey-property"></a>JET_INDEXCREATE.szKey

Obtém ou define a descrição da chave de índice. Essa é uma cadeia de caracteres terminada em nulo dupla de tokens delimitados por nulo. Cada token é do formato \[ nome-da-coluna do especificador de direção, em \] \[ \] que direction-specification é "+" ou "-". por exemplo, uma szKey de "+abc \\ 0-def 0+gee 0" será indexada sobre as três \\ \\ colunas "abc" (em ordem crescente), "def" (em ordem decrescente) e "gee" (em ordem crescente).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_INDEXCREATE classe](./jet-indexcreate-class.md)

[JET_INDEXCREATE membros](./jet-indexcreate-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
