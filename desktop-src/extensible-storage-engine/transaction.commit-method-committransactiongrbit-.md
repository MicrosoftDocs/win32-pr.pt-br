---
description: 'Saiba mais sobre: método Transaction. Commit (CommitTransactionGrbit)'
title: Método Transaction. Commit (CommitTransactionGrbit)
TOCTitle: Commit method (CommitTransactionGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104071
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 048071a08d1211d6091fb6c2c23f9cfe302f8872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170714"
---
# <a name="transactioncommit-method-committransactiongrbit"></a><span data-ttu-id="febf6-103">Método Transaction. Commit (CommitTransactionGrbit)</span><span class="sxs-lookup"><span data-stu-id="febf6-103">Transaction.Commit method (CommitTransactionGrbit)</span></span>

<span data-ttu-id="febf6-104">Confirme uma transação.</span><span class="sxs-lookup"><span data-stu-id="febf6-104">Commit a transaction.</span></span> <span data-ttu-id="febf6-105">Esse objeto deve estar em uma transação.</span><span class="sxs-lookup"><span data-stu-id="febf6-105">This object should be in a transaction.</span></span>

<span data-ttu-id="febf6-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="febf6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="febf6-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="febf6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="febf6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="febf6-108">Syntax</span></span>

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit

instance.Commit(grbit)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="febf6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="febf6-109">Parameters</span></span>

  - <span data-ttu-id="febf6-110">grbit</span><span class="sxs-lookup"><span data-stu-id="febf6-110">grbit</span></span>  
    <span data-ttu-id="febf6-111">Tipo: [Microsoft. ISAM. ESENT. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="febf6-111">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="febf6-112">Opções de JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="febf6-112">JetCommitTransaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="febf6-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="febf6-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="febf6-114">Referência</span><span class="sxs-lookup"><span data-stu-id="febf6-114">Reference</span></span>

[<span data-ttu-id="febf6-115">Classe de transação</span><span class="sxs-lookup"><span data-stu-id="febf6-115">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="febf6-116">Membros da transação</span><span class="sxs-lookup"><span data-stu-id="febf6-116">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="febf6-117">Sobrecarga de confirmação</span><span class="sxs-lookup"><span data-stu-id="febf6-117">Commit overload</span></span>](./transaction.commit-method.md)

[<span data-ttu-id="febf6-118">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="febf6-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
