---
description: 'Saiba mais sobre: IJET_LOGTIME. Método ToDateTime'
title: IJET_LOGTIME. Método ToDateTime
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.ijet_logtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39510507
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78226731ef945025aef0609cfeb905fe9b42101d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813722"
---
# <a name="ijet_logtimetodatetime-method"></a>IJET_LOGTIME. Método ToDateTime

Gere uma representação DateTime desta IJET_LOGTIME.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As IJET_LOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Um DateTime que representa o IJET_LOGTIME. Se o IJET_LOGTIME for NULL, NULL será retornado.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Interface IJET_LOGTIME](./ijet-logtime-interface.md)

[Membros do IJET_LOGTIME](./ijet-logtime-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
