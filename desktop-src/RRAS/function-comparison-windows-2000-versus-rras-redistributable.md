---
title: Comparação de funções Windows 2000 versus RRAS redistribuível
description: A API RAS é distribuída como um recurso do Windows 2000 e sistemas operacionais posteriores e está disponível como um pacote redistribuível para o Windows NT 4,0 com Service Pack 3 (SP3) e anterior.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748748"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a><span data-ttu-id="16dda-103">Comparação de funções: Windows 2000 x RRAS redistribuível</span><span class="sxs-lookup"><span data-stu-id="16dda-103">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>

<span data-ttu-id="16dda-104">A API RAS é distribuída como um recurso do Windows 2000 e sistemas operacionais posteriores e está disponível como um pacote redistribuível para o Windows NT 4,0 com Service Pack 3 (SP3) e anterior.</span><span class="sxs-lookup"><span data-stu-id="16dda-104">The RAS API is distributed as a feature of Windows 2000 and later operating systems and is available as a redistributable for Windows NT 4.0 with Service Pack 3 (SP3) and earlier.</span></span> <span data-ttu-id="16dda-105">O RAS fornece a mesma funcionalidade em ambos os formulários, mas a Convenção de nomenclatura usada é diferente para os elementos de referência em cada versão da API RAS.</span><span class="sxs-lookup"><span data-stu-id="16dda-105">RAS provides the same functionality in both of these forms but the naming convention that is used is different for the reference elements in each version of the RAS API.</span></span>

