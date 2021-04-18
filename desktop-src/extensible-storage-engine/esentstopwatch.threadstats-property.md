---
description: 'Saiba mais sobre: Propriedade EsentStopwatch. ThreadStats'
title: Propriedade EsentStopwatch. ThreadStats
TOCTitle: 'ThreadStats property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch.threadstats(v=EXCHG.10)
ms:contentKeyID: 55102996
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.get_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.set_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 241b7d80e86eb3c773aecd58b7d16e749e040611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788608"
---
# <a name="esentstopwatchthreadstats-property"></a><span data-ttu-id="60cdb-103">Propriedade EsentStopwatch. ThreadStats</span><span class="sxs-lookup"><span data-stu-id="60cdb-103">EsentStopwatch.ThreadStats property</span></span>

<span data-ttu-id="60cdb-104">Obtém o total de estatísticas de trabalho de ESENT medido pela instância atual.</span><span class="sxs-lookup"><span data-stu-id="60cdb-104">Gets the total ESENT work stats measured by the current instance.</span></span>

<span data-ttu-id="60cdb-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="60cdb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="60cdb-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="60cdb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="60cdb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="60cdb-107">Syntax</span></span>

``` vb
'Declaration
Public Property ThreadStats As JET_THREADSTATS
    Get
    Private Set
'Usage
Dim instance As EsentStopwatch
Dim value As JET_THREADSTATS

value = instance.ThreadStats
```

``` csharp
public JET_THREADSTATS ThreadStats { get; private set; }
```

#### <a name="property-value"></a><span data-ttu-id="60cdb-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="60cdb-108">Property value</span></span>

<span data-ttu-id="60cdb-109">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="60cdb-109">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="60cdb-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="60cdb-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="60cdb-111">Referência</span><span class="sxs-lookup"><span data-stu-id="60cdb-111">Reference</span></span>

[<span data-ttu-id="60cdb-112">Classe EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="60cdb-112">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="60cdb-113">Membros do EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="60cdb-113">EsentStopwatch members</span></span>](./esentstopwatch-members.md)

[<span data-ttu-id="60cdb-114">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="60cdb-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
