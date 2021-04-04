---
title: Configurações do registro de porta do firewall
description: Configurações do registro de porta do firewall
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, configurações do registro de porta do firewall
- Windows Media Player, configurações do registro de porta
- Windows Media Player, registro
- configurações de porta do registro, firewall
- registro, configurações de porta
- registro, configurações do Windows Media Player
- configurações do registro de porta do firewall
- configurações do registro de porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822342"
---
# <a name="firewall-port-registry-settings"></a><span data-ttu-id="55419-111">Configurações do registro de porta do firewall</span><span class="sxs-lookup"><span data-stu-id="55419-111">Firewall Port Registry Settings</span></span>

<span data-ttu-id="55419-112">O Windows Media Player coloca entradas no registro para que os firewalls possam determinar se devem ser abertas ou fechadas as portas usadas pelo compartilhamento de biblioteca de mídia.</span><span class="sxs-lookup"><span data-stu-id="55419-112">Windows Media Player places entries in the registry so that firewalls can determine whether to open or close the ports that are used by media library sharing.</span></span>

<span data-ttu-id="55419-113">**Entrada do registro AcceptedEULA**</span><span class="sxs-lookup"><span data-stu-id="55419-113">**AcceptedEULA Registry Entry**</span></span>

<span data-ttu-id="55419-114">O Windows Media Player usa a seguinte entrada de registro para indicar se o usuário aceitou o EULA (contrato de licença de usuário final).</span><span class="sxs-lookup"><span data-stu-id="55419-114">Windows Media Player uses the following registry entry to indicate whether the user has accepted the end user license agreement (EULA).</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



<span data-ttu-id="55419-115">Um valor de 1 indica que o usuário aceitou o contrato de licença.</span><span class="sxs-lookup"><span data-stu-id="55419-115">A value of 1 indicates that the user has accepted the license agreement.</span></span> <span data-ttu-id="55419-116">Um valor de 0 indica que o usuário não aceitou o contrato de licença.</span><span class="sxs-lookup"><span data-stu-id="55419-116">A value of 0 indicates that the user has not accepted the license agreement.</span></span>

<span data-ttu-id="55419-117">**Entrada do registro WMPNSSFirewallPortsOpen**</span><span class="sxs-lookup"><span data-stu-id="55419-117">**WMPNSSFirewallPortsOpen Registry Entry**</span></span>

<span data-ttu-id="55419-118">O Windows Media Player usa a seguinte entrada de registro para indicar se o usuário optou por compartilhar sua biblioteca de mídias com outros computadores em uma rede doméstica.</span><span class="sxs-lookup"><span data-stu-id="55419-118">Windows Media Player uses the following registry entry to indicate whether the user has chosen to share his or her media library with other computers on a home network.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



<span data-ttu-id="55419-119">Um valor de 1 indica que o usuário optou por compartilhar a biblioteca.</span><span class="sxs-lookup"><span data-stu-id="55419-119">A value of 1 indicates that the user has chosen to share the library.</span></span> <span data-ttu-id="55419-120">Um valor de 0 indica que o usuário optou por não compartilhar a biblioteca.</span><span class="sxs-lookup"><span data-stu-id="55419-120">A value of 0 indicates that the user has chosen not to share the library.</span></span>

<span data-ttu-id="55419-121">**Portas relacionadas ao compartilhamento de biblioteca de mídia**</span><span class="sxs-lookup"><span data-stu-id="55419-121">**Ports Related to Media Library Sharing**</span></span>

