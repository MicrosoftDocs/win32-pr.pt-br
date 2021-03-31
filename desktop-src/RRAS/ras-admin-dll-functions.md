---
title: Funções DLL de administração de RAS
description: Uma DLL de administração de RAS deve implementar e exportar todas as funções a seguir
ms.assetid: bf2bd4d4-6da2-471e-843c-c0f0563d3795
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a02c8dc9212f3cfd173c9a236f81fcf766658424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641549"
---
# <a name="ras-administration-dll-functions"></a><span data-ttu-id="32d46-103">Funções DLL de administração de RAS</span><span class="sxs-lookup"><span data-stu-id="32d46-103">RAS administration DLL functions</span></span>

<span data-ttu-id="32d46-104">Uma DLL de administração de RAS deve implementar e exportar todas as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="32d46-104">A RAS administration DLL must implement and export all of the following functions:</span></span>

-   [<span data-ttu-id="32d46-105">**MprAdminAcceptNewLink**</span><span class="sxs-lookup"><span data-stu-id="32d46-105">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   <span data-ttu-id="32d46-106">[**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) ou [ **MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span><span class="sxs-lookup"><span data-stu-id="32d46-106">[**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) or [**MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span></span>
-   <span data-ttu-id="32d46-107">[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) ou [ **MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span><span class="sxs-lookup"><span data-stu-id="32d46-107">[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) or [**MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span></span>
-   [<span data-ttu-id="32d46-108">**MprAdminLinkHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="32d46-108">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [<span data-ttu-id="32d46-109">**MprAdminTerminateDll**</span><span class="sxs-lookup"><span data-stu-id="32d46-109">**MprAdminTerminateDll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

<span data-ttu-id="32d46-110">**Windows 2000/NT:** A DLL de administração de RAS também deve implementar e exportar o seguinte par de funções: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) e [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="32d46-110">**Windows 2000/NT:** The RAS administration DLL must also implement and export the following pair of functions: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>

<span data-ttu-id="32d46-111">Além disso, a DLL de administração de RAS deve implementar e exportar um dos seguintes pares de funções:</span><span class="sxs-lookup"><span data-stu-id="32d46-111">In addition, the RAS administration DLL must implement and export one of the following pairs of functions:</span></span>

-   <span data-ttu-id="32d46-112">[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e [ **MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span><span class="sxs-lookup"><span data-stu-id="32d46-112">[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) and [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span></span>
-   <span data-ttu-id="32d46-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) e [ **MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span><span class="sxs-lookup"><span data-stu-id="32d46-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) and [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span></span>
-   <span data-ttu-id="32d46-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) e [ **MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span><span class="sxs-lookup"><span data-stu-id="32d46-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) and [**MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span></span>
-   <span data-ttu-id="32d46-115">[**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) e [ **MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span><span class="sxs-lookup"><span data-stu-id="32d46-115">[**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) and [**MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span></span>

<span data-ttu-id="32d46-116">Se uma das funções necessárias não for implementada, o serviço de acesso remoto não será iniciado.</span><span class="sxs-lookup"><span data-stu-id="32d46-116">If one of the required functions is not implemented, the remote access service fails to start.</span></span>

<span data-ttu-id="32d46-117">Uma DLL de administração não é necessária para implementar os seguintes pares de funções:</span><span class="sxs-lookup"><span data-stu-id="32d46-117">An administration DLL is not required to implement the following pairs of functions:</span></span>

-   <span data-ttu-id="32d46-118">[**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) e [ **MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="32d46-118">[**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>
-   <span data-ttu-id="32d46-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) e [ *MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span><span class="sxs-lookup"><span data-stu-id="32d46-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) and [*MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span></span>

<span data-ttu-id="32d46-120">No entanto, se a DLL implementar uma função em um par listado acima, ela também deverá implementar a outra função no par.</span><span class="sxs-lookup"><span data-stu-id="32d46-120">However, if the DLL implements one function in a pair listed above, it must implement the other function in the pair as well.</span></span>

<span data-ttu-id="32d46-121">Para obter mais informações sobre DLLs de administração de RAS, consulte o tópico Visão geral, [dll de administração de Ras](ras-administration-dll.md).</span><span class="sxs-lookup"><span data-stu-id="32d46-121">For more information on RAS Administration DLLs, see the overview topic, [RAS Administration DLL](ras-administration-dll.md).</span></span>

 

 