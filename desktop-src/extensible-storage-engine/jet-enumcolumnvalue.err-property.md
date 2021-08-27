---
description: 'Saiba mais sobre a propriedade: JET_ENUMCOLUMNVALUE. err'
title: Propriedade JET_ENUMCOLUMNVALUE. err
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue.err(v=EXCHG.10)
ms:contentKeyID: 55103626
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.get_err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.set_err
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e87abbb77cb472048725f9ee0d797a565625cb0872aed6066ff9e5bfb7aaaf0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116126"
---
# <a name="jet_enumcolumnvalueerr-property"></a>Propriedade JET_ENUMCOLUMNVALUE. err

Obtém o código de status da coluna resultante da enumeração do valor da coluna.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md)

[Membros do JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[ColumnNull](./jet-wrn-enumeration.md)

[ColumnSkipped](./jet-wrn-enumeration.md)

[ColumnTruncated](./jet-wrn-enumeration.md)
