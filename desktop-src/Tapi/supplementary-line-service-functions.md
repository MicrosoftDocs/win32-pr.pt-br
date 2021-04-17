---
description: As funções de serviço de linha suplementar são listadas por categoria nos tópicos a seguir.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funções de serviço de linha suplementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782899"
---
# <a name="supplementary-line-service-functions"></a><span data-ttu-id="49228-103">Funções de serviço de linha suplementar</span><span class="sxs-lookup"><span data-stu-id="49228-103">Supplementary Line Service Functions</span></span>

<span data-ttu-id="49228-104">As funções de serviço de linha suplementar são listadas por categoria nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="49228-104">The supplementary line service functions are listed by category in the following topics.</span></span> <span data-ttu-id="49228-105">Uma função será identificada como [*assíncrona*](a-tapgloss.md) se ela indicar conclusão em uma mensagem de resposta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="49228-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="49228-106">Se a função sempre retornar seu resultado ao aplicativo imediatamente, a função será considerada [*síncrona*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="49228-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="49228-107">A seguir está um agrupamento funcional das funções de serviço de linha suplementar:</span><span class="sxs-lookup"><span data-stu-id="49228-107">Following is a functional grouping of the supplementary line service functions:</span></span>

-   [<span data-ttu-id="49228-108">Agentes</span><span class="sxs-lookup"><span data-stu-id="49228-108">Agents</span></span>](#agents)
-   [<span data-ttu-id="49228-109">Prioridade do aplicativo</span><span class="sxs-lookup"><span data-stu-id="49228-109">Application priority</span></span>](#application-priority)
-   [<span data-ttu-id="49228-110">Modo e taxa de portador</span><span class="sxs-lookup"><span data-stu-id="49228-110">Bearer mode and rate</span></span>](#bearer-mode-and-rate)
-   [<span data-ttu-id="49228-111">Aceitar e redirecionar chamada</span><span class="sxs-lookup"><span data-stu-id="49228-111">Call accept and redirect</span></span>](#call-accept-and-redirect)
-   [<span data-ttu-id="49228-112">Conclusão da chamada</span><span class="sxs-lookup"><span data-stu-id="49228-112">Call completion</span></span>](#call-completion)
-   [<span data-ttu-id="49228-113">Conferência de chamada</span><span class="sxs-lookup"><span data-stu-id="49228-113">Call conference</span></span>](#call-conference)
-   [<span data-ttu-id="49228-114">Encaminhamento de chamadas</span><span class="sxs-lookup"><span data-stu-id="49228-114">Call forwarding</span></span>](#call-forwarding)
-   [<span data-ttu-id="49228-115">Espera de chamada</span><span class="sxs-lookup"><span data-stu-id="49228-115">Call hold</span></span>](#call-hold)
-   [<span data-ttu-id="49228-116">Entre em contato com o parque</span><span class="sxs-lookup"><span data-stu-id="49228-116">Call park</span></span>](#call-park)
-   [<span data-ttu-id="49228-117">Chamar retirada</span><span class="sxs-lookup"><span data-stu-id="49228-117">Call pickup</span></span>](#call-pickup)
-   [<span data-ttu-id="49228-118">Rejeitar chamada</span><span class="sxs-lookup"><span data-stu-id="49228-118">Call reject</span></span>](#call-reject)
-   [<span data-ttu-id="49228-119">Transferência de chamada</span><span class="sxs-lookup"><span data-stu-id="49228-119">Call transfer</span></span>](#call-transfer)
-   [<span data-ttu-id="49228-120">Monitoramento e coleta de dígitos</span><span class="sxs-lookup"><span data-stu-id="49228-120">Digit monitoring and gathering</span></span>](#digit-monitoring-and-gathering)
-   [<span data-ttu-id="49228-121">Gerando dígitos de banda e tons</span><span class="sxs-lookup"><span data-stu-id="49228-121">Generating inband digits and tones</span></span>](#generating-inband-digits-and-tones)
-   [<span data-ttu-id="49228-122">Fazendo chamadas</span><span class="sxs-lookup"><span data-stu-id="49228-122">Making calls</span></span>](basic-telephony-services-reference.md)
-   [<span data-ttu-id="49228-123">Controle de mídia</span><span class="sxs-lookup"><span data-stu-id="49228-123">Media control</span></span>](#media-control)
-   [<span data-ttu-id="49228-124">Monitoramento de mídia</span><span class="sxs-lookup"><span data-stu-id="49228-124">Media monitoring</span></span>](#media-monitoring)
-   [<span data-ttu-id="49228-125">Proxies</span><span class="sxs-lookup"><span data-stu-id="49228-125">Proxies</span></span>](#proxies)
-   [<span data-ttu-id="49228-126">Qualidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="49228-126">Quality of Service</span></span>](#quality-of-service)
-   [<span data-ttu-id="49228-127">Enviando informações para a parte remota</span><span class="sxs-lookup"><span data-stu-id="49228-127">Sending information to remote party</span></span>](#sending-information-to-remote-party)
-   [<span data-ttu-id="49228-128">Gerenciamento do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="49228-128">Service provider management</span></span>](#service-provider-management)
-   [<span data-ttu-id="49228-129">Configurando um terminal para conversas por telefone</span><span class="sxs-lookup"><span data-stu-id="49228-129">Setting a terminal for phone conversations</span></span>](#setting-a-terminal-for-phone-conversations)
-   [<span data-ttu-id="49228-130">Monitoramento de Tom</span><span class="sxs-lookup"><span data-stu-id="49228-130">Tone monitoring</span></span>](#tone-monitoring)

<span data-ttu-id="49228-131">Há também funções de serviço de linha suplementar [diversas](#miscellaneous) .</span><span class="sxs-lookup"><span data-stu-id="49228-131">There are also [miscellaneous](#miscellaneous) supplementary line service functions.</span></span>

## <a name="bearer-mode-and-rate"></a><span data-ttu-id="49228-132">Modo e taxa de portador</span><span class="sxs-lookup"><span data-stu-id="49228-132">Bearer Mode and Rate</span></span>



| <span data-ttu-id="49228-133">Função</span><span class="sxs-lookup"><span data-stu-id="49228-133">Function</span></span>                                       | <span data-ttu-id="49228-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-134">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="49228-135">**lineSetCallParams**</span><span class="sxs-lookup"><span data-stu-id="49228-135">**lineSetCallParams**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | <span data-ttu-id="49228-136">Solicita uma alteração nos parâmetros de chamada de uma chamada existente.</span><span class="sxs-lookup"><span data-stu-id="49228-136">Requests a change in the call parameters of an existing call.</span></span> <span data-ttu-id="49228-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-137">Synchronous.</span></span> |



 

## <a name="media-monitoring"></a><span data-ttu-id="49228-138">Monitoramento de mídia</span><span class="sxs-lookup"><span data-stu-id="49228-138">Media Monitoring</span></span>



| <span data-ttu-id="49228-139">Função</span><span class="sxs-lookup"><span data-stu-id="49228-139">Function</span></span>                                     | <span data-ttu-id="49228-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-140">Description</span></span>                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-141">**lineMonitorMedia**</span><span class="sxs-lookup"><span data-stu-id="49228-141">**lineMonitorMedia**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | <span data-ttu-id="49228-142">Habilita ou desabilita a notificação do modo de mídia em uma chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="49228-142">Enables or disables media mode notification on a specified call.</span></span> <span data-ttu-id="49228-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-143">Synchronous.</span></span> |



 

## <a name="digit-monitoring-and-gathering"></a><span data-ttu-id="49228-144">Monitoramento e coleta de dígitos</span><span class="sxs-lookup"><span data-stu-id="49228-144">Digit Monitoring and Gathering</span></span>



| <span data-ttu-id="49228-145">Função</span><span class="sxs-lookup"><span data-stu-id="49228-145">Function</span></span>                                       | <span data-ttu-id="49228-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-146">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-147">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="49228-147">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | <span data-ttu-id="49228-148">Habilita ou desabilita a notificação de detecção de dígitos em uma chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="49228-148">Enables or disables digit detection notification on a specified call.</span></span> <span data-ttu-id="49228-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-149">Synchronous.</span></span> |
| [<span data-ttu-id="49228-150">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="49228-150">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | <span data-ttu-id="49228-151">Executa a coleta de dígitos em buffer em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="49228-151">Performs the buffered gathering of digits on a call.</span></span> <span data-ttu-id="49228-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-152">Synchronous.</span></span>                  |



 

## <a name="tone-monitoring"></a><span data-ttu-id="49228-153">Monitoramento de Tom</span><span class="sxs-lookup"><span data-stu-id="49228-153">Tone Monitoring</span></span>



| <span data-ttu-id="49228-154">Função</span><span class="sxs-lookup"><span data-stu-id="49228-154">Function</span></span>                                     | <span data-ttu-id="49228-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-155">Description</span></span>                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="49228-156">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="49228-156">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | <span data-ttu-id="49228-157">Especifica quais tons detectar em uma chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="49228-157">Specifies which tones to detect on a specified call.</span></span> <span data-ttu-id="49228-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-158">Synchronous.</span></span> |



 

## <a name="media-control"></a><span data-ttu-id="49228-159">Controle de mídia</span><span class="sxs-lookup"><span data-stu-id="49228-159">Media Control</span></span>



| <span data-ttu-id="49228-160">Função</span><span class="sxs-lookup"><span data-stu-id="49228-160">Function</span></span>                                           | <span data-ttu-id="49228-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-161">Description</span></span>                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-162">**lineSetMediaControl**</span><span class="sxs-lookup"><span data-stu-id="49228-162">**lineSetMediaControl**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | <span data-ttu-id="49228-163">Configura o fluxo de mídia de uma chamada para o controle de mídia.</span><span class="sxs-lookup"><span data-stu-id="49228-163">Sets up a call's media stream for media control.</span></span> <span data-ttu-id="49228-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-164">Synchronous.</span></span>                                                        |
| [<span data-ttu-id="49228-165">**lineSetMediaMode**</span><span class="sxs-lookup"><span data-stu-id="49228-165">**lineSetMediaMode**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | <span data-ttu-id="49228-166">Define os modos de mídia da chamada especificada em sua estrutura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="49228-166">Sets the media mode(s) of the specified call in its [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="49228-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-167">Synchronous.</span></span> |



 

## <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="49228-168">Gerando dígitos de banda e tons</span><span class="sxs-lookup"><span data-stu-id="49228-168">Generating Inband Digits and Tones</span></span>



| <span data-ttu-id="49228-169">Função</span><span class="sxs-lookup"><span data-stu-id="49228-169">Function</span></span>                                         | <span data-ttu-id="49228-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-170">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="49228-171">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="49228-171">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | <span data-ttu-id="49228-172">Gera dígitos de inband em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="49228-172">Generates inband digits on a call.</span></span> <span data-ttu-id="49228-173">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-173">Synchronous.</span></span>               |
| [<span data-ttu-id="49228-174">**lineGenerateTone**</span><span class="sxs-lookup"><span data-stu-id="49228-174">**lineGenerateTone**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | <span data-ttu-id="49228-175">Gera um determinado conjunto de tons de faixas em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="49228-175">Generates a given set of tones inband on a call.</span></span> <span data-ttu-id="49228-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-176">Synchronous.</span></span> |



 

## <a name="call-accept-and-redirect"></a><span data-ttu-id="49228-177">Aceitar e redirecionar chamada</span><span class="sxs-lookup"><span data-stu-id="49228-177">Call Accept and Redirect</span></span>



| <span data-ttu-id="49228-178">Função</span><span class="sxs-lookup"><span data-stu-id="49228-178">Function</span></span>                             | <span data-ttu-id="49228-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-179">Description</span></span>                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-180">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="49228-180">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | <span data-ttu-id="49228-181">Aceita uma chamada oferecida e começa a emitir um alerta tanto para o chamador (em um toque) quanto para a parte chamada (anel).</span><span class="sxs-lookup"><span data-stu-id="49228-181">Accepts an offered call and starts alerting both caller (ringback) and called party (ring).</span></span> <span data-ttu-id="49228-182">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-182">Asynchronous.</span></span> |
| [<span data-ttu-id="49228-183">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="49228-183">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | <span data-ttu-id="49228-184">Redireciona uma chamada de oferta para outro endereço.</span><span class="sxs-lookup"><span data-stu-id="49228-184">Redirects an offering call to another address.</span></span> <span data-ttu-id="49228-185">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-185">Asynchronous.</span></span>                                              |



 

## <a name="call-reject"></a><span data-ttu-id="49228-186">Rejeitar chamada</span><span class="sxs-lookup"><span data-stu-id="49228-186">Call Reject</span></span>



| <span data-ttu-id="49228-187">Função</span><span class="sxs-lookup"><span data-stu-id="49228-187">Function</span></span>                     | <span data-ttu-id="49228-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-188">Description</span></span>                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="49228-189">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="49228-189">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop) | <span data-ttu-id="49228-190">Desconecta uma chamada ou abandona uma tentativa de chamada em andamento.</span><span class="sxs-lookup"><span data-stu-id="49228-190">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="49228-191">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-191">Asynchronous.</span></span> |



 

## <a name="call-hold"></a><span data-ttu-id="49228-192">Espera de chamada</span><span class="sxs-lookup"><span data-stu-id="49228-192">Call Hold</span></span>



| <span data-ttu-id="49228-193">Função</span><span class="sxs-lookup"><span data-stu-id="49228-193">Function</span></span>                         | <span data-ttu-id="49228-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-194">Description</span></span>                                           |
|----------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="49228-195">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="49228-195">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)     | <span data-ttu-id="49228-196">Coloca a chamada especificada em retenção rígida.</span><span class="sxs-lookup"><span data-stu-id="49228-196">Places the specified call on hard hold.</span></span> <span data-ttu-id="49228-197">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-197">Asynchronous.</span></span> |
| [<span data-ttu-id="49228-198">**lineUnhold**</span><span class="sxs-lookup"><span data-stu-id="49228-198">**lineUnhold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | <span data-ttu-id="49228-199">Recupera uma chamada mantida.</span><span class="sxs-lookup"><span data-stu-id="49228-199">Retrieves a held call.</span></span> <span data-ttu-id="49228-200">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-200">Asynchronous.</span></span>                  |



 

## <a name="securing-calls"></a><span data-ttu-id="49228-201">Protegendo chamadas</span><span class="sxs-lookup"><span data-stu-id="49228-201">Securing Calls</span></span>



| <span data-ttu-id="49228-202">Função</span><span class="sxs-lookup"><span data-stu-id="49228-202">Function</span></span>                                 | <span data-ttu-id="49228-203">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-203">Description</span></span>                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-204">**lineSecureCall**</span><span class="sxs-lookup"><span data-stu-id="49228-204">**lineSecureCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | <span data-ttu-id="49228-205">Protege uma chamada existente da interferência por outros eventos, como alarmes de espera de chamada em conexões de dados.</span><span class="sxs-lookup"><span data-stu-id="49228-205">Secures an existing call from interference by other events such as call-waiting beeps on data connections.</span></span> <span data-ttu-id="49228-206">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-206">Asynchronous.</span></span> |



 

## <a name="call-transfer"></a><span data-ttu-id="49228-207">Transferência de chamada</span><span class="sxs-lookup"><span data-stu-id="49228-207">Call Transfer</span></span>



| <span data-ttu-id="49228-208">Função</span><span class="sxs-lookup"><span data-stu-id="49228-208">Function</span></span>                                             | <span data-ttu-id="49228-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-209">Description</span></span>                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-210">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="49228-210">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | <span data-ttu-id="49228-211">Prepara uma chamada especificada para transferência para outro endereço.</span><span class="sxs-lookup"><span data-stu-id="49228-211">Prepares a specified call for transfer to another address.</span></span> <span data-ttu-id="49228-212">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-212">Asynchronous.</span></span>                                       |
| [<span data-ttu-id="49228-213">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="49228-213">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | <span data-ttu-id="49228-214">Transfere uma chamada que foi configurada para transferência para outra chamada ou que entra em uma conferência de três vias.</span><span class="sxs-lookup"><span data-stu-id="49228-214">Transfers a call that was set up for transfer to another call, or enters a three-way conference.</span></span> <span data-ttu-id="49228-215">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-215">Asynchronous.</span></span> |
| [<span data-ttu-id="49228-216">**lineBlindTransfer**</span><span class="sxs-lookup"><span data-stu-id="49228-216">**lineBlindTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | <span data-ttu-id="49228-217">Transfere uma chamada para outra entidade.</span><span class="sxs-lookup"><span data-stu-id="49228-217">Transfers a call to another party.</span></span> <span data-ttu-id="49228-218">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-218">Asynchronous.</span></span>                                                               |
| [<span data-ttu-id="49228-219">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="49228-219">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | <span data-ttu-id="49228-220">Troca a chamada ativa pela chamada atualmente em retenção de consulta.</span><span class="sxs-lookup"><span data-stu-id="49228-220">Swaps the active call with the call currently on consultation hold.</span></span> <span data-ttu-id="49228-221">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-221">Asynchronous.</span></span>                              |



 

## <a name="call-conference"></a><span data-ttu-id="49228-222">Conferência de chamada</span><span class="sxs-lookup"><span data-stu-id="49228-222">Call Conference</span></span>



| <span data-ttu-id="49228-223">Função</span><span class="sxs-lookup"><span data-stu-id="49228-223">Function</span></span>                                                         | <span data-ttu-id="49228-224">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-224">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-225">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="49228-225">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | <span data-ttu-id="49228-226">Prepara uma determinada chamada para a adição de outra parte.</span><span class="sxs-lookup"><span data-stu-id="49228-226">Prepares a given call for the addition of another party.</span></span> <span data-ttu-id="49228-227">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-227">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="49228-228">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="49228-228">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | <span data-ttu-id="49228-229">Prepara para adicionar uma entidade a uma chamada de conferência existente colocando a chamada de conferência em estado de espera e criando uma chamada de consulta que pode ser adicionada posteriormente à chamada de conferência.</span><span class="sxs-lookup"><span data-stu-id="49228-229">Prepares to add a party to an existing conference call by placing the conference call in a hold state and creating a consultation call that can be added later to the conference call.</span></span> <span data-ttu-id="49228-230">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-230">Asynchronous.</span></span> |
| [<span data-ttu-id="49228-231">**lineAddToConference**</span><span class="sxs-lookup"><span data-stu-id="49228-231">**lineAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | <span data-ttu-id="49228-232">Adiciona uma chamada de consulta a uma chamada de conferência existente.</span><span class="sxs-lookup"><span data-stu-id="49228-232">Adds a consultation call to an existing conference call.</span></span> <span data-ttu-id="49228-233">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-233">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="49228-234">**lineRemoveFromConference**</span><span class="sxs-lookup"><span data-stu-id="49228-234">**lineRemoveFromConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | <span data-ttu-id="49228-235">Remove uma entidade de uma chamada de conferência.</span><span class="sxs-lookup"><span data-stu-id="49228-235">Removes a party from a conference call.</span></span> <span data-ttu-id="49228-236">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-236">Asynchronous.</span></span>                                                                                                                                                |



 

## <a name="call-park"></a><span data-ttu-id="49228-237">Entre em contato com o parque</span><span class="sxs-lookup"><span data-stu-id="49228-237">Call Park</span></span>



| <span data-ttu-id="49228-238">Função</span><span class="sxs-lookup"><span data-stu-id="49228-238">Function</span></span>                         | <span data-ttu-id="49228-239">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-239">Description</span></span>                                          |
|----------------------------------|------------------------------------------------------|
| [<span data-ttu-id="49228-240">**linePark**</span><span class="sxs-lookup"><span data-stu-id="49228-240">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)     | <span data-ttu-id="49228-241">Parques de uma determinada chamada em outro endereço.</span><span class="sxs-lookup"><span data-stu-id="49228-241">Parks a given call at another address.</span></span> <span data-ttu-id="49228-242">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-242">Asynchronous.</span></span> |
| [<span data-ttu-id="49228-243">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="49228-243">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | <span data-ttu-id="49228-244">Recupera uma chamada estacionada.</span><span class="sxs-lookup"><span data-stu-id="49228-244">Retrieves a parked call.</span></span> <span data-ttu-id="49228-245">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-245">Asynchronous.</span></span>               |



 

## <a name="call-forwarding"></a><span data-ttu-id="49228-246">Encaminhamento de chamadas</span><span class="sxs-lookup"><span data-stu-id="49228-246">Call Forwarding</span></span>



| <span data-ttu-id="49228-247">Função</span><span class="sxs-lookup"><span data-stu-id="49228-247">Function</span></span>                           | <span data-ttu-id="49228-248">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-248">Description</span></span>                                             |
|------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="49228-249">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="49228-249">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward) | <span data-ttu-id="49228-250">Define ou cancela solicitações de encaminhamento de chamada.</span><span class="sxs-lookup"><span data-stu-id="49228-250">Sets or cancels call forwarding requests.</span></span> <span data-ttu-id="49228-251">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-251">Asynchronous.</span></span> |



 

## <a name="call-pickup"></a><span data-ttu-id="49228-252">Chamar retirada</span><span class="sxs-lookup"><span data-stu-id="49228-252">Call Pickup</span></span>



| <span data-ttu-id="49228-253">Função</span><span class="sxs-lookup"><span data-stu-id="49228-253">Function</span></span>                         | <span data-ttu-id="49228-254">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-254">Description</span></span>                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-255">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="49228-255">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup) | <span data-ttu-id="49228-256">Pega um alerta de chamada em um endereço de destino especificado e retorna um identificador de chamada para a chamada de retirada ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) também pode ser usado para espera de chamada).</span><span class="sxs-lookup"><span data-stu-id="49228-256">Picks up a call alerting at a specified destination address and returns a call handle for the picked-up call ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can also be used for call waiting).</span></span> <span data-ttu-id="49228-257">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-257">Asynchronous.</span></span> |



 

## <a name="sending-information-to-remote-party"></a><span data-ttu-id="49228-258">Enviando informações para a parte remota</span><span class="sxs-lookup"><span data-stu-id="49228-258">Sending Information to Remote Party</span></span>



| <span data-ttu-id="49228-259">Função</span><span class="sxs-lookup"><span data-stu-id="49228-259">Function</span></span>                                                   | <span data-ttu-id="49228-260">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-260">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-261">**lineReleaseUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="49228-261">**lineReleaseUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | <span data-ttu-id="49228-262">Libera informações do usuário usuário, permitindo que o sistema Substitua esse armazenamento por novas informações.</span><span class="sxs-lookup"><span data-stu-id="49228-262">Releases user-user information, permitting the system to overwrite this storage with new information.</span></span> <span data-ttu-id="49228-263">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-263">Asynchronous.</span></span> |
| [<span data-ttu-id="49228-264">**lineSendUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="49228-264">**lineSendUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | <span data-ttu-id="49228-265">Envia informações do usuário ao usuário para a parte remota na chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="49228-265">Sends user-user information to the remote party on the specified call.</span></span> <span data-ttu-id="49228-266">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-266">Asynchronous.</span></span>                                |



 

## <a name="call-completion"></a><span data-ttu-id="49228-267">Conclusão da chamada</span><span class="sxs-lookup"><span data-stu-id="49228-267">Call Completion</span></span>



| <span data-ttu-id="49228-268">Função</span><span class="sxs-lookup"><span data-stu-id="49228-268">Function</span></span>                                         | <span data-ttu-id="49228-269">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-269">Description</span></span>                                      |
|--------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="49228-270">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="49228-270">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | <span data-ttu-id="49228-271">Coloca uma solicitação de conclusão de chamada.</span><span class="sxs-lookup"><span data-stu-id="49228-271">Places a call completion request.</span></span> <span data-ttu-id="49228-272">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-272">Asynchronous.</span></span>  |
| [<span data-ttu-id="49228-273">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="49228-273">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | <span data-ttu-id="49228-274">Cancela uma solicitação de conclusão de chamada.</span><span class="sxs-lookup"><span data-stu-id="49228-274">Cancels a call completion request.</span></span> <span data-ttu-id="49228-275">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-275">Asynchronous.</span></span> |



 

## <a name="setting-a-terminal-for-phone-conversations"></a><span data-ttu-id="49228-276">Configurando um terminal para conversas por telefone</span><span class="sxs-lookup"><span data-stu-id="49228-276">Setting a Terminal for Phone Conversations</span></span>



| <span data-ttu-id="49228-277">Função</span><span class="sxs-lookup"><span data-stu-id="49228-277">Function</span></span>                                   | <span data-ttu-id="49228-278">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-278">Description</span></span>                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-279">**lineSetTerminal**</span><span class="sxs-lookup"><span data-stu-id="49228-279">**lineSetTerminal**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | <span data-ttu-id="49228-280">Especifica o dispositivo de terminal para o qual a linha especificada, os eventos de endereço ou os eventos de fluxo de mídia de chamada são roteados.</span><span class="sxs-lookup"><span data-stu-id="49228-280">Specifies the terminal device to which the specified line, address events, or call media stream events are routed.</span></span> <span data-ttu-id="49228-281">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-281">Asynchronous.</span></span> |



 

## <a name="application-priority"></a><span data-ttu-id="49228-282">Prioridade do aplicativo</span><span class="sxs-lookup"><span data-stu-id="49228-282">Application Priority</span></span>



| <span data-ttu-id="49228-283">Função</span><span class="sxs-lookup"><span data-stu-id="49228-283">Function</span></span>                                         | <span data-ttu-id="49228-284">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-284">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-285">**lineGetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="49228-285">**lineGetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | <span data-ttu-id="49228-286">Recupera informações de prioridade de telefonia assistida e/ou de entrega para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="49228-286">Retrieves handoff and/or Assisted Telephony priority information for an application.</span></span> <span data-ttu-id="49228-287">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-287">Synchronous.</span></span> |
| [<span data-ttu-id="49228-288">**lineSetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="49228-288">**lineSetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | <span data-ttu-id="49228-289">Define a prioridade de telefonia de entrega e/ou assistida para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="49228-289">Sets the handoff and/or Assisted Telephony priority for an application.</span></span> <span data-ttu-id="49228-290">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-290">Synchronous.</span></span>              |



 

## <a name="service-provider-management"></a><span data-ttu-id="49228-291">Gerenciamento do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="49228-291">Service Provider Management</span></span>



| <span data-ttu-id="49228-292">Função</span><span class="sxs-lookup"><span data-stu-id="49228-292">Function</span></span>                                           | <span data-ttu-id="49228-293">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-293">Description</span></span>                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="49228-294">**lineAddProvider**</span><span class="sxs-lookup"><span data-stu-id="49228-294">**lineAddProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | <span data-ttu-id="49228-295">Instala um provedor de serviços de telefonia.</span><span class="sxs-lookup"><span data-stu-id="49228-295">Installs a telephony service provider.</span></span> <span data-ttu-id="49228-296">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-296">Synchronous.</span></span>                   |
| [<span data-ttu-id="49228-297">**lineConfigProvider**</span><span class="sxs-lookup"><span data-stu-id="49228-297">**lineConfigProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | <span data-ttu-id="49228-298">Exibe a caixa de diálogo de configuração de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="49228-298">Displays configuration dialog box of a service provider.</span></span> <span data-ttu-id="49228-299">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-299">Synchronous.</span></span> |
| [<span data-ttu-id="49228-300">**lineRemoveProvider**</span><span class="sxs-lookup"><span data-stu-id="49228-300">**lineRemoveProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | <span data-ttu-id="49228-301">Remove um provedor de serviços de telefonia existente.</span><span class="sxs-lookup"><span data-stu-id="49228-301">Removes an existing telephony service provider.</span></span> <span data-ttu-id="49228-302">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-302">Synchronous.</span></span>          |
| [<span data-ttu-id="49228-303">**lineGetProviderList**</span><span class="sxs-lookup"><span data-stu-id="49228-303">**lineGetProviderList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | <span data-ttu-id="49228-304">Recupera uma lista de provedores de serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="49228-304">Retrieves a list of installed service providers.</span></span> <span data-ttu-id="49228-305">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-305">Synchronous.</span></span>         |



 

## <a name="agents"></a><span data-ttu-id="49228-306">Agentes</span><span class="sxs-lookup"><span data-stu-id="49228-306">Agents</span></span>



| <span data-ttu-id="49228-307">Função</span><span class="sxs-lookup"><span data-stu-id="49228-307">Function</span></span>                                                     | <span data-ttu-id="49228-308">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-308">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-309">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="49228-309">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | <span data-ttu-id="49228-310">Permite que o aplicativo acesse funções específicas do manipulador proprietário do manipulador do agente associado ao endereço.</span><span class="sxs-lookup"><span data-stu-id="49228-310">Allows the application to access proprietary handler-specific functions of the agent handler associated with the address.</span></span> <span data-ttu-id="49228-311">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-311">Asynchronous.</span></span> |
| [<span data-ttu-id="49228-312">**lineGetAgentActivityList**</span><span class="sxs-lookup"><span data-stu-id="49228-312">**lineGetAgentActivityList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | <span data-ttu-id="49228-313">Obtém a lista de atividades da qual um aplicativo seleciona as funções que um agente está executando.</span><span class="sxs-lookup"><span data-stu-id="49228-313">Obtains the list of activities from which an application selects the functions an agent is performing.</span></span> <span data-ttu-id="49228-314">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-314">Asynchronous.</span></span>                    |
| [<span data-ttu-id="49228-315">**lineGetAgentCaps**</span><span class="sxs-lookup"><span data-stu-id="49228-315">**lineGetAgentCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | <span data-ttu-id="49228-316">Obtém os recursos relacionados ao agente com suporte no dispositivo de linha especificado.</span><span class="sxs-lookup"><span data-stu-id="49228-316">Obtains the agent-related capabilities supported on the specified line device.</span></span> <span data-ttu-id="49228-317">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-317">Asynchronous.</span></span>                                            |
| [<span data-ttu-id="49228-318">**lineGetAgentGroupList**</span><span class="sxs-lookup"><span data-stu-id="49228-318">**lineGetAgentGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | <span data-ttu-id="49228-319">Obtém a lista de grupos de agentes nos quais um agente pode fazer logon no distribuidor de chamada automática.</span><span class="sxs-lookup"><span data-stu-id="49228-319">Obtains the list of agent groups into which an agent can log into on the automatic call distributor.</span></span> <span data-ttu-id="49228-320">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-320">Asynchronous.</span></span>                      |
| [<span data-ttu-id="49228-321">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="49228-321">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | <span data-ttu-id="49228-322">Obtém o status relacionado ao agente no endereço especificado.</span><span class="sxs-lookup"><span data-stu-id="49228-322">Obtains the agent-related status on the specified address.</span></span> <span data-ttu-id="49228-323">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-323">Asynchronous.</span></span>                                                                |
| [<span data-ttu-id="49228-324">**lineSetAgentActivity**</span><span class="sxs-lookup"><span data-stu-id="49228-324">**lineSetAgentActivity**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | <span data-ttu-id="49228-325">Define o código de atividade do agente associado a um endereço específico.</span><span class="sxs-lookup"><span data-stu-id="49228-325">Sets the agent activity code associated with a particular address.</span></span> <span data-ttu-id="49228-326">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-326">Asynchronous.</span></span>                                                        |
| [<span data-ttu-id="49228-327">**lineSetAgentGroup**</span><span class="sxs-lookup"><span data-stu-id="49228-327">**lineSetAgentGroup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | <span data-ttu-id="49228-328">Define os grupos de agentes nos quais o agente está conectado em um endereço específico.</span><span class="sxs-lookup"><span data-stu-id="49228-328">Sets the agent groups that the agent is logged into on a particular address.</span></span> <span data-ttu-id="49228-329">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-329">Asynchronous.</span></span>                                              |
| [<span data-ttu-id="49228-330">**lineSetAgentState**</span><span class="sxs-lookup"><span data-stu-id="49228-330">**lineSetAgentState**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | <span data-ttu-id="49228-331">Define o estado do agente associado a um endereço específico.</span><span class="sxs-lookup"><span data-stu-id="49228-331">Sets the agent state associated with a particular address.</span></span> <span data-ttu-id="49228-332">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-332">Asynchronous.</span></span>                                                                |



 

## <a name="proxies"></a><span data-ttu-id="49228-333">Proxies</span><span class="sxs-lookup"><span data-stu-id="49228-333">Proxies</span></span>



| <span data-ttu-id="49228-334">Função</span><span class="sxs-lookup"><span data-stu-id="49228-334">Function</span></span>                                       | <span data-ttu-id="49228-335">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-335">Description</span></span>                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-336">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="49228-336">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | <span data-ttu-id="49228-337">Usado por um manipulador de solicitação proxy registrado para gerar mensagens TAPI.</span><span class="sxs-lookup"><span data-stu-id="49228-337">Used by a registered proxy request handler to generate TAPI messages.</span></span> <span data-ttu-id="49228-338">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-338">Synchronous.</span></span>  |
| [<span data-ttu-id="49228-339">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="49228-339">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | <span data-ttu-id="49228-340">Indica a conclusão de uma solicitação de proxy por um manipulador de proxy registrado.</span><span class="sxs-lookup"><span data-stu-id="49228-340">Indicates completion of a proxy request by a registered proxy handler.</span></span> <span data-ttu-id="49228-341">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="49228-341">Synchronous.</span></span> |



 

## <a name="quality-of-service"></a><span data-ttu-id="49228-342">Qualidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="49228-342">Quality of Service</span></span>



| <span data-ttu-id="49228-343">Função</span><span class="sxs-lookup"><span data-stu-id="49228-343">Function</span></span>                                                           | <span data-ttu-id="49228-344">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-344">Description</span></span>                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-345">**lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="49228-345">**lineSetCallQualityOfService**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | <span data-ttu-id="49228-346">Solicita uma alteração da qualidade dos parâmetros de serviço para uma chamada existente.</span><span class="sxs-lookup"><span data-stu-id="49228-346">Requests a change of the quality of service parameters for an existing call.</span></span> <span data-ttu-id="49228-347">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-347">Asynchronous.</span></span> |



 

## <a name="miscellaneous"></a><span data-ttu-id="49228-348">Diversos</span><span class="sxs-lookup"><span data-stu-id="49228-348">Miscellaneous</span></span>



| <span data-ttu-id="49228-349">Função</span><span class="sxs-lookup"><span data-stu-id="49228-349">Function</span></span>                                             | <span data-ttu-id="49228-350">Descrição</span><span class="sxs-lookup"><span data-stu-id="49228-350">Description</span></span>                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49228-351">**lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="49228-351">**lineSetCallData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | <span data-ttu-id="49228-352">Define o membro **calldata** da estrutura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="49228-352">Sets the **CallData** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="49228-353">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-353">Asynchronous.</span></span> |
| [<span data-ttu-id="49228-354">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="49228-354">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | <span data-ttu-id="49228-355">Define os sons que o usuário ouve quando uma chamada não é respondida ou está em espera.</span><span class="sxs-lookup"><span data-stu-id="49228-355">Sets the sounds that the user hears when a call is unanswered or on hold.</span></span> <span data-ttu-id="49228-356">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-356">Asynchronous.</span></span>               |
| [<span data-ttu-id="49228-357">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="49228-357">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | <span data-ttu-id="49228-358">Define o status do dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="49228-358">Sets the line device status.</span></span> <span data-ttu-id="49228-359">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49228-359">Asynchronous.</span></span>                                                            |



 

 

 



