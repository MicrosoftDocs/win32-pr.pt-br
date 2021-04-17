---
description: 'Saiba mais sobre: estrutura de JET_COLUMNID'
title: Estrutura de JET_COLUMNID
TOCTitle: JET_COLUMNID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_COLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid(v=EXCHG.10)
ms:contentKeyID: 39510915
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 163c10250e9d1f109b9557f8d222790c71561f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787558"
---
# <a name="jet_columnid-structure"></a>Estrutura de JET_COLUMNID

Uma JET_COLUMNID identifica uma coluna dentro de uma tabela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Structure JET_COLUMNID _
    Implements IEquatable(Of JET_COLUMNID), IComparable(Of JET_COLUMNID),  _
    IFormattable
'Usage
Dim instance As JET_COLUMNID
```

``` csharp
public struct JET_COLUMNID : IEquatable<JET_COLUMNID>, 
    IComparable<JET_COLUMNID>, IFormattable
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do JET_COLUMNID](./jet-columnid-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
