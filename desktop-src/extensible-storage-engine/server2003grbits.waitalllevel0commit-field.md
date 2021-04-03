---
description: 'Saiba mais sobre: campo Server2003Grbits. WaitAllLevel0Commit'
title: Campo Server2003Grbits. WaitAllLevel0Commit (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: WaitAllLevel0Commit field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.waitalllevel0commit(v=EXCHG.10)
ms:contentKeyID: 55104104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16390069adf81ead8e819bc5148a88e30900b508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828635"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a><span data-ttu-id="900ef-103">Campo Server2003Grbits. WaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="900ef-103">Server2003Grbits.WaitAllLevel0Commit field</span></span>

<span data-ttu-id="900ef-104">Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberadas para o arquivo de log de transações serão liberadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="900ef-104">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="900ef-105">Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="900ef-105">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="900ef-106">Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</span><span class="sxs-lookup"><span data-stu-id="900ef-106">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="900ef-107">Essa opção não pode ser usada em combinação com nenhuma outra opção.</span><span class="sxs-lookup"><span data-stu-id="900ef-107">This option cannot be used in combination with any other option.</span></span>

<span data-ttu-id="900ef-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="900ef-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="900ef-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="900ef-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="900ef-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="900ef-110">Syntax</span></span>

``` vb
'Declaration
Public Const WaitAllLevel0Commit As CommitTransactionGrbit
'Usage
Dim value As CommitTransactionGrbit

value = Server2003Grbits.WaitAllLevel0Commit
```

``` csharp
public const CommitTransactionGrbit WaitAllLevel0Commit
```

## <a name="see-also"></a><span data-ttu-id="900ef-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="900ef-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="900ef-112">Referência</span><span class="sxs-lookup"><span data-stu-id="900ef-112">Reference</span></span>

[<span data-ttu-id="900ef-113">Classe Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="900ef-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="900ef-114">Membros do Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="900ef-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="900ef-115">Namespace Microsoft. ISAM. ESENT. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="900ef-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
