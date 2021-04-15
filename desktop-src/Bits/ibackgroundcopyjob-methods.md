---
title: Métodos método ibackgroundcopyjob (BITS)
description: A interface método ibackgroundcopyjob expõe os métodos a seguir. | Métodos método ibackgroundcopyjob (BITS)
ms.assetid: CB1C6D64-416A-4F31-AC9D-B3C1A6818034
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a7ebeeefa90c90435f1294d78c4816cf77be3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506385"
---
# <a name="ibackgroundcopyjob-methods-bits"></a><span data-ttu-id="7d984-104">Métodos método ibackgroundcopyjob (BITS)</span><span class="sxs-lookup"><span data-stu-id="7d984-104">IBackgroundCopyJob Methods (BITS)</span></span>

<span data-ttu-id="7d984-105">A interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) expõe os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d984-105">The [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7d984-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7d984-106">In this section</span></span>

-   [<span data-ttu-id="7d984-107">**Método AddFile**</span><span class="sxs-lookup"><span data-stu-id="7d984-107">**AddFile Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
-   [<span data-ttu-id="7d984-108">**Método addfileset**</span><span class="sxs-lookup"><span data-stu-id="7d984-108">**AddFileSet Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
-   [<span data-ttu-id="7d984-109">**Método Cancel**</span><span class="sxs-lookup"><span data-stu-id="7d984-109">**Cancel Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   [<span data-ttu-id="7d984-110">**Método Complete**</span><span class="sxs-lookup"><span data-stu-id="7d984-110">**Complete Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)
-   [<span data-ttu-id="7d984-111">**Método EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="7d984-111">**EnumFiles Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles)
-   [<span data-ttu-id="7d984-112">**Método GetDescription**</span><span class="sxs-lookup"><span data-stu-id="7d984-112">**GetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdescription)
-   [<span data-ttu-id="7d984-113">**Método GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="7d984-113">**GetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)
-   [<span data-ttu-id="7d984-114">**Método GetError**</span><span class="sxs-lookup"><span data-stu-id="7d984-114">**GetError Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror)
-   [<span data-ttu-id="7d984-115">**Método GetErrorCount**</span><span class="sxs-lookup"><span data-stu-id="7d984-115">**GetErrorCount Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterrorcount)
-   [<span data-ttu-id="7d984-116">**Método GetId**</span><span class="sxs-lookup"><span data-stu-id="7d984-116">**GetId Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getid)
-   [<span data-ttu-id="7d984-117">**Método GetMinimumRetryDelay**</span><span class="sxs-lookup"><span data-stu-id="7d984-117">**GetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay)
-   [<span data-ttu-id="7d984-118">**Método GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="7d984-118">**GetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout)
-   [<span data-ttu-id="7d984-119">**Método GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="7d984-119">**GetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyflags)
-   [<span data-ttu-id="7d984-120">**Método GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="7d984-120">**GetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyinterface)
-   [<span data-ttu-id="7d984-121">**Método GetOwner**</span><span class="sxs-lookup"><span data-stu-id="7d984-121">**GetOwner Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)
-   [<span data-ttu-id="7d984-122">**Método GetPriority**</span><span class="sxs-lookup"><span data-stu-id="7d984-122">**GetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getpriority)
-   [<span data-ttu-id="7d984-123">**Método GetProgress**</span><span class="sxs-lookup"><span data-stu-id="7d984-123">**GetProgress Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)
-   [<span data-ttu-id="7d984-124">**Método GetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="7d984-124">**GetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getproxysettings)
-   [<span data-ttu-id="7d984-125">**Método GetState**</span><span class="sxs-lookup"><span data-stu-id="7d984-125">**GetState Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate)
-   [<span data-ttu-id="7d984-126">**Método gettimeies**</span><span class="sxs-lookup"><span data-stu-id="7d984-126">**GetTimes Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettimes)
-   [<span data-ttu-id="7d984-127">**Método GetType**</span><span class="sxs-lookup"><span data-stu-id="7d984-127">**GetType Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettype)
-   [<span data-ttu-id="7d984-128">**Método resume**</span><span class="sxs-lookup"><span data-stu-id="7d984-128">**Resume Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
-   [<span data-ttu-id="7d984-129">**Método SetDescription**</span><span class="sxs-lookup"><span data-stu-id="7d984-129">**SetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdescription)
-   [<span data-ttu-id="7d984-130">**Método SetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="7d984-130">**SetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdisplayname)
-   [<span data-ttu-id="7d984-131">**Método SetMinimumRetryDelay**</span><span class="sxs-lookup"><span data-stu-id="7d984-131">**SetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay)
-   [<span data-ttu-id="7d984-132">**Método SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="7d984-132">**SetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout)
-   [<span data-ttu-id="7d984-133">**Método SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="7d984-133">**SetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)
-   [<span data-ttu-id="7d984-134">**Método SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="7d984-134">**SetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)
-   [<span data-ttu-id="7d984-135">**Método SetPriority**</span><span class="sxs-lookup"><span data-stu-id="7d984-135">**SetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority)
-   [<span data-ttu-id="7d984-136">**Método SetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="7d984-136">**SetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)
-   [<span data-ttu-id="7d984-137">**Método Suspend**</span><span class="sxs-lookup"><span data-stu-id="7d984-137">**Suspend Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend)
-   [<span data-ttu-id="7d984-138">**Método TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="7d984-138">**TakeOwnership Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)

 

 




