---
title: O que há de novo no gerenciamento de rede
description: O que há de novo no gerenciamento de rede
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104366898"
---
# <a name="whats-new-in-network-management"></a><span data-ttu-id="ffbc1-103">O que há de novo no gerenciamento de rede</span><span class="sxs-lookup"><span data-stu-id="ffbc1-103">What's New in Network Management</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="ffbc1-104">Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffbc1-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="ffbc1-105">O Microsoft Windows 8 apresenta novos recursos de programação de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-105">Microsoft Windows 8 introduces new Network Management programming features.</span></span> <span data-ttu-id="ffbc1-106">Esses novos elementos estendem a funcionalidade do gerenciamento de rede para criar pacotes de provisionamento para operações de ingresso no domínio offline ao provisionar computadores com o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-106">These new elements extend the capability of Network Management to create provisioning packages for offline domain join operations when provisioning computers with Windows 8.</span></span>

<span data-ttu-id="ffbc1-107">A seguir estão as novas funções de gerenciamento de rede:</span><span class="sxs-lookup"><span data-stu-id="ffbc1-107">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="ffbc1-108">**NetCreateProvisioningPackage**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-108">**NetCreateProvisioningPackage**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="ffbc1-109">**NetRequestProvisioningPackageInstall**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-109">**NetRequestProvisioningPackageInstall**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

<span data-ttu-id="ffbc1-110">A seguir estão as novas estruturas de gerenciamento de rede:</span><span class="sxs-lookup"><span data-stu-id="ffbc1-110">The following are new Network Management structures:</span></span>

-   [<span data-ttu-id="ffbc1-111">**parâmetros de provisionamento do Netsetup \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-111">**NETSETUP\_PROVISIONING\_PARAMS**</span></span>](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [<span data-ttu-id="ffbc1-112">**Informações do usuário \_ \_ 24**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-112">**USER\_INFO\_24**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

<span data-ttu-id="ffbc1-113">A função [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) foi aprimorada no Windows 8 para dar suporte a um novo nível de informações e retornar uma estrutura de informações de [**usuário \_ \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) com informações de conta de usuário para uma conta conectada a uma identidade de Internet.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-113">The [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) function has been enhanced on Windows 8 to support a new information level and return a [**USER\_INFO\_24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) structure with user account information for an account connected to an Internet identity.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="ffbc1-114">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffbc1-114">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="ffbc1-115">O Microsoft Windows 7 apresenta novos recursos de programação de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-115">Microsoft Windows 7 introduces new Network Management programming features.</span></span> <span data-ttu-id="ffbc1-116">Esses elementos estendem a capacidade do gerenciamento de rede para permitir operações de ingresso no domínio offline ao provisionar computadores com o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-116">These elements extend the capability of Network Management to allow offline domain join operations when provisioning computers with Windows 7.</span></span>

<span data-ttu-id="ffbc1-117">A seguir estão as novas funções de gerenciamento de rede:</span><span class="sxs-lookup"><span data-stu-id="ffbc1-117">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="ffbc1-118">**NetProvisionComputerAccount**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-118">**NetProvisionComputerAccount**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="ffbc1-119">**NetRequestOfflineDomainJoin**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-119">**NetRequestOfflineDomainJoin**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

<span data-ttu-id="ffbc1-120">As seguintes funções de gerenciamento de rede existentes foram aprimoradas para dar suporte a opções adicionais:</span><span class="sxs-lookup"><span data-stu-id="ffbc1-120">The following existing Network Management functions were enhanced to support additional options:</span></span>

-   [<span data-ttu-id="ffbc1-121">**NetJoinDomain**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-121">**NetJoinDomain**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a><span data-ttu-id="ffbc1-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ffbc1-122">Windows Server 2003</span></span>

<span data-ttu-id="ffbc1-123">O Microsoft Windows Server 2003 apresenta novos recursos de programação de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-123">Microsoft Windows Server 2003 introduces new Network Management programming features.</span></span> <span data-ttu-id="ffbc1-124">Esses elementos estendem o recurso de operações de gerenciamento de rede no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-124">These elements extend the capability of Network Management operations on Windows Server 2003 and later.</span></span>

## <a name="windows-xp"></a><span data-ttu-id="ffbc1-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ffbc1-125">Windows XP</span></span>

<span data-ttu-id="ffbc1-126">O Microsoft Windows XP apresenta novos recursos de programação de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-126">Microsoft Windows XP introduces new Network Management programming features.</span></span> <span data-ttu-id="ffbc1-127">Esses elementos estendem o recurso de operações de gerenciamento de rede no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-127">These elements extend the capability of Network Management operations on Windows XP and later.</span></span>

<span data-ttu-id="ffbc1-128">A seguir estão as novas funções de gerenciamento de rede:</span><span class="sxs-lookup"><span data-stu-id="ffbc1-128">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="ffbc1-129">**NetAddAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-129">**NetAddAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [<span data-ttu-id="ffbc1-130">**NetEnumerateComputerNames**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-130">**NetEnumerateComputerNames**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [<span data-ttu-id="ffbc1-131">**NetRemoveAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-131">**NetRemoveAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [<span data-ttu-id="ffbc1-132">**NetSetPrimaryComputerName**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-132">**NetSetPrimaryComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [<span data-ttu-id="ffbc1-133">**SetNetScheduleAccountInformation**</span><span class="sxs-lookup"><span data-stu-id="ffbc1-133">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




