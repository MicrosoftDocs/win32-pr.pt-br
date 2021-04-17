---
description: 'Saiba mais sobre: JET_THREADSTATS. Adicionar método'
title: JET_THREADSTATS. Método Add (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.add(v=EXCHG.10)
ms:contentKeyID: 39514259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Add
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a824249fde43de92c65d64d02fbab4097b7dc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813741"
---
# <a name="jet_threadstatsadd-method"></a><span data-ttu-id="d831d-103">JET_THREADSTATS. Adicionar método</span><span class="sxs-lookup"><span data-stu-id="d831d-103">JET_THREADSTATS.Add method</span></span>

<span data-ttu-id="d831d-104">Adicione as estatísticas em duas estruturas de JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="d831d-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="d831d-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d831d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d831d-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d831d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d831d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d831d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Add ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Add(t1, t2)
```

``` csharp
public static JET_THREADSTATS Add(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="d831d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d831d-108">Parameters</span></span>

  - <span data-ttu-id="d831d-109">t1</span><span class="sxs-lookup"><span data-stu-id="d831d-109">t1</span></span>  
    <span data-ttu-id="d831d-110">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d831d-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="d831d-111">O primeiro JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="d831d-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="d831d-112">T2</span><span class="sxs-lookup"><span data-stu-id="d831d-112">t2</span></span>  
    <span data-ttu-id="d831d-113">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d831d-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="d831d-114">A segunda JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="d831d-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d831d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d831d-115">Return value</span></span>

<span data-ttu-id="d831d-116">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d831d-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="d831d-117">Uma JET_THREADSTATS que contém o resultado da adição das estatísticas em T1 e T2.</span><span class="sxs-lookup"><span data-stu-id="d831d-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d831d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d831d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d831d-119">Referência</span><span class="sxs-lookup"><span data-stu-id="d831d-119">Reference</span></span>

[<span data-ttu-id="d831d-120">Estrutura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="d831d-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="d831d-121">Membros do JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="d831d-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="d831d-122">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="d831d-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
