---
description: 'Saiba mais sobre: JET_THREADSTATS. Método Subtract'
title: JET_THREADSTATS. Método Subtract (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.subtract(v=EXCHG.10)
ms:contentKeyID: 39514465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf1f47258fe965c41b0a02ccbb32712b0a54c97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763820"
---
# <a name="jet_threadstatssubtract-method"></a><span data-ttu-id="c5e51-103">JET_THREADSTATS. Método Subtract</span><span class="sxs-lookup"><span data-stu-id="c5e51-103">JET_THREADSTATS.Subtract method</span></span>

<span data-ttu-id="c5e51-104">Calcule a diferença em estatísticas entre duas estruturas de JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="c5e51-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="c5e51-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5e51-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="c5e51-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c5e51-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e51-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5e51-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Subtract(t1, t2)
```

``` csharp
public static JET_THREADSTATS Subtract(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="c5e51-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5e51-108">Parameters</span></span>

  - <span data-ttu-id="c5e51-109">t1</span><span class="sxs-lookup"><span data-stu-id="c5e51-109">t1</span></span>  
    <span data-ttu-id="c5e51-110">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c5e51-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="c5e51-111">O primeiro JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="c5e51-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5e51-112">T2</span><span class="sxs-lookup"><span data-stu-id="c5e51-112">t2</span></span>  
    <span data-ttu-id="c5e51-113">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c5e51-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="c5e51-114">A segunda JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="c5e51-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c5e51-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5e51-115">Return value</span></span>

<span data-ttu-id="c5e51-116">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c5e51-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="c5e51-117">Uma JET_THREADSTATS que contém a diferença em estatísticas entre T1 e T2.</span><span class="sxs-lookup"><span data-stu-id="c5e51-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5e51-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5e51-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5e51-119">Referência</span><span class="sxs-lookup"><span data-stu-id="c5e51-119">Reference</span></span>

[<span data-ttu-id="c5e51-120">Estrutura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="c5e51-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="c5e51-121">Membros do JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="c5e51-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="c5e51-122">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="c5e51-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
