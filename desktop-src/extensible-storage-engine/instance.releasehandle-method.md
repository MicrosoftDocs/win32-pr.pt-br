---
description: 'Saiba mais sobre: método instance. ReleaseHandle'
title: Método instance. ReleaseHandle
TOCTitle: 'ReleaseHandle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.releasehandle(v=EXCHG.10)
ms:contentKeyID: 55103298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fcac0fcbffc685fb91bd0c0bf2f97865540cb1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011436"
---
# <a name="instancereleasehandle-method"></a>Método instance. ReleaseHandle

Libere o identificador para esta instância.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected Overrides Function ReleaseHandle As Boolean
'Usage
Dim returnValue As Boolean

returnValue = Me.ReleaseHandle()
```

``` csharp
protected override bool ReleaseHandle()
```

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se o identificador puder ser liberado.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de instância](./instance-class.md)

[Membros da Instância ](./instance-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