<span data-ttu-id="16dda-106">As funções RAS para Windows NT 4,0 com SP3 e versões anteriores normalmente começam com o prefixo "RasAdmin".</span><span class="sxs-lookup"><span data-stu-id="16dda-106">The RAS functions for Windows NT 4.0 with SP3 and earlier typically begin with the "RasAdmin" prefix.</span></span> <span data-ttu-id="16dda-107">As funções análogas para roteamento e serviço de acesso remoto (RRAS) começam com o prefixo "MprAdmin".</span><span class="sxs-lookup"><span data-stu-id="16dda-107">The analogous functions for Routing and Remote Access Service (RRAS) begin with the "MprAdmin" prefix.</span></span> <span data-ttu-id="16dda-108">Por exemplo, o RAS fornece uma função chamada [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span><span class="sxs-lookup"><span data-stu-id="16dda-108">For example, RAS provides a function called [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span></span> <span data-ttu-id="16dda-109">A função análoga no RRAS é chamada de [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span><span class="sxs-lookup"><span data-stu-id="16dda-109">The analogous function in RRAS is called [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span></span> <span data-ttu-id="16dda-110">Como exemplo semelhante, o RAS fornece a função de retorno de chamada [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="16dda-110">As a similar example, RAS provides the callback function [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span> <span data-ttu-id="16dda-111">O RRAS fornece uma função de retorno de chamada semelhante chamada [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span><span class="sxs-lookup"><span data-stu-id="16dda-111">RRAS provides a similar callback function called [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span></span> <span data-ttu-id="16dda-112">As exceções a essa regra são [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), que sob o RRAS é [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), e [**RASADMINFREEBUFFER**](rasadminfreebuffer.md), que sob o RRAS é [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span><span class="sxs-lookup"><span data-stu-id="16dda-112">Exceptions to this rule are [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), which under RRAS is [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), and [**RasAdminFreeBuffer**](rasadminfreebuffer.md), which under RRAS is [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span></span>

<span data-ttu-id="16dda-113">A tabela a seguir lista as funções RAS do Windows NT 4,0 SP3 e as funções de RRAS correspondentes.</span><span class="sxs-lookup"><span data-stu-id="16dda-113">The following table lists the Windows NT 4.0 SP3 RAS functions and the corresponding RRAS functions.</span></span>



| <span data-ttu-id="16dda-114">RAS do Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="16dda-114">Windows NT 4.0 RAS</span></span>                                                                   | <span data-ttu-id="16dda-115">RRAS</span><span class="sxs-lookup"><span data-stu-id="16dda-115">RRAS</span></span>                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="16dda-116">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="16dda-116">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)                   | [<span data-ttu-id="16dda-117">**MprAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="16dda-117">**MprAdminAcceptNewConnection**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [<span data-ttu-id="16dda-118">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="16dda-118">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md) | [<span data-ttu-id="16dda-119">**MprAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="16dda-119">**MprAdminConnectionHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [<span data-ttu-id="16dda-120">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="16dda-120">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)                                     | [<span data-ttu-id="16dda-121">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="16dda-121">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [<span data-ttu-id="16dda-122">**RasAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="16dda-122">**RasAdminGetErrorString**</span></span>](rasadmingeterrorstring.md)                             | [<span data-ttu-id="16dda-123">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="16dda-123">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [<span data-ttu-id="16dda-124">**RasAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="16dda-124">**RasAdminGetIpAddressForUser**</span></span>](rasadmingetipaddressforuser.md)                   | [<span data-ttu-id="16dda-125">**MprAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="16dda-125">**MprAdminGetIpAddressForUser**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [<span data-ttu-id="16dda-126">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="16dda-126">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)                   | [<span data-ttu-id="16dda-127">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="16dda-127">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [<span data-ttu-id="16dda-128">**RasAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="16dda-128">**RasAdminPortDisconnect**</span></span>](rasadminportdisconnect.md)                             | [<span data-ttu-id="16dda-129">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="16dda-129">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [<span data-ttu-id="16dda-130">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="16dda-130">**RasAdminPortEnum**</span></span>](rasadminportenum.md)                                         | [<span data-ttu-id="16dda-131">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="16dda-131">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [<span data-ttu-id="16dda-132">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="16dda-132">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)                                   | [<span data-ttu-id="16dda-133">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="16dda-133">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [<span data-ttu-id="16dda-134">**RasAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="16dda-134">**RasAdminReleaseIpAddress**</span></span>](rasadminreleaseipaddress.md)                         | [<span data-ttu-id="16dda-135">**MprAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="16dda-135">**MprAdminReleaseIpAddress**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [<span data-ttu-id="16dda-136">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="16dda-136">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)                                   | [<span data-ttu-id="16dda-137">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="16dda-137">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [<span data-ttu-id="16dda-138">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="16dda-138">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)                                   | [<span data-ttu-id="16dda-139">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="16dda-139">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

<span data-ttu-id="16dda-140">Embora as funções de RRAS sejam semelhantes às do Windows NT 4,0 com SP3 e às contrapartes RAS anteriores na funcionalidade, as funções de RRAS geralmente usam um conjunto diferente de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="16dda-140">Although the RRAS functions are similar to their Windows NT 4.0 with SP3 and earlier RAS counterparts in functionality, RRAS functions often take a different set of parameters.</span></span> <span data-ttu-id="16dda-141">Consulte a página de referência de uma função específica para obter informações completas sobre a lista de parâmetros da função.</span><span class="sxs-lookup"><span data-stu-id="16dda-141">See the reference page for a particular function for complete information on that function's parameter list.</span></span>

<span data-ttu-id="16dda-142">O RRAS redistribuível para Windows NT 4,0 com SP3 e versões anteriores adiciona as seguintes funções, que não têm nenhuma contraparte de RAS:</span><span class="sxs-lookup"><span data-stu-id="16dda-142">The RRAS redistributable for Windows NT 4.0 with SP3 and earlier adds the following functions, which have no RAS counterparts:</span></span>

[<span data-ttu-id="16dda-143">**MprAdminAcceptNewLink**</span><span class="sxs-lookup"><span data-stu-id="16dda-143">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[<span data-ttu-id="16dda-144">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="16dda-144">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[<span data-ttu-id="16dda-145">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="16dda-145">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[<span data-ttu-id="16dda-146">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="16dda-146">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[<span data-ttu-id="16dda-147">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="16dda-147">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[<span data-ttu-id="16dda-148">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="16dda-148">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[<span data-ttu-id="16dda-149">**MprAdminLinkHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="16dda-149">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[<span data-ttu-id="16dda-150">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="16dda-150">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[<span data-ttu-id="16dda-151">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="16dda-151">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[<span data-ttu-id="16dda-152">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="16dda-152">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="16dda-153">Além das funções anteriores, os sistemas operacionais Windows 2000 e posteriores adicionam as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="16dda-153">In addition to the preceding functions, Windows 2000 and later operating systems add the following functions:</span></span>

[<span data-ttu-id="16dda-154">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="16dda-154">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[<span data-ttu-id="16dda-155">**MprAdminAcceptNewConnection2**</span><span class="sxs-lookup"><span data-stu-id="16dda-155">**MprAdminAcceptNewConnection2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[<span data-ttu-id="16dda-156">**MprAdminConnectionHangupNotification2**</span><span class="sxs-lookup"><span data-stu-id="16dda-156">**MprAdminConnectionHangupNotification2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




