---
description: Quando um aplicativo redireciona uma sessão, a TAPI retém informações de identificação sobre o local que redirecionou a sessão e o local para o qual ela foi redirecionada.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Redirecionar identificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780112"
---
# <a name="redirect-identification"></a><span data-ttu-id="df267-103">Redirecionar identificação</span><span class="sxs-lookup"><span data-stu-id="df267-103">Redirect Identification</span></span>

<span data-ttu-id="df267-104">Quando um aplicativo [redireciona](redirect-ovr.md) uma sessão, a TAPI retém informações de identificação sobre o local que redirecionou a sessão e o local para o qual ela foi redirecionada.</span><span class="sxs-lookup"><span data-stu-id="df267-104">When an application [redirects](redirect-ovr.md) a session, TAPI retains identification information about the location that redirected the session and the location to which it was redirected.</span></span>

<span data-ttu-id="df267-105">"Redirecionando" refere-se ao local que invocou a operação de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="df267-105">"Redirecting" refers to the location that invoked the redirect operation.</span></span> <span data-ttu-id="df267-106">"Redirecionamento" identifica o novo destino para a sessão.</span><span class="sxs-lookup"><span data-stu-id="df267-106">"Redirection" identifies the new destination for the session.</span></span>

<span data-ttu-id="df267-107">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="df267-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="df267-108">\* \* TAPI 2. x: \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** e **dwRedirectingIDNameOffset** membros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="df267-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize**, and **dwRedirectingIDNameOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="df267-109">\* \* TAPI 3. x: \* \*[**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)chamado com o **cis \_ REDIRECTIONIDNAME**, **cis \_ REDIRECTIONIDNUMBER**, **cis \_ REDIRECTINGIDNAME** ou o **membro \_ REDIRECTINGIDNUMBER do CIS** da [**cadeia de \_ caracteres CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span><span class="sxs-lookup"><span data-stu-id="df267-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with the **CIS\_REDIRECTIONIDNAME**, **CIS\_REDIRECTIONIDNUMBER**, **CIS\_REDIRECTINGIDNAME**, or **CIS\_REDIRECTINGIDNUMBER** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span></span>

 

 
