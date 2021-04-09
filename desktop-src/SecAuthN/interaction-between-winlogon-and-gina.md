---
description: O Winlogon e a GINA devem comunicar informações de inicialização, lidar com monitoramento e notificação de sequência de atenção segura (SAS) e permitir atividades de logoff e desligamento.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interação entre Winlogon e GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011627"
---
# <a name="interaction-between-winlogon-and-gina"></a><span data-ttu-id="3db1b-103">Interação entre Winlogon e GINA </span><span class="sxs-lookup"><span data-stu-id="3db1b-103">Interaction Between Winlogon and GINA</span></span>

<span data-ttu-id="3db1b-104">O [*Winlogon*](../secgloss/w-gly.md) e a [*Gina*](../secgloss/g-gly.md) devem comunicar informações de inicialização, lidar com monitoramento e notificação de [*sequência de atenção segura*](../secgloss/s-gly.md) (SAS) e permitir atividades de logoff e desligamento.</span><span class="sxs-lookup"><span data-stu-id="3db1b-104">[*Winlogon*](../secgloss/w-gly.md) and the [*GINA*](../secgloss/g-gly.md) must communicate initialization information, handle [*secure attention sequence*](../secgloss/s-gly.md) (SAS) monitoring and notification, and permit logoff and shutdown activities.</span></span> <span data-ttu-id="3db1b-105">O estado do Winlogon determina qual função GINA é chamada para processar qualquer evento SAS específico.</span><span class="sxs-lookup"><span data-stu-id="3db1b-105">The state of Winlogon determines which GINA function is called to process any given SAS event.</span></span> <span data-ttu-id="3db1b-106">As comunicações ocorrem na ordem mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="3db1b-106">Communications occur in the order shown here.</span></span>

