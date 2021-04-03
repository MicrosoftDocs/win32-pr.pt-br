---
title: Configurações de rede padrão
description: Configurações de rede padrão
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- SDK do Windows Media Format, configurações de rede padrão
- Formato de sistema avançado (ASF), configurações de rede padrão
- ASF (formato de sistemas avançados), configurações de rede padrão
- SDK do Windows Media Format, configurações de rede
- ASF (Advanced Systems Format), configurações de rede
- ASF (formato de sistemas avançados), configurações de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823022"
---
# <a name="default-networking-settings"></a><span data-ttu-id="12705-109">Configurações de rede padrão</span><span class="sxs-lookup"><span data-stu-id="12705-109">Default Networking Settings</span></span>

<span data-ttu-id="12705-110">As tabelas a seguir descrevem as configurações padrão dos parâmetros de rede no Windows Media Format SDK, agrupadas por interface.</span><span class="sxs-lookup"><span data-stu-id="12705-110">The following tables describe the default settings of the networking parameters in the Windows Media Format SDK, grouped by interface.</span></span>



| <span data-ttu-id="12705-111">IWMReaderNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="12705-111">IWMReaderNetworkConfig</span></span>                | <span data-ttu-id="12705-112">Configuração padrão</span><span class="sxs-lookup"><span data-stu-id="12705-112">Default setting</span></span>              |
|---------------------------------------|------------------------------|
| <span data-ttu-id="12705-113">Tempo de buffer</span><span class="sxs-lookup"><span data-stu-id="12705-113">Buffering time</span></span>                        | <span data-ttu-id="12705-114">5 segundos</span><span class="sxs-lookup"><span data-stu-id="12705-114">5 seconds</span></span>                    |
| <span data-ttu-id="12705-115">UseFixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="12705-115">UseFixedUDPPort</span></span>                       | <span data-ttu-id="12705-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="12705-116">FALSE</span></span>                        |
| <span data-ttu-id="12705-117">FixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="12705-117">FixedUDPPort</span></span>                          | <span data-ttu-id="12705-118">0 (não é válido)</span><span class="sxs-lookup"><span data-stu-id="12705-118">0 (not valid)</span></span>                |
| <span data-ttu-id="12705-119">ProxySetting: HTTP</span><span class="sxs-lookup"><span data-stu-id="12705-119">ProxySetting: HTTP</span></span>                    | <span data-ttu-id="12705-120">\_navegador de \_ configurações de proxy WMT \_</span><span class="sxs-lookup"><span data-stu-id="12705-120">WMT\_PROXY\_SETTING\_BROWSER</span></span> |
| <span data-ttu-id="12705-121">ProxySetting: MMS</span><span class="sxs-lookup"><span data-stu-id="12705-121">ProxySetting: MMS</span></span>                     | <span data-ttu-id="12705-122">\_configuração de proxy WMT \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="12705-122">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="12705-123">ProxySetting: RTSP</span><span class="sxs-lookup"><span data-stu-id="12705-123">ProxySetting: RTSP</span></span>                    | <span data-ttu-id="12705-124">\_configuração de proxy WMT \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="12705-124">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="12705-125">ProxyHostName (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="12705-125">ProxyHostName (HTTP, MMS, RTSP)</span></span>       | <span data-ttu-id="12705-126">""</span><span class="sxs-lookup"><span data-stu-id="12705-126">""</span></span>                           |
| <span data-ttu-id="12705-127">ProxyPort: HTTP</span><span class="sxs-lookup"><span data-stu-id="12705-127">ProxyPort: HTTP</span></span>                       | <span data-ttu-id="12705-128">80</span><span class="sxs-lookup"><span data-stu-id="12705-128">80</span></span>                           |
| <span data-ttu-id="12705-129">ProxyPort: MMS</span><span class="sxs-lookup"><span data-stu-id="12705-129">ProxyPort: MMS</span></span>                        | <span data-ttu-id="12705-130">1755</span><span class="sxs-lookup"><span data-stu-id="12705-130">1755</span></span>                         |
| <span data-ttu-id="12705-131">ProxtPort: RTSP</span><span class="sxs-lookup"><span data-stu-id="12705-131">ProxtPort: RTSP</span></span>                       | <span data-ttu-id="12705-132">554</span><span class="sxs-lookup"><span data-stu-id="12705-132">554</span></span>                          |
| <span data-ttu-id="12705-133">ProxyExceptionList (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="12705-133">ProxyExceptionList (HTTP, MMS, RTSP)</span></span>  | <span data-ttu-id="12705-134">""</span><span class="sxs-lookup"><span data-stu-id="12705-134">""</span></span>                           |
| <span data-ttu-id="12705-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="12705-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span></span> | <span data-ttu-id="12705-136">FALSE</span><span class="sxs-lookup"><span data-stu-id="12705-136">FALSE</span></span>                        |
| <span data-ttu-id="12705-137">ForceRerunAutoDetection</span><span class="sxs-lookup"><span data-stu-id="12705-137">ForceRerunAutoDetection</span></span>               | <span data-ttu-id="12705-138">FALSE</span><span class="sxs-lookup"><span data-stu-id="12705-138">FALSE</span></span>                        |
| <span data-ttu-id="12705-139">EnableMulticast</span><span class="sxs-lookup"><span data-stu-id="12705-139">EnableMulticast</span></span>                       | <span data-ttu-id="12705-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="12705-140">TRUE</span></span>                         |
| <span data-ttu-id="12705-141">EnableHTTP</span><span class="sxs-lookup"><span data-stu-id="12705-141">EnableHTTP</span></span>                            | <span data-ttu-id="12705-142">TRUE</span><span class="sxs-lookup"><span data-stu-id="12705-142">TRUE</span></span>                         |
| <span data-ttu-id="12705-143">EnableTCP</span><span class="sxs-lookup"><span data-stu-id="12705-143">EnableTCP</span></span>                             | <span data-ttu-id="12705-144">TRUE</span><span class="sxs-lookup"><span data-stu-id="12705-144">TRUE</span></span>                         |
| <span data-ttu-id="12705-145">EnableUDP</span><span class="sxs-lookup"><span data-stu-id="12705-145">EnableUDP</span></span>                             | <span data-ttu-id="12705-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="12705-146">TRUE</span></span>                         |
| <span data-ttu-id="12705-147">Largura de banda da conexão</span><span class="sxs-lookup"><span data-stu-id="12705-147">Connection Bandwidth</span></span>                  | <span data-ttu-id="12705-148">0 (detecção automática)</span><span class="sxs-lookup"><span data-stu-id="12705-148">0 (auto-detect)</span></span>              |



 



| <span data-ttu-id="12705-149">IWMReaderNetworkConfig2</span><span class="sxs-lookup"><span data-stu-id="12705-149">IWMReaderNetworkConfig2</span></span>        | <span data-ttu-id="12705-150">Configuração padrão</span><span class="sxs-lookup"><span data-stu-id="12705-150">Default setting</span></span>        |
|--------------------------------|------------------------|
| <span data-ttu-id="12705-151">Duração de streaming acelerada</span><span class="sxs-lookup"><span data-stu-id="12705-151">Accelerated streaming duration</span></span> | <span data-ttu-id="12705-152">100 milhões (10 segundos)</span><span class="sxs-lookup"><span data-stu-id="12705-152">100000000 (10 seconds)</span></span> |
| <span data-ttu-id="12705-153">Habilitar o Caching de conteúdo</span><span class="sxs-lookup"><span data-stu-id="12705-153">Enable content caching</span></span>         | <span data-ttu-id="12705-154">TRUE</span><span class="sxs-lookup"><span data-stu-id="12705-154">TRUE</span></span>                   |
| <span data-ttu-id="12705-155">Habilitar cache rápido</span><span class="sxs-lookup"><span data-stu-id="12705-155">Enable fast cache</span></span>              | <span data-ttu-id="12705-156">TRUE</span><span class="sxs-lookup"><span data-stu-id="12705-156">TRUE</span></span>                   |
| <span data-ttu-id="12705-157">Habilitar reenvios</span><span class="sxs-lookup"><span data-stu-id="12705-157">Enable resends</span></span>                 | <span data-ttu-id="12705-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="12705-158">TRUE</span></span>                   |
| <span data-ttu-id="12705-159">Habilitar o estreitamento de conteúdo</span><span class="sxs-lookup"><span data-stu-id="12705-159">Enable content thinning</span></span>        | <span data-ttu-id="12705-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="12705-160">TRUE</span></span>                   |
| <span data-ttu-id="12705-161">Limite de reconexão</span><span class="sxs-lookup"><span data-stu-id="12705-161">Reconnect limit</span></span>                | <span data-ttu-id="12705-162">25</span><span class="sxs-lookup"><span data-stu-id="12705-162">25</span></span>                     |



 



| <span data-ttu-id="12705-163">IWMWriterNetworkSink</span><span class="sxs-lookup"><span data-stu-id="12705-163">IWMWriterNetworkSink</span></span> | <span data-ttu-id="12705-164">Configuração padrão</span><span class="sxs-lookup"><span data-stu-id="12705-164">Default setting</span></span>         |
|----------------------|-------------------------|
| <span data-ttu-id="12705-165">Máximo de clientes</span><span class="sxs-lookup"><span data-stu-id="12705-165">Maximum clients</span></span>      | <span data-ttu-id="12705-166">5</span><span class="sxs-lookup"><span data-stu-id="12705-166">5</span></span>                       |
| <span data-ttu-id="12705-167">Protocolo de rede</span><span class="sxs-lookup"><span data-stu-id="12705-167">Network protocol</span></span>     | <span data-ttu-id="12705-168">0 ( \_ protocolo \_ http WMT)</span><span class="sxs-lookup"><span data-stu-id="12705-168">0 (WMT\_PROTOCOL\_HTTP)</span></span> |
| <span data-ttu-id="12705-169">URL do host</span><span class="sxs-lookup"><span data-stu-id="12705-169">Host URL</span></span>             | <span data-ttu-id="12705-170">0 (não é válido)</span><span class="sxs-lookup"><span data-stu-id="12705-170">0 (not valid)</span></span>           |



 



| <span data-ttu-id="12705-171">IWMWriterAdvanced2</span><span class="sxs-lookup"><span data-stu-id="12705-171">IWMWriterAdvanced2</span></span>  | <span data-ttu-id="12705-172">Configuração padrão</span><span class="sxs-lookup"><span data-stu-id="12705-172">Default setting</span></span>             |
|---------------------|-----------------------------|
| <span data-ttu-id="12705-173">Tamanho máximo do pacote</span><span class="sxs-lookup"><span data-stu-id="12705-173">Maximum packet size</span></span> | <span data-ttu-id="12705-174">1.400</span><span class="sxs-lookup"><span data-stu-id="12705-174">1400</span></span>                        |
| <span data-ttu-id="12705-175">ID do cliente de log</span><span class="sxs-lookup"><span data-stu-id="12705-175">Log client ID</span></span>       | <span data-ttu-id="12705-176">FALSE</span><span class="sxs-lookup"><span data-stu-id="12705-176">FALSE</span></span>                       |
| <span data-ttu-id="12705-177">Modo de reprodução</span><span class="sxs-lookup"><span data-stu-id="12705-177">Play mode</span></span>           | <span data-ttu-id="12705-178">SELEÇÃO asWMT de \_ modo de reprodução \_ \_</span><span class="sxs-lookup"><span data-stu-id="12705-178">WMT\_PLAY\_MODE\_AUTOSELECT</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="12705-179">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12705-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12705-180">**Implementando a funcionalidade de rede**</span><span class="sxs-lookup"><span data-stu-id="12705-180">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




