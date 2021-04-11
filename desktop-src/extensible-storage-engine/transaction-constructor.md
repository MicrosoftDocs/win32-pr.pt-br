---
description: 'Saiba mais sobre: Construtor de transação'
title: Construtor de transação
TOCTitle: 'Transaction constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.transaction(v=EXCHG.10)
ms:contentKeyID: 55104069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.Transaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a8c3214ebe3d88ce8b50aff000d64270ec50a6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170720"
---
# <a name="transaction-constructor"></a><span data-ttu-id="98be9-103">Construtor de transação</span><span class="sxs-lookup"><span data-stu-id="98be9-103">Transaction constructor</span></span>

<span data-ttu-id="98be9-104">Inicializa uma nova instância da classe Transaction.</span><span class="sxs-lookup"><span data-stu-id="98be9-104">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="98be9-105">Isso inicia automaticamente uma transação.</span><span class="sxs-lookup"><span data-stu-id="98be9-105">This automatically begins a transaction.</span></span> <span data-ttu-id="98be9-106">A transação será revertida se não confirmada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="98be9-106">The transaction will be rolled back if not explicitly committed.</span></span>

<span data-ttu-id="98be9-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="98be9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="98be9-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="98be9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="98be9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98be9-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID

Dim instance As New Transaction(sesid)
```

``` csharp
public Transaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="98be9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98be9-110">Parameters</span></span>

  - <span data-ttu-id="98be9-111">sesid</span><span class="sxs-lookup"><span data-stu-id="98be9-111">sesid</span></span>  
    <span data-ttu-id="98be9-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="98be9-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="98be9-113">A sessão para a qual iniciar a transação.</span><span class="sxs-lookup"><span data-stu-id="98be9-113">The session to start the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="98be9-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="98be9-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="98be9-115">Referência</span><span class="sxs-lookup"><span data-stu-id="98be9-115">Reference</span></span>

[<span data-ttu-id="98be9-116">Classe de transação</span><span class="sxs-lookup"><span data-stu-id="98be9-116">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="98be9-117">Membros da transação</span><span class="sxs-lookup"><span data-stu-id="98be9-117">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="98be9-118">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="98be9-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