> [!Note]  
> <span data-ttu-id="3db1b-107">As DLLs GINAs são ignoradas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3db1b-107">GINA DLLs are ignored in Windows Vista.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3db1b-108">Evento</span><span class="sxs-lookup"><span data-stu-id="3db1b-108">Event</span></span></th>
<th><span data-ttu-id="3db1b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3db1b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3db1b-110">Inicialização da estação de trabalho</span><span class="sxs-lookup"><span data-stu-id="3db1b-110">Workstation boot</span></span></td>
<td><ol>
<li><span data-ttu-id="3db1b-111">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> da Gina para notificar a Gina sobre a versão do Winlogon em uso.</span><span class="sxs-lookup"><span data-stu-id="3db1b-111">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> function to notify the GINA about the version of Winlogon in use.</span></span></li>
<li><span data-ttu-id="3db1b-112">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> da Gina para dar ao Gina os endereços das funções de suporte, um identificador para o Winlogon e obter as informações de <a href="/windows/desktop/SecGloss/c-gly"><em>contexto</em></a> para a Gina (a ser usada em todas as chamadas futuras para a Gina).</span><span class="sxs-lookup"><span data-stu-id="3db1b-112">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> function to give the GINA the addresses of the support functions, a handle to Winlogon, and to obtain the <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> information for the GINA (to be used in all future calls to the GINA).</span></span><br/> <span data-ttu-id="3db1b-113">O Winlogon está no estado de logoff.</span><span class="sxs-lookup"><span data-stu-id="3db1b-113">Winlogon is in the logged-out state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3db1b-114">Ninguém está conectado</span><span class="sxs-lookup"><span data-stu-id="3db1b-114">No one is logged on</span></span></td>
<td><span data-ttu-id="3db1b-115">(A GINA monitora os dispositivos em busca de eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="3db1b-115">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3db1b-116">O GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> do Winlogon quando um evento SAS foi recebido.</span><span class="sxs-lookup"><span data-stu-id="3db1b-116">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="3db1b-117">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> da Gina, permitindo que a Gina processe a identificação de um usuário e as informações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3db1b-117">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> function, allowing the GINA to process a user's identification and authentication information.</span></span><br/> <span data-ttu-id="3db1b-118">Quando o logon for bem-sucedido, o Winlogon estará no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="3db1b-118">When logon is successful, Winlogon is in the logged-on state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3db1b-119">O usuário está conectado</span><span class="sxs-lookup"><span data-stu-id="3db1b-119">The user is logged on</span></span></td>
<td><span data-ttu-id="3db1b-120">(A GINA monitora os dispositivos em busca de eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="3db1b-120">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3db1b-121">O GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> do Winlogon quando um evento SAS foi recebido.</span><span class="sxs-lookup"><span data-stu-id="3db1b-121">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="3db1b-122">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> da Gina, permitindo que a Gina apresente opções ao usuário que está conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="3db1b-122">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function, allowing the GINA to present options to the user who is currently logged on.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3db1b-123">O usuário está conectado e deseja bloquear o computador</span><span class="sxs-lookup"><span data-stu-id="3db1b-123">The user is logged on and wants to lock computer</span></span></td>
<td><span data-ttu-id="3db1b-124">(A GINA monitora os dispositivos em busca de eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="3db1b-124">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3db1b-125">A GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3db1b-125">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-126">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-126">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-127">A GINA retorna WLX_SAS_ACTION_LOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="3db1b-127">The GINA returns WLX_SAS_ACTION_LOCK_WKSTA.</span></span><br/> <span data-ttu-id="3db1b-128">O Winlogon está no estado bloqueado da estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3db1b-128">Winlogon is in the workstation-locked state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3db1b-129">O usuário está conectado, a estação de trabalho está bloqueada e o usuário deseja desbloquear o computador</span><span class="sxs-lookup"><span data-stu-id="3db1b-129">The user is logged on, the workstation is locked, and the user wants to unlock computer</span></span></td>
<td><span data-ttu-id="3db1b-130">(A GINA monitora os dispositivos em busca de eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="3db1b-130">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3db1b-131">A GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3db1b-131">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-132">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-132">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-133">A GINA retorna WLX_SAS_ACTION_UNLOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="3db1b-133">The GINA returns WLX_SAS_ACTION_UNLOCK_WKSTA.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3db1b-134">O usuário está conectado e o programa chama a função <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="3db1b-134">The user is logged on, and the program calls the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> function</span></span></td>
<td><span data-ttu-id="3db1b-135">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-135">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3db1b-136">O usuário está conectado e deseja fazer logoff usando SAS</span><span class="sxs-lookup"><span data-stu-id="3db1b-136">The user is logged on and wants to log off by using SAS</span></span></td>
<td><span data-ttu-id="3db1b-137">(A GINA monitora os dispositivos em busca de eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="3db1b-137">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3db1b-138">A GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3db1b-138">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-139">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-139">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-140">A GINA retorna WLX_SAS_ACTION_LOGOFF.</span><span class="sxs-lookup"><span data-stu-id="3db1b-140">The GINA returns WLX_SAS_ACTION_LOGOFF.</span></span></li>
<li><span data-ttu-id="3db1b-141">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-141">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3db1b-142">O usuário está conectado e deseja fazer logoff e desligar usando o <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="3db1b-142">The user is logged on and wants to log off and shut down by using <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="3db1b-143">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-143">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-144">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-144">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3db1b-145">O usuário está conectado e deseja fazer logoff e desligar usando SAS</span><span class="sxs-lookup"><span data-stu-id="3db1b-145">The user is logged on and wants to log off and shut down by using SAS</span></span></td>
<td><span data-ttu-id="3db1b-146">(A GINA monitora os dispositivos em busca de eventos de SAS).</span><span class="sxs-lookup"><span data-stu-id="3db1b-146">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="3db1b-147">A GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3db1b-147">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-148">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-148">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-149">A GINA retorna WLX_SAS_ACTION_SHUTDOWN.</span><span class="sxs-lookup"><span data-stu-id="3db1b-149">The GINA returns WLX_SAS_ACTION_SHUTDOWN.</span></span></li>
<li><span data-ttu-id="3db1b-150">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-150">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="3db1b-151">O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> da Gina.</span><span class="sxs-lookup"><span data-stu-id="3db1b-151">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
