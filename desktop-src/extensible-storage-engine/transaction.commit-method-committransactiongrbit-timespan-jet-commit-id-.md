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
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a><span data-ttu-id="5e415-103">Método Transaction. Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</span><span class="sxs-lookup"><span data-stu-id="5e415-103">Transaction.Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</span></span>

<span data-ttu-id="5e415-104">Confirme uma transação.</span><span class="sxs-lookup"><span data-stu-id="5e415-104">Commit a transaction.</span></span> <span data-ttu-id="5e415-105">Esse objeto deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="5e415-105">This object should be in a transaction.</span></span>

<span data-ttu-id="5e415-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5e415-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5e415-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5e415-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5e415-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e415-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="5e415-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e415-109">Parameters</span></span>

  - <span data-ttu-id="5e415-110">grbit</span><span class="sxs-lookup"><span data-stu-id="5e415-110">grbit</span></span>  
    <span data-ttu-id="5e415-111">Tipo: [Microsoft. ISAM. ESENT. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5e415-111">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5e415-112">Opções de JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="5e415-112">JetCommitTransaction options.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e415-113">durableCommit</span><span class="sxs-lookup"><span data-stu-id="5e415-113">durableCommit</span></span>  
    <span data-ttu-id="5e415-114">Tipo: [System. TimeSpan](/dotnet/api/system.timespan)</span><span class="sxs-lookup"><span data-stu-id="5e415-114">Type: [System.TimeSpan](/dotnet/api/system.timespan)</span></span>  
    
    <span data-ttu-id="5e415-115">Duração da confirmação de transações lentas.</span><span class="sxs-lookup"><span data-stu-id="5e415-115">Duration for committing lazy transactions.</span></span>

<!-- end list -->

  - <span data-ttu-id="5e415-116">commitId</span><span class="sxs-lookup"><span data-stu-id="5e415-116">commitId</span></span>  
    <span data-ttu-id="5e415-117">Tipo: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="5e415-117">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="5e415-118">Confirme a ID deste registro de confirmação.</span><span class="sxs-lookup"><span data-stu-id="5e415-118">Commit-id for this commit record.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e415-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e415-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5e415-120">Referência</span><span class="sxs-lookup"><span data-stu-id="5e415-120">Reference</span></span>

[<span data-ttu-id="5e415-121">Classe de transação</span><span class="sxs-lookup"><span data-stu-id="5e415-121">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="5e415-122">Membros da transação</span><span class="sxs-lookup"><span data-stu-id="5e415-122">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="5e415-123">Sobrecarga de confirmação</span><span class="sxs-lookup"><span data-stu-id="5e415-123">Commit overload</span></span>](./transaction.commit-method.md)

[<span data-ttu-id="5e415-124">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5e415-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
