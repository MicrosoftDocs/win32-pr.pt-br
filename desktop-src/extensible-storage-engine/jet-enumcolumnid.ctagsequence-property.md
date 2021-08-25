---
description: 'Saiba mais sobre: JET_ENUMCOLUMNID.ctagSequence'
title: JET_ENUMCOLUMNID.ctagSequence
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e60ae86a27f1c82a237ae9c02e54298cbe6aa7de251e9c1c38d7bc08dad42cc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890895"
---
# <a name="jet_enumcolumnidctagsequence-property"></a>JET_ENUMCOLUMNID.ctagSequence

Obtém ou define a contagem de valores de coluna (por índice baseado em um) para enumerar para a ID de coluna especificada. Se ctagSequence for 0 (zero), rgtagSequence será ignorado e todos os valores de coluna para a ID de coluna especificada serão enumerados.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_ENUMCOLUMNID classe](./jet-enumcolumnid-class.md)

[JET_ENUMCOLUMNID membros](./jet-enumcolumnid-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
