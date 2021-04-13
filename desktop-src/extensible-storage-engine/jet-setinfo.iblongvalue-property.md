---
description: 'Saiba mais sobre a propriedade: JET_SETINFO. ibLongValue'
title: Propriedade JET_SETINFO. ibLongValue
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103918
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324b3cd5c45be8f463ff9b2a9cfe11f1dcad4554
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501492"
---
# <a name="jet_setinfoiblongvalue-property"></a>Propriedade JET_SETINFO. ibLongValue

Obtém ou define o deslocamento para o primeiro byte a ser definido em uma coluna do tipo [LongBinary](./jet-coltyp-enumeration.md) ou [LONGTEXT](./jet-coltyp-enumeration.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_SETINFO](./jet-setinfo-class.md)

[Membros do JET_SETINFO](./jet-setinfo-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
