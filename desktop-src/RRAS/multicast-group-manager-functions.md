---
title: Funções do Gerenciador de grupos multicast
description: As funções a seguir são usadas para registrar com o Gerenciador de grupo de multicast
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292720"
---
# <a name="multicast-group-manager-functions"></a><span data-ttu-id="319ff-103">Funções do Gerenciador de grupos multicast</span><span class="sxs-lookup"><span data-stu-id="319ff-103">Multicast Group Manager Functions</span></span>

<span data-ttu-id="319ff-104">As funções a seguir são usadas para registrar com o Gerenciador do grupo de multicast:</span><span class="sxs-lookup"><span data-stu-id="319ff-104">The following functions are used to register with the multicast group manager:</span></span>

[<span data-ttu-id="319ff-105">**MgmRegisterMProtocol**</span><span class="sxs-lookup"><span data-stu-id="319ff-105">**MgmRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[<span data-ttu-id="319ff-106">**MgmDeRegisterMProtocol**</span><span class="sxs-lookup"><span data-stu-id="319ff-106">**MgmDeRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

<span data-ttu-id="319ff-107">As funções a seguir são usadas para gerenciar a propriedade da interface:</span><span class="sxs-lookup"><span data-stu-id="319ff-107">The following functions are used to manage interface ownership:</span></span>

[<span data-ttu-id="319ff-108">**MgmGetProtocolOnInterface**</span><span class="sxs-lookup"><span data-stu-id="319ff-108">**MgmGetProtocolOnInterface**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[<span data-ttu-id="319ff-109">**MgmTakeInterfaceOwnership**</span><span class="sxs-lookup"><span data-stu-id="319ff-109">**MgmTakeInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[<span data-ttu-id="319ff-110">**MgmReleaseInterfaceOwnership**</span><span class="sxs-lookup"><span data-stu-id="319ff-110">**MgmReleaseInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

<span data-ttu-id="319ff-111">As funções a seguir são usadas para gerenciar a associação de Grupo:</span><span class="sxs-lookup"><span data-stu-id="319ff-111">The following functions are used to manage group membership:</span></span>

[<span data-ttu-id="319ff-112">**MgmAddGroupMembershipEntry**</span><span class="sxs-lookup"><span data-stu-id="319ff-112">**MgmAddGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[<span data-ttu-id="319ff-113">**MgmDeleteGroupMembershipEntry**</span><span class="sxs-lookup"><span data-stu-id="319ff-113">**MgmDeleteGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

<span data-ttu-id="319ff-114">As funções a seguir são usadas para obter entradas de encaminhamento de multicast (MFEs) e estatísticas de MFE:</span><span class="sxs-lookup"><span data-stu-id="319ff-114">The following functions are used to obtain multicast forwarding entries (MFEs) and MFE statistics:</span></span>

[<span data-ttu-id="319ff-115">**MgmGetFirstMfe**</span><span class="sxs-lookup"><span data-stu-id="319ff-115">**MgmGetFirstMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[<span data-ttu-id="319ff-116">**MgmGetNextMfe**</span><span class="sxs-lookup"><span data-stu-id="319ff-116">**MgmGetNextMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[<span data-ttu-id="319ff-117">**MgmGetMfe**</span><span class="sxs-lookup"><span data-stu-id="319ff-117">**MgmGetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[<span data-ttu-id="319ff-118">**MgmGetFirstMfeStats**</span><span class="sxs-lookup"><span data-stu-id="319ff-118">**MgmGetFirstMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[<span data-ttu-id="319ff-119">**MgmGetNextMfeStats**</span><span class="sxs-lookup"><span data-stu-id="319ff-119">**MgmGetNextMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[<span data-ttu-id="319ff-120">**MgmGetMfeStats**</span><span class="sxs-lookup"><span data-stu-id="319ff-120">**MgmGetMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

<span data-ttu-id="319ff-121">A função a seguir é usada para modificar MFEs:</span><span class="sxs-lookup"><span data-stu-id="319ff-121">The following function is used to modify MFEs:</span></span>

[<span data-ttu-id="319ff-122">**MgmSetMfe**</span><span class="sxs-lookup"><span data-stu-id="319ff-122">**MgmSetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

<span data-ttu-id="319ff-123">As funções a seguir são usadas para obter uma lista de grupos que foram associados:</span><span class="sxs-lookup"><span data-stu-id="319ff-123">The following functions are used obtain a list of groups that have been joined:</span></span>

[<span data-ttu-id="319ff-124">**MgmGroupEnumerationStart**</span><span class="sxs-lookup"><span data-stu-id="319ff-124">**MgmGroupEnumerationStart**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[<span data-ttu-id="319ff-125">**MgmGroupEnumerationGetNext**</span><span class="sxs-lookup"><span data-stu-id="319ff-125">**MgmGroupEnumerationGetNext**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[<span data-ttu-id="319ff-126">**MgmGroupEnumerationEnd**</span><span class="sxs-lookup"><span data-stu-id="319ff-126">**MgmGroupEnumerationEnd**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




