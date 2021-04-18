---
description: 'Saiba mais sobre: JET_PFNSTATUS delegado'
title: JET_PFNSTATUS delegado
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813531"
---
# <a name="jet_pfnstatus-delegate"></a>JET_PFNSTATUS delegado

Recebe informações sobre o progresso de operações de execução longa, como operações de desfragmentação, backup ou restauração. Durante essas operações, o mecanismo de banco de dados chama essa função de retorno de chamada para fornecer uma atualização no andamento da operação.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão com a qual a operação de longa execução foi chamada.

<!-- end list -->

  - padrões  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SNP](./jet-snp-enumeration.md)  
    
    O tipo de operação.

<!-- end list -->

  - snt  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SNT](./jet-snt-enumeration.md)  
    
    O status da operação.

<!-- end list -->

  - data  
    Tipo: [System. Object](/dotnet/api/system.object)  
    
    Dados opcionais. Pode ser um [JET_SNPROG](./jet-snprog-class.md).

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
