---
description: Você pode usar as funções a seguir para trabalhar com dados de desempenho no Visual Basic.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Funções de contadores de desempenho para Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828381"
---
# <a name="performance-counters-functions-for-visual-basic"></a><span data-ttu-id="af91a-103">Funções de contadores de desempenho para Visual Basic</span><span class="sxs-lookup"><span data-stu-id="af91a-103">Performance Counters Functions for Visual Basic</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af91a-104">As funções descritas neste tópico podem ser alteradas ou não disponíveis no futuro.</span><span class="sxs-lookup"><span data-stu-id="af91a-104">The functions that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="af91a-105">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="af91a-105">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="af91a-106">Você pode usar as funções a seguir para trabalhar com dados de desempenho no Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="af91a-106">You can use the following functions to work with performance data in Visual Basic.</span></span>

- [<span data-ttu-id="af91a-107">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="af91a-107">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="af91a-108">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="af91a-108">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="af91a-109">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="af91a-109">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="af91a-110">**PdhVbAddCounter**</span><span class="sxs-lookup"><span data-stu-id="af91a-110">**PdhVbAddCounter**</span></span>](pdhvbaddcounter.md)
- [<span data-ttu-id="af91a-111">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="af91a-111">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
- [<span data-ttu-id="af91a-112">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="af91a-112">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
- [<span data-ttu-id="af91a-113">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="af91a-113">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
- [<span data-ttu-id="af91a-114">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="af91a-114">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
- [<span data-ttu-id="af91a-115">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="af91a-115">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
- [<span data-ttu-id="af91a-116">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="af91a-116">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
- [<span data-ttu-id="af91a-117">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="af91a-117">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
- [<span data-ttu-id="af91a-118">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="af91a-118">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
- [<span data-ttu-id="af91a-119">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="af91a-119">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
- [<span data-ttu-id="af91a-120">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="af91a-120">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)

> [!NOTE]
> <span data-ttu-id="af91a-121">As `PdhVb***` funções funcionam em uma sessão por processo e não são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="af91a-121">The `PdhVb***` functions work on a per-process session and are not thread-safe.</span></span> <span data-ttu-id="af91a-122">Essas funções só devem ser usadas de aplicativos simples de thread único.</span><span class="sxs-lookup"><span data-stu-id="af91a-122">These functions should only be used from simple single-threaded applications.</span></span>
