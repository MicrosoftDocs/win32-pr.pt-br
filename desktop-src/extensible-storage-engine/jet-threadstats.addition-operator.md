---
description: 'Saiba mais sobre: JET_THREADSTATS. Operador de adição'
title: JET_THREADSTATS. Operador de adição (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_addition(v=EXCHG.10)
ms:contentKeyID: 39516195
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 829bf96b3c7095b95644db220a5d18c7e987e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789374"
---
# <a name="jet_threadstatsaddition-operator"></a><span data-ttu-id="6a9f0-103">JET_THREADSTATS. Operador de adição</span><span class="sxs-lookup"><span data-stu-id="6a9f0-103">JET_THREADSTATS.Addition operator</span></span>

<span data-ttu-id="6a9f0-104">Adicione as estatísticas em duas estruturas de JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="6a9f0-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="6a9f0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a9f0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="6a9f0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a9f0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9f0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a9f0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 + t2)
```

``` csharp
public static JET_THREADSTATS operator +(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="6a9f0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a9f0-108">Parameters</span></span>

  - <span data-ttu-id="6a9f0-109">t1</span><span class="sxs-lookup"><span data-stu-id="6a9f0-109">t1</span></span>  
    <span data-ttu-id="6a9f0-110">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6a9f0-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="6a9f0-111">O primeiro JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="6a9f0-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a9f0-112">T2</span><span class="sxs-lookup"><span data-stu-id="6a9f0-112">t2</span></span>  
    <span data-ttu-id="6a9f0-113">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6a9f0-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="6a9f0-114">A segunda JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="6a9f0-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6a9f0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a9f0-115">Return value</span></span>

<span data-ttu-id="6a9f0-116">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="6a9f0-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="6a9f0-117">Uma JET_THREADSTATS que contém o resultado da adição das estatísticas em T1 e T2.</span><span class="sxs-lookup"><span data-stu-id="6a9f0-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6a9f0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a9f0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a9f0-119">Referência</span><span class="sxs-lookup"><span data-stu-id="6a9f0-119">Reference</span></span>

[<span data-ttu-id="6a9f0-120">Estrutura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="6a9f0-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="6a9f0-121">Membros do JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="6a9f0-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="6a9f0-122">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="6a9f0-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
