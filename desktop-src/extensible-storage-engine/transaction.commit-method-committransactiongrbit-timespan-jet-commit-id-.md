---
description: 'Saiba mais sobre: método Transaction. Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)'
title: Método Transaction. Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
TOCTitle: Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104166
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18df363e4320a4b1a53c34e15fcf68939fce96ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011487"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a>Método Transaction. Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)

Confirme uma transação. Esse objeto deve estar em uma transação.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_ID

instance.Commit(grbit, durableCommit, _
    commitId)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a>Parâmetros

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)  
    
    Opções de JetCommitTransaction.

<!-- end list -->

  - durableCommit  
    Tipo: [System. TimeSpan](/dotnet/api/system.timespan)  
    
    Duração da confirmação de transações lentas.

<!-- end list -->

  - commitId  
    Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Confirme a ID deste registro de confirmação.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de transação](./transaction-class.md)

[Membros da transação](./transaction-members.md)

[Sobrecarga de confirmação](./transaction.commit-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
