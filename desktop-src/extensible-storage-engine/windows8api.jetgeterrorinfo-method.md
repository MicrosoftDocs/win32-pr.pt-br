---
description: 'Saiba mais sobre: método Windows8Api. JetGetErrorInfo'
title: Método Windows8Api. JetGetErrorInfo (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetGetErrorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo(Microsoft.Isam.Esent.Interop.JET_err,Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetgeterrorinfo(v=EXCHG.10)
ms:contentKeyID: 55104459
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c94e6594c2d52769f5034bdf1c7253bee838edaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761292"
---
# <a name="windows8apijetgeterrorinfo-method"></a>Método Windows8Api. JetGetErrorInfo

Obtém informações estendidas sobre um erro.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetErrorInfo ( _
    error As JET_err, _
    <OutAttribute> ByRef errinfo As JET_ERRINFOBASIC _
)
'Usage
Dim error As JET_err
Dim errinfo As JET_ERRINFOBASICWindows8Api.JetGetErrorInfo(error, errinfo)
```

``` csharp
public static void JetGetErrorInfo(
    JET_err error,
    out JET_ERRINFOBASIC errinfo
)
```

#### <a name="parameters"></a>Parâmetros

  - erro  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  
    
    O código de erro sobre o qual recuperar informações.

<!-- end list -->

  - errinfo  
    Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)  
    
    Informações sobre o código de erro especificado.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Windows8Api](./windows8api-class.md)

[Membros do Windows8Api](./windows8api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
