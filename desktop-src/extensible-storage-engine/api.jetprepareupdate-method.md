---
description: 'Saiba mais sobre: método API. JetPrepareUpdate'
title: Método API. JetPrepareUpdate
TOCTitle: 'JetPrepareUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetprepareupdate(v=EXCHG.10)
ms:contentKeyID: 55100782
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8094fef5fcf008dd5f6eb6f2bfd05a0be1bf077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171765"
---
# <a name="apijetprepareupdate-method"></a>Método API. JetPrepareUpdate

Prepare um cursor para atualização.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetPrepareUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prepApi.JetPrepareUpdate(sesid, tableid, _
    prep)
```

``` csharp
public static void JetPrepareUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão que está iniciando a atualização.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor para o qual iniciar a atualização.

<!-- end list -->

  - Prep  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_prep](./jet-prep-enumeration.md)  
    
    O tipo de atualização a ser preparada.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
