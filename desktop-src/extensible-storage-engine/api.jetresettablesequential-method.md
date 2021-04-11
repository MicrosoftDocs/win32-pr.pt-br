---
description: 'Saiba mais sobre: método API. JetResetTableSequential'
title: Método API. JetResetTableSequential
TOCTitle: 'JetResetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b45ca118894015df7cda56201733cdaad9b88d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171762"
---
# <a name="apijetresettablesequential-method"></a>Método API. JetResetTableSequential

Notifica o mecanismo de banco de dados de que o aplicativo não está mais verificando o índice inteiro no qual o cursor está posicionado. Essa chamada reverte uma notificação enviada por [JetSetTableSequential (JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetResetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As ResetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As ResetTableSequentialGrbitApi.JetResetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetResetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ResetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor que estava acessando os dados.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)  
    
    Reservado para uso futuro.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
