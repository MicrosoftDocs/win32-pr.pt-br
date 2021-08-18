---
description: 'Saiba mais sobre: método Windows8Api. JetSetSessionParameter'
title: Método Windows8Api. JetSetSessionParameter (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetSetSessionParameter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetsessionparameter(v=EXCHG.10)
ms:contentKeyID: 55104461
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b995fe5b749640ced2164cdbed72a421510f3bf23cb02e30acb18b47b262efa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117889375"
---
# <a name="windows8apijetsetsessionparameter-method"></a>Método Windows8Api. JetSetSessionParameter

Define um parâmetro no estado de sessão fornecido, usado para o tempo de vida desta sessão ou até a redefinição.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetSetSessionParameter ( _
    sesid As JET_SESID, _
    sesparamid As JET_sesparam, _
    data As Byte(), _
    dataSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim sesparamid As JET_sesparam
Dim data As Byte()
Dim dataSize As IntegerWindows8Api.JetSetSessionParameter(sesid, _
    sesparamid, data, dataSize)
```

``` csharp
public static void JetSetSessionParameter(
    JET_SESID sesid,
    JET_sesparam sesparamid,
    byte[] data,
    int dataSize
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão na qual definir o parâmetro.

<!-- end list -->

  - sesparamid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)  
    
    A ID do parâmetro de sessão a ser definido.

<!-- end list -->

  - data  
    Escreva \[\]  
    
    Dados a serem definidos neste parâmetro de sessão.

<!-- end list -->

  - dataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Tamanho dos dados fornecidos.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Windows8Api](./windows8api-class.md)

[Membros do Windows8Api](./windows8api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
