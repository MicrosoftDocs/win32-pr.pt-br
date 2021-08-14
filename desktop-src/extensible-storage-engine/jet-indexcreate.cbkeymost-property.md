---
description: 'Saiba mais sobre: JET_INDEXCREATE.cbKeyMost'
title: JET_INDEXCREATE.cbKeyMost
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17908b19cba3ed047b98f4532982001019516d9b32e2799c29a6671cbd862fe7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232676"
---
# <a name="jet_indexcreatecbkeymost-property"></a>JET_INDEXCREATE.cbKeyMost

Obtém ou define o tamanho máximo permitida, em bytes, para chaves no índice. O tamanho máximo mínimo de chave com suporte é JET_cbKeyMostMin (255), que é o tamanho máximo da chave herdado. O tamanho máximo da chave depende do tamanho da página do banco de [dados DatabasePageSize](./jet-param-enumeration.md). O tamanho máximo da chave pode ser recuperado com [KeyMost.](./systemparameters.keymost-property.md) Esse parâmetro é ignorado no Windows XP e Windows Server 2003. Ao contrário da API não gerenciamento, **IndexKeyMost()** (JET_bitIndexKeyMost) não é necessário, ela será adicionada automaticamente.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_INDEXCREATE classe](./jet-indexcreate-class.md)

[JET_INDEXCREATE membros](./jet-indexcreate-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
