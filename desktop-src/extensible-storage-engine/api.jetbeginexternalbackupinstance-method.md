---
description: 'Saiba mais sobre: método API. JetBeginExternalBackupInstance'
title: Método API. JetBeginExternalBackupInstance
TOCTitle: 'JetBeginExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100659
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c42f5d1f62de0af7582247fb47d407f82981a42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920794"
---
# <a name="apijetbeginexternalbackupinstance-method"></a>Método API. JetBeginExternalBackupInstance

Inicia um backup externo enquanto o mecanismo e o banco de dados estão online e ativos.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetBeginExternalBackupInstance ( _
    instance As JET_INSTANCE, _
    grbit As BeginExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As BeginExternalBackupGrbitApi.JetBeginExternalBackupInstance(instance, _
    grbit)
```

``` csharp
public static void JetBeginExternalBackupInstance(
    JET_INSTANCE instance,
    BeginExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância se prepara para o backup.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)  
    
    Opções de backup.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
