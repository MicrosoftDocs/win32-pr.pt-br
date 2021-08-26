---
description: 'Saiba mais sobre: Método Windows8Api.JetCommitTransaction2'
title: Método Windows8Api.JetCommitTransaction2 (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'JetCommitTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcommittransaction2(v=EXCHG.10)
ms:contentKeyID: 55104454
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7daf80ffae87469c5bd6ad49ddd3092efdad4f8c95f5c2f27239a38328cbdd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967026"
---
# <a name="windows8apijetcommittransaction2-method"></a>Método Windows8Api.JetCommitTransaction2

Confirma as alterações feitas no estado do banco de dados durante o ponto de salvar atual e as migra para o ponto de salvar anterior. Se o ponto de economia mais externo for confirmado, as alterações feitas durante esse ponto de salvar serão comprometidas no estado do banco de dados e a sessão sairá da transação.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetCommitTransaction2 ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_IDWindows8Api.JetCommitTransaction2(sesid, _
    grbit, durableCommit, commitId)
```

``` csharp
public static void JetCommitTransaction2(
    JET_SESID sesid,
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão para a que a transação será confirmada.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)  
    
    Opções de commit.

<!-- end list -->

  - durableCommit  
    Tipo: [System.TimeSpan](/dotnet/api/system.timespan)  
    
    Duração para fazer commit da transação lento.

<!-- end list -->

  - commitId  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    ID de commit associada a esse registro de commit.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Windows8Api](./windows8api-class.md)

[Membros do Windows8Api](./windows8api-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
