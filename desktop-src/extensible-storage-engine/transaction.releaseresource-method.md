---
description: 'Saiba mais sobre: método Transaction. ReleaseResource'
title: Método Transaction. ReleaseResource
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78d3dc358b6c7c5dfe297132fd83f08c64693c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090650"
---
# <a name="transactionreleaseresource-method"></a><span data-ttu-id="0c58c-103">Método Transaction. ReleaseResource</span><span class="sxs-lookup"><span data-stu-id="0c58c-103">Transaction.ReleaseResource method</span></span>

<span data-ttu-id="0c58c-104">Chamado quando a transação está sendo descartada enquanto ativa.</span><span class="sxs-lookup"><span data-stu-id="0c58c-104">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="0c58c-105">Isso deve reverter a transação.</span><span class="sxs-lookup"><span data-stu-id="0c58c-105">This should rollback the transaction.</span></span>

<span data-ttu-id="0c58c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c58c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c58c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c58c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c58c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c58c-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="see-also"></a><span data-ttu-id="0c58c-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c58c-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c58c-110">Referência</span><span class="sxs-lookup"><span data-stu-id="0c58c-110">Reference</span></span>

[<span data-ttu-id="0c58c-111">Classe de transação</span><span class="sxs-lookup"><span data-stu-id="0c58c-111">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="0c58c-112">Membros da transação</span><span class="sxs-lookup"><span data-stu-id="0c58c-112">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="0c58c-113">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0c58c-113">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
