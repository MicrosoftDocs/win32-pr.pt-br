---
description: 'Saiba mais sobre: propriedade BoolColumnValue.Size'
title: Propriedade BoolColumnValue.Size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.boolcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55100904
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c06c1645ddca2461122477ff07a963bb9e0727967983c5e76ee82ef060a3200c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275276"
---
# <a name="boolcolumnvaluesize-property"></a>Propriedade BoolColumnValue.Size

Obtém o tamanho do valor na coluna. Isso retorna 0 para colunas de tamanho variável (ou seja, binário e cadeia de caracteres).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe BoolColumnValue](./boolcolumnvalue-class.md)

[Membros BoolColumnValue](./boolcolumnvalue-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
