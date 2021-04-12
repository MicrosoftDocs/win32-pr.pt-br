---
title: Funções de administração de RAS
description: Esta documentação descreve as funções do RRAS que são usadas para desenvolver software para administrar conexões dial-up de RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292700"
---
# <a name="ras-administration-functions"></a><span data-ttu-id="3f033-103">Funções de administração de RAS</span><span class="sxs-lookup"><span data-stu-id="3f033-103">RAS Administration Functions</span></span>

<span data-ttu-id="3f033-104">Esta documentação descreve as funções do RRAS que são usadas para desenvolver software para administrar conexões dial-up de RAS.</span><span class="sxs-lookup"><span data-stu-id="3f033-104">This documentation describes RRAS functions that are used to develop software to administer RAS dial-up connections.</span></span> <span data-ttu-id="3f033-105">Essas funções incluem:</span><span class="sxs-lookup"><span data-stu-id="3f033-105">These functions include:</span></span>

-   [<span data-ttu-id="3f033-106">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="3f033-106">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [<span data-ttu-id="3f033-107">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="3f033-107">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [<span data-ttu-id="3f033-108">**MprAdminConnectionEnumEx**</span><span class="sxs-lookup"><span data-stu-id="3f033-108">**MprAdminConnectionEnumEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [<span data-ttu-id="3f033-109">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="3f033-109">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [<span data-ttu-id="3f033-110">**MprAdminConnectionGetInfoEx**</span><span class="sxs-lookup"><span data-stu-id="3f033-110">**MprAdminConnectionGetInfoEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [<span data-ttu-id="3f033-111">**MprAdminConnectionRemoveQuarantine**</span><span class="sxs-lookup"><span data-stu-id="3f033-111">**MprAdminConnectionRemoveQuarantine**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [<span data-ttu-id="3f033-112">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="3f033-112">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [<span data-ttu-id="3f033-113">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="3f033-113">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [<span data-ttu-id="3f033-114">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="3f033-114">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [<span data-ttu-id="3f033-115">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="3f033-115">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [<span data-ttu-id="3f033-116">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="3f033-116">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

<span data-ttu-id="3f033-117">Funções adicionais são usadas para administração RAS e administração de roteador.</span><span class="sxs-lookup"><span data-stu-id="3f033-117">Additional functions are used for both RAS administration and router administration.</span></span> <span data-ttu-id="3f033-118">As funções a seguir documentadas na referência de [funções de administração do roteador](router-administration-functions.md) :</span><span class="sxs-lookup"><span data-stu-id="3f033-118">The following functions documented in the [Router Administration Functions](router-administration-functions.md) reference:</span></span>

-   [<span data-ttu-id="3f033-119">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="3f033-119">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [<span data-ttu-id="3f033-120">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="3f033-120">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [<span data-ttu-id="3f033-121">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="3f033-121">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [<span data-ttu-id="3f033-122">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="3f033-122">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [<span data-ttu-id="3f033-123">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="3f033-123">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="3f033-124">Para implementar uma DLL de administração de RAS, use as funções descritas no tópico a seguir:</span><span class="sxs-lookup"><span data-stu-id="3f033-124">To implement a RAS administration DLL, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="3f033-125">Funções DLL de administração de RAS</span><span class="sxs-lookup"><span data-stu-id="3f033-125">RAS Admin DLL Functions</span></span>](ras-admin-dll-functions.md)

<span data-ttu-id="3f033-126">Para gerenciar usuários de um servidor RAS, use as funções descritas no tópico a seguir:</span><span class="sxs-lookup"><span data-stu-id="3f033-126">To manage users of a RAS server, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="3f033-127">Funções de administração de usuário RAS</span><span class="sxs-lookup"><span data-stu-id="3f033-127">RAS User Administration Functions</span></span>](ras-user-administration-functions.md)

 

 