<span data-ttu-id="55419-122">No Windows Vista, se a entrada do registro **WMPNSSFirewallPortsOpen** tiver um valor de 1, as portas a seguir deverão ser abertas.</span><span class="sxs-lookup"><span data-stu-id="55419-122">On Windows Vista, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="55419-123">Porta</span><span class="sxs-lookup"><span data-stu-id="55419-123">Port</span></span>          | <span data-ttu-id="55419-124">Protocolo</span><span class="sxs-lookup"><span data-stu-id="55419-124">Protocol</span></span>                  | <span data-ttu-id="55419-125">Processar</span><span class="sxs-lookup"><span data-stu-id="55419-125">Process</span></span>                         | <span data-ttu-id="55419-126">Direção</span><span class="sxs-lookup"><span data-stu-id="55419-126">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="55419-127">554</span><span class="sxs-lookup"><span data-stu-id="55419-127">554</span></span>           | <span data-ttu-id="55419-128">RTSP TCP</span><span class="sxs-lookup"><span data-stu-id="55419-128">TCP RTSP</span></span>                  | <span data-ttu-id="55419-129">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="55419-129">wmpnetwk.exe</span></span>                    | <span data-ttu-id="55419-130">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-130">inbound and outbound</span></span> |
| <span data-ttu-id="55419-131">8554-8558</span><span class="sxs-lookup"><span data-stu-id="55419-131">8554 - 8558</span></span>   | <span data-ttu-id="55419-132">RTSP TCP</span><span class="sxs-lookup"><span data-stu-id="55419-132">TCP RTSP</span></span>                  | <span data-ttu-id="55419-133">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="55419-133">wmpnetwk.exe</span></span>                    | <span data-ttu-id="55419-134">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-134">inbound and outbound</span></span> |
| <span data-ttu-id="55419-135">5004, 5005</span><span class="sxs-lookup"><span data-stu-id="55419-135">5004, 5005</span></span>    | <span data-ttu-id="55419-136">UDP RTCP/RTP</span><span class="sxs-lookup"><span data-stu-id="55419-136">UDP RTCP/RTP</span></span>              | <span data-ttu-id="55419-137">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="55419-137">wmpnetwk.exe</span></span>                    | <span data-ttu-id="55419-138">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-138">inbound and outbound</span></span> |
| <span data-ttu-id="55419-139">50004-50013</span><span class="sxs-lookup"><span data-stu-id="55419-139">50004 - 50013</span></span> | <span data-ttu-id="55419-140">UDP RTCP/RTP</span><span class="sxs-lookup"><span data-stu-id="55419-140">UDP RTCP/RTP</span></span>              | <span data-ttu-id="55419-141">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="55419-141">wmpnetwk.exe</span></span>                    | <span data-ttu-id="55419-142">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-142">inbound and outbound</span></span> |
| <span data-ttu-id="55419-143">1900</span><span class="sxs-lookup"><span data-stu-id="55419-143">1900</span></span>          | <span data-ttu-id="55419-144">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="55419-144">UDP SSDP</span></span>                  | <span data-ttu-id="55419-145">SSDPsrv em svchost.exe</span><span class="sxs-lookup"><span data-stu-id="55419-145">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="55419-146">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-146">inbound and outbound</span></span> |
| <span data-ttu-id="55419-147">2869</span><span class="sxs-lookup"><span data-stu-id="55419-147">2869</span></span>          | <span data-ttu-id="55419-148">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="55419-148">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="55419-149">SSDPsrv/UPnPHost no svchost.exe</span><span class="sxs-lookup"><span data-stu-id="55419-149">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="55419-150">entrada</span><span class="sxs-lookup"><span data-stu-id="55419-150">inbound</span></span>              |
| <span data-ttu-id="55419-151">10280-10284</span><span class="sxs-lookup"><span data-stu-id="55419-151">10280 - 10284</span></span> | <span data-ttu-id="55419-152">Registro de WMDRM-ND de UDP</span><span class="sxs-lookup"><span data-stu-id="55419-152">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="55419-153">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="55419-153">wmpnetwk.exe</span></span>                    | <span data-ttu-id="55419-154">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-154">inbound and outbound</span></span> |
| <span data-ttu-id="55419-155">10243</span><span class="sxs-lookup"><span data-stu-id="55419-155">10243</span></span>         | <span data-ttu-id="55419-156">HTTP TCP</span><span class="sxs-lookup"><span data-stu-id="55419-156">TCP HTTP</span></span>                  | <span data-ttu-id="55419-157">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="55419-157">wmpnetwk.exe</span></span>                    | <span data-ttu-id="55419-158">entrada</span><span class="sxs-lookup"><span data-stu-id="55419-158">inbound</span></span>              |
| <span data-ttu-id="55419-159">2177</span><span class="sxs-lookup"><span data-stu-id="55419-159">2177</span></span>          | <span data-ttu-id="55419-160">QWAVE TCP UDP</span><span class="sxs-lookup"><span data-stu-id="55419-160">TCP UDP qWAVE</span></span>             | <span data-ttu-id="55419-161">svchost.exe</span><span class="sxs-lookup"><span data-stu-id="55419-161">svchost.exe</span></span>                     | <span data-ttu-id="55419-162">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-162">inbound and outbound</span></span> |



 

