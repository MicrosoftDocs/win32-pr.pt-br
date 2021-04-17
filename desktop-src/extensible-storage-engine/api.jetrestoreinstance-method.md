---
description: 'Saiba mais sobre: método API. JetRestoreInstance'
title: Método API. JetRestoreInstance
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789614"
---
# <a name="apijetrestoreinstance-method"></a>Método API. JetRestoreInstance

Restaura e recupera um backup de streaming de uma instância do, incluindo todos os bancos de dados anexados. Ele foi projetado para funcionar com um backup criado com a função [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) . Essa é a função de restauração mais simples e encapsulada.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância a ser usada. A instância não deve ser inicializada. A restauração dos arquivos irá inicializar a instância.

<!-- end list -->

  - source  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Local do backup. O backup deve ter sido criado com [JetBackupInstance (JET_INSTANCE, String, BackupGrbit JET_PFNSTATUS)](./api.jetbackupinstance-method.md).

<!-- end list -->

  - destino  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nome da pasta em que os arquivos de banco de dados do conjunto de backup serão copiados e recuperados. Se isso for definido como NULL, os arquivos de banco de dados serão copiados e recuperados em seu local original.

<!-- end list -->

  - statusCallback  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Retorno de chamada de notificação de status opcional.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
