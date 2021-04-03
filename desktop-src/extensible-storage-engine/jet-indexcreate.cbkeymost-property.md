---
description: 'Saiba mais sobre a propriedade: JET_INDEXCREATE. cbKeyMost'
title: Propriedade JET_INDEXCREATE. cbKeyMost
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
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829253"
---
# <a name="jet_indexcreatecbkeymost-property"></a>Propriedade JET_INDEXCREATE. cbKeyMost

Obtém ou define o tamanho máximo permitido, em bytes, para as chaves no índice. O tamanho mínimo de chave máximo suportado é JET_cbKeyMostMin (255), que é o tamanho de chave máximo herdado. O tamanho máximo da chave depende do tamanho da página do banco de dados [DatabasePageSize](./jet-param-enumeration.md). O tamanho máximo da chave pode ser recuperado com o [máximo](./systemparameters.keymost-property.md). Esse parâmetro é ignorado no Windows XP e no Windows Server 2003. Diferentemente da API não gerenciada, **IndexKeyMost ()** (JET_bitIndexKeyMost) não é necessária, ela será adicionada automaticamente.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

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

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Membros do JET_INDEXCREATE](./jet-indexcreate-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
