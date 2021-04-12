---
title: Funções do Gerenciador de tabela de roteamento versão 2
description: As funções a seguir são usadas para interagir com o Gerenciador de tabela de roteamento.
ms.assetid: ac5c6ada-c38e-476a-9896-cdd8c51cc0be
keywords:
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 2, funções
- Gerenciador de tabela de roteamento versão 2 RRAS, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f59e4a1ad2bf091d8a74672f1f473589c5fa1d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364139"
---
# <a name="routing-table-manager-version-2-functions"></a><span data-ttu-id="3d104-105">Funções do Gerenciador de tabela de roteamento versão 2</span><span class="sxs-lookup"><span data-stu-id="3d104-105">Routing Table Manager Version 2 Functions</span></span>

<span data-ttu-id="3d104-106">As funções a seguir são usadas para interagir com o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="3d104-106">The following functions are used to interact with the routing table manager.</span></span>

## <a name="registration-functions"></a><span data-ttu-id="3d104-107">Funções de registro</span><span class="sxs-lookup"><span data-stu-id="3d104-107">Registration Functions</span></span>

[<span data-ttu-id="3d104-108">**RtmRegisterEntity**</span><span class="sxs-lookup"><span data-stu-id="3d104-108">**RtmRegisterEntity**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

[<span data-ttu-id="3d104-109">**RtmDeregisterEntity**</span><span class="sxs-lookup"><span data-stu-id="3d104-109">**RtmDeregisterEntity**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)

[<span data-ttu-id="3d104-110">**RtmGetRegisteredEntities**</span><span class="sxs-lookup"><span data-stu-id="3d104-110">**RtmGetRegisteredEntities**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities)

[<span data-ttu-id="3d104-111">**RtmReleaseEntities**</span><span class="sxs-lookup"><span data-stu-id="3d104-111">**RtmReleaseEntities**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities)

## <a name="opaque-pointer-functions"></a><span data-ttu-id="3d104-112">Funções de ponteiro opaco</span><span class="sxs-lookup"><span data-stu-id="3d104-112">Opaque Pointer Functions</span></span>

[<span data-ttu-id="3d104-113">**RtmLockDestination**</span><span class="sxs-lookup"><span data-stu-id="3d104-113">**RtmLockDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination)

[<span data-ttu-id="3d104-114">**RtmGetOpaqueInformationPointer**</span><span class="sxs-lookup"><span data-stu-id="3d104-114">**RtmGetOpaqueInformationPointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer)

## <a name="export-method-functions"></a><span data-ttu-id="3d104-115">Funções de método de exportação</span><span class="sxs-lookup"><span data-stu-id="3d104-115">Export Method Functions</span></span>

[<span data-ttu-id="3d104-116">**RtmGetEntityMethods**</span><span class="sxs-lookup"><span data-stu-id="3d104-116">**RtmGetEntityMethods**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods)

[<span data-ttu-id="3d104-117">**RtmInvokeMethod**</span><span class="sxs-lookup"><span data-stu-id="3d104-117">**RtmInvokeMethod**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod)

[<span data-ttu-id="3d104-118">**RtmBlockMethods**</span><span class="sxs-lookup"><span data-stu-id="3d104-118">**RtmBlockMethods**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)

## <a name="handle-to-information-structure-functions"></a><span data-ttu-id="3d104-119">Identificador para funções de estrutura de informações</span><span class="sxs-lookup"><span data-stu-id="3d104-119">Handle to Information Structure Functions</span></span>

[<span data-ttu-id="3d104-120">**RtmGetEntityInfo**</span><span class="sxs-lookup"><span data-stu-id="3d104-120">**RtmGetEntityInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)

[<span data-ttu-id="3d104-121">**RtmGetDestInfo**</span><span class="sxs-lookup"><span data-stu-id="3d104-121">**RtmGetDestInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)

[<span data-ttu-id="3d104-122">**RtmGetRouteInfo**</span><span class="sxs-lookup"><span data-stu-id="3d104-122">**RtmGetRouteInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)

[<span data-ttu-id="3d104-123">**RtmGetNextHopInfo**</span><span class="sxs-lookup"><span data-stu-id="3d104-123">**RtmGetNextHopInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

[<span data-ttu-id="3d104-124">**RtmReleaseEntityInfo**</span><span class="sxs-lookup"><span data-stu-id="3d104-124">**RtmReleaseEntityInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)

[<span data-ttu-id="3d104-125">**RtmReleaseDestInfo**</span><span class="sxs-lookup"><span data-stu-id="3d104-125">**RtmReleaseDestInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)

[<span data-ttu-id="3d104-126">**RtmReleaseRouteInfo**</span><span class="sxs-lookup"><span data-stu-id="3d104-126">**RtmReleaseRouteInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo)

[<span data-ttu-id="3d104-127">**RtmReleaseNextHopInfo**</span><span class="sxs-lookup"><span data-stu-id="3d104-127">**RtmReleaseNextHopInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

## <a name="routing-table-insertion-and-deletion-functions"></a><span data-ttu-id="3d104-128">Funções de inserção e exclusão da tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="3d104-128">Routing Table Insertion and Deletion Functions</span></span>

[<span data-ttu-id="3d104-129">**RtmAddRouteToDest**</span><span class="sxs-lookup"><span data-stu-id="3d104-129">**RtmAddRouteToDest**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)

[<span data-ttu-id="3d104-130">**RtmDeleteRouteToDest**</span><span class="sxs-lookup"><span data-stu-id="3d104-130">**RtmDeleteRouteToDest**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest)

[<span data-ttu-id="3d104-131">**RtmHoldDestination**</span><span class="sxs-lookup"><span data-stu-id="3d104-131">**RtmHoldDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination)

[<span data-ttu-id="3d104-132">**RtmGetRoutePointer**</span><span class="sxs-lookup"><span data-stu-id="3d104-132">**RtmGetRoutePointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetroutepointer)

[<span data-ttu-id="3d104-133">**RtmLockRoute**</span><span class="sxs-lookup"><span data-stu-id="3d104-133">**RtmLockRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute)

[<span data-ttu-id="3d104-134">**RtmUpdateAndUnlockRoute**</span><span class="sxs-lookup"><span data-stu-id="3d104-134">**RtmUpdateAndUnlockRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute)

## <a name="routing-table-query-functions"></a><span data-ttu-id="3d104-135">Funções de consulta de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="3d104-135">Routing Table Query Functions</span></span>

[<span data-ttu-id="3d104-136">**RtmGetExactMatchDestination**</span><span class="sxs-lookup"><span data-stu-id="3d104-136">**RtmGetExactMatchDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination)

[<span data-ttu-id="3d104-137">**RtmGetMostSpecificDestination**</span><span class="sxs-lookup"><span data-stu-id="3d104-137">**RtmGetMostSpecificDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)

[<span data-ttu-id="3d104-138">**RtmGetLessSpecificDestination**</span><span class="sxs-lookup"><span data-stu-id="3d104-138">**RtmGetLessSpecificDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination)

[<span data-ttu-id="3d104-139">**RtmGetExactMatchRoute**</span><span class="sxs-lookup"><span data-stu-id="3d104-139">**RtmGetExactMatchRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute)

[<span data-ttu-id="3d104-140">**RtmIsBestRoute**</span><span class="sxs-lookup"><span data-stu-id="3d104-140">**RtmIsBestRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute)

## <a name="next-hop-insertion-and-deletion-functions"></a><span data-ttu-id="3d104-141">Funções de inserção e exclusão de próximo salto</span><span class="sxs-lookup"><span data-stu-id="3d104-141">Next-Hop Insertion and Deletion Functions</span></span>

[<span data-ttu-id="3d104-142">**RtmAddNextHop**</span><span class="sxs-lookup"><span data-stu-id="3d104-142">**RtmAddNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)

[<span data-ttu-id="3d104-143">**RtmFindNextHop**</span><span class="sxs-lookup"><span data-stu-id="3d104-143">**RtmFindNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)

[<span data-ttu-id="3d104-144">**RtmDeleteNextHop**</span><span class="sxs-lookup"><span data-stu-id="3d104-144">**RtmDeleteNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)

[<span data-ttu-id="3d104-145">**RtmGetNextHopPointer**</span><span class="sxs-lookup"><span data-stu-id="3d104-145">**RtmGetNextHopPointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthoppointer)

[<span data-ttu-id="3d104-146">**RtmLockNextHop**</span><span class="sxs-lookup"><span data-stu-id="3d104-146">**RtmLockNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop)

## <a name="routing-table-enumeration-functions"></a><span data-ttu-id="3d104-147">Funções de enumeração da tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="3d104-147">Routing Table Enumeration Functions</span></span>

[<span data-ttu-id="3d104-148">**RtmCreateDestEnum**</span><span class="sxs-lookup"><span data-stu-id="3d104-148">**RtmCreateDestEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum)

[<span data-ttu-id="3d104-149">**RtmGetEnumDests**</span><span class="sxs-lookup"><span data-stu-id="3d104-149">**RtmGetEnumDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests)

[<span data-ttu-id="3d104-150">**RtmReleaseDests**</span><span class="sxs-lookup"><span data-stu-id="3d104-150">**RtmReleaseDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests)

[<span data-ttu-id="3d104-151">**RtmCreateRouteEnum**</span><span class="sxs-lookup"><span data-stu-id="3d104-151">**RtmCreateRouteEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum)

[<span data-ttu-id="3d104-152">**RtmGetEnumRoutes**</span><span class="sxs-lookup"><span data-stu-id="3d104-152">**RtmGetEnumRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes)

[<span data-ttu-id="3d104-153">**RtmReleaseRoutes**</span><span class="sxs-lookup"><span data-stu-id="3d104-153">**RtmReleaseRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes)

[<span data-ttu-id="3d104-154">**RtmCreateNextHopEnum**</span><span class="sxs-lookup"><span data-stu-id="3d104-154">**RtmCreateNextHopEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum)

[<span data-ttu-id="3d104-155">**RtmGetEnumNextHops**</span><span class="sxs-lookup"><span data-stu-id="3d104-155">**RtmGetEnumNextHops**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops)

[<span data-ttu-id="3d104-156">**RtmReleaseNextHops**</span><span class="sxs-lookup"><span data-stu-id="3d104-156">**RtmReleaseNextHops**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops)

[<span data-ttu-id="3d104-157">**RtmDeleteEnumHandle**</span><span class="sxs-lookup"><span data-stu-id="3d104-157">**RtmDeleteEnumHandle**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle)

## <a name="change-notification-functions"></a><span data-ttu-id="3d104-158">Alterar funções de notificação</span><span class="sxs-lookup"><span data-stu-id="3d104-158">Change Notification Functions</span></span>

[<span data-ttu-id="3d104-159">**RtmRegisterForChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="3d104-159">**RtmRegisterForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)

[<span data-ttu-id="3d104-160">**RtmGetChangedDests**</span><span class="sxs-lookup"><span data-stu-id="3d104-160">**RtmGetChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)

[<span data-ttu-id="3d104-161">**RtmReleaseChangedDests**</span><span class="sxs-lookup"><span data-stu-id="3d104-161">**RtmReleaseChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)

[<span data-ttu-id="3d104-162">**RtmIgnoreChangedDests**</span><span class="sxs-lookup"><span data-stu-id="3d104-162">**RtmIgnoreChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)

[<span data-ttu-id="3d104-163">**RtmGetChangeStatus**</span><span class="sxs-lookup"><span data-stu-id="3d104-163">**RtmGetChangeStatus**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)

[<span data-ttu-id="3d104-164">**RtmMarkDestForChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="3d104-164">**RtmMarkDestForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)

[<span data-ttu-id="3d104-165">**RtmIsMarkedForChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="3d104-165">**RtmIsMarkedForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmismarkedforchangenotification)

[<span data-ttu-id="3d104-166">**RtmDeregisterFromChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="3d104-166">**RtmDeregisterFromChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

## <a name="route-list-function"></a><span data-ttu-id="3d104-167">Função de lista de rotas</span><span class="sxs-lookup"><span data-stu-id="3d104-167">Route List Function</span></span>

[<span data-ttu-id="3d104-168">**RtmCreateRouteList**</span><span class="sxs-lookup"><span data-stu-id="3d104-168">**RtmCreateRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist)

[<span data-ttu-id="3d104-169">**RtmInsertInRouteList**</span><span class="sxs-lookup"><span data-stu-id="3d104-169">**RtmInsertInRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist)

[<span data-ttu-id="3d104-170">**RtmCreateRouteListEnum**</span><span class="sxs-lookup"><span data-stu-id="3d104-170">**RtmCreateRouteListEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum)

[<span data-ttu-id="3d104-171">**RtmGetListEnumRoutes**</span><span class="sxs-lookup"><span data-stu-id="3d104-171">**RtmGetListEnumRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes)

[<span data-ttu-id="3d104-172">**RtmDeleteRouteList**</span><span class="sxs-lookup"><span data-stu-id="3d104-172">**RtmDeleteRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist)

## <a name="handle-management-functions"></a><span data-ttu-id="3d104-173">Gerenciar funções de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3d104-173">Handle Management Functions</span></span>

[<span data-ttu-id="3d104-174">**RtmReferenceHandles**</span><span class="sxs-lookup"><span data-stu-id="3d104-174">**RtmReferenceHandles**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles)

 

 