<span data-ttu-id="55419-163">No Windows Vista, se a entrada do registro **AcceptedEULA** tiver um valor de 1, as portas a seguir deverão ser abertas.</span><span class="sxs-lookup"><span data-stu-id="55419-163">On Windows Vista, if the **AcceptedEULA** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="55419-164">Porta</span><span class="sxs-lookup"><span data-stu-id="55419-164">Port</span></span>          | <span data-ttu-id="55419-165">Protocolo</span><span class="sxs-lookup"><span data-stu-id="55419-165">Protocol</span></span>       | <span data-ttu-id="55419-166">Processar</span><span class="sxs-lookup"><span data-stu-id="55419-166">Process</span></span>                         | <span data-ttu-id="55419-167">Direção</span><span class="sxs-lookup"><span data-stu-id="55419-167">Direction</span></span>            |
|---------------|----------------|---------------------------------|----------------------|
| <span data-ttu-id="55419-168">Todas as portas UDP</span><span class="sxs-lookup"><span data-stu-id="55419-168">All UDP ports</span></span> | <span data-ttu-id="55419-169">UDP RTP, MSB</span><span class="sxs-lookup"><span data-stu-id="55419-169">UDP RTP, MSB</span></span>   | <span data-ttu-id="55419-170">wmplayer.exe, qualquer sub-rede</span><span class="sxs-lookup"><span data-stu-id="55419-170">wmplayer.exe, any subnet</span></span>        | <span data-ttu-id="55419-171">entrada</span><span class="sxs-lookup"><span data-stu-id="55419-171">inbound</span></span>              |
| <span data-ttu-id="55419-172">1900</span><span class="sxs-lookup"><span data-stu-id="55419-172">1900</span></span>          | <span data-ttu-id="55419-173">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="55419-173">UDP SSDP</span></span>       | <span data-ttu-id="55419-174">SSDPsrv/UPnPHost no svchost.exe</span><span class="sxs-lookup"><span data-stu-id="55419-174">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="55419-175">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-175">inbound and outbound</span></span> |
| <span data-ttu-id="55419-176">2869</span><span class="sxs-lookup"><span data-stu-id="55419-176">2869</span></span>          | <span data-ttu-id="55419-177">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="55419-177">TCP SSDP, UPnP</span></span> | <span data-ttu-id="55419-178">SSDPsrv, UPnPHost</span><span class="sxs-lookup"><span data-stu-id="55419-178">SSDPsrv, UPnPHost</span></span>               | <span data-ttu-id="55419-179">entrada</span><span class="sxs-lookup"><span data-stu-id="55419-179">inbound</span></span>              |



 

<span data-ttu-id="55419-180">No Microsoft Windows XP, se a entrada do registro **WMPNSSFirewallPortsOpen** tiver um valor de 1, as portas a seguir deverão ser abertas.</span><span class="sxs-lookup"><span data-stu-id="55419-180">On Microsoft Windows XP, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="55419-181">Porta</span><span class="sxs-lookup"><span data-stu-id="55419-181">Port</span></span>          | <span data-ttu-id="55419-182">Protocolo</span><span class="sxs-lookup"><span data-stu-id="55419-182">Protocol</span></span>                  | <span data-ttu-id="55419-183">Processar</span><span class="sxs-lookup"><span data-stu-id="55419-183">Process</span></span>                         | <span data-ttu-id="55419-184">Direção</span><span class="sxs-lookup"><span data-stu-id="55419-184">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="55419-185">1900</span><span class="sxs-lookup"><span data-stu-id="55419-185">1900</span></span>          | <span data-ttu-id="55419-186">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="55419-186">UDP SSDP</span></span>                  | <span data-ttu-id="55419-187">SSDPsrv em svchost.exe</span><span class="sxs-lookup"><span data-stu-id="55419-187">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="55419-188">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-188">inbound and outbound</span></span> |
| <span data-ttu-id="55419-189">2869</span><span class="sxs-lookup"><span data-stu-id="55419-189">2869</span></span>          | <span data-ttu-id="55419-190">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="55419-190">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="55419-191">SSDPsrv/UPnPHost no svchost.exe</span><span class="sxs-lookup"><span data-stu-id="55419-191">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="55419-192">entrada</span><span class="sxs-lookup"><span data-stu-id="55419-192">inbound</span></span>              |
| <span data-ttu-id="55419-193">10280-10284</span><span class="sxs-lookup"><span data-stu-id="55419-193">10280 - 10284</span></span> | <span data-ttu-id="55419-194">Registro de WMDRM-ND de UDP</span><span class="sxs-lookup"><span data-stu-id="55419-194">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="55419-195">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="55419-195">wmpnetwk.exe</span></span>                    | <span data-ttu-id="55419-196">entrada e saída</span><span class="sxs-lookup"><span data-stu-id="55419-196">inbound and outbound</span></span> |
| <span data-ttu-id="55419-197">10243</span><span class="sxs-lookup"><span data-stu-id="55419-197">10243</span></span>         | <span data-ttu-id="55419-198">HTTP TCP</span><span class="sxs-lookup"><span data-stu-id="55419-198">TCP HTTP</span></span>                  | <span data-ttu-id="55419-199">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="55419-199">wmpnetwk.exe</span></span>                    | <span data-ttu-id="55419-200">entrada</span><span class="sxs-lookup"><span data-stu-id="55419-200">inbound</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="55419-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55419-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55419-202">**Configurações do registro**</span><span class="sxs-lookup"><span data-stu-id="55419-202">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




