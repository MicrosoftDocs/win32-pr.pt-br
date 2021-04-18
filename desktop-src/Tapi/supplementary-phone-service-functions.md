---
description: As funções de serviço de telefone suplementar são listadas por categoria nos tópicos a seguir.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Funções de serviço de telefone suplementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757199"
---
# <a name="supplementary-phone-service-functions"></a><span data-ttu-id="54673-103">Funções de serviço de telefone suplementar</span><span class="sxs-lookup"><span data-stu-id="54673-103">Supplementary Phone Service Functions</span></span>

<span data-ttu-id="54673-104">As funções de serviço de telefone suplementar são listadas por categoria nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="54673-104">The supplementary phone service functions are listed by category in the following topics.</span></span> <span data-ttu-id="54673-105">Uma função será identificada como [*assíncrona*](a-tapgloss.md) se ela indicar conclusão em uma mensagem de resposta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54673-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="54673-106">Se a função sempre retornar seu resultado ao aplicativo imediatamente, a função será considerada [*síncrona*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="54673-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="54673-107">A seguir está um agrupamento funcional das funções de serviço de telefone suplementar:</span><span class="sxs-lookup"><span data-stu-id="54673-107">Following is a functional grouping of the supplementary phone service functions:</span></span>

-   [<span data-ttu-id="54673-108">Botões</span><span class="sxs-lookup"><span data-stu-id="54673-108">Buttons</span></span>](#buttons)
-   [<span data-ttu-id="54673-109">Áreas de dados</span><span class="sxs-lookup"><span data-stu-id="54673-109">Data areas</span></span>](#data-areas)
-   [<span data-ttu-id="54673-110">Exibição</span><span class="sxs-lookup"><span data-stu-id="54673-110">Display</span></span>](#display)
-   [<span data-ttu-id="54673-111">Dispositivos Hookswitch</span><span class="sxs-lookup"><span data-stu-id="54673-111">Hookswitch devices</span></span>](#hookswitch-devices)
-   [<span data-ttu-id="54673-112">Lâmpadas</span><span class="sxs-lookup"><span data-stu-id="54673-112">Lamps</span></span>](#lamps)
-   [<span data-ttu-id="54673-113">Abrindo e fechando dispositivos de telefone</span><span class="sxs-lookup"><span data-stu-id="54673-113">Opening and closing phone devices</span></span>](#opening-and-closing-phone-devices)
-   [<span data-ttu-id="54673-114">Inicialização e desligamento do telefone</span><span class="sxs-lookup"><span data-stu-id="54673-114">Phone initialization and shutdown</span></span>](#phone-initialization-and-shutdown)
-   [<span data-ttu-id="54673-115">Status e recursos do telefone</span><span class="sxs-lookup"><span data-stu-id="54673-115">Phone status and capabilities</span></span>](#phone-status-and-capabilities)
-   [<span data-ttu-id="54673-116">Negociação de versão do telefone</span><span class="sxs-lookup"><span data-stu-id="54673-116">Phone version negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="54673-117">Anel</span><span class="sxs-lookup"><span data-stu-id="54673-117">Ring</span></span>](#ring)
-   [<span data-ttu-id="54673-118">Status</span><span class="sxs-lookup"><span data-stu-id="54673-118">Status</span></span>](#status)

## <a name="phone-initialization-and-shutdown"></a><span data-ttu-id="54673-119">Inicialização e desligamento do telefone</span><span class="sxs-lookup"><span data-stu-id="54673-119">Phone Initialization and Shutdown</span></span>



| <span data-ttu-id="54673-120">Função</span><span class="sxs-lookup"><span data-stu-id="54673-120">Function</span></span>                                       | <span data-ttu-id="54673-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-121">Description</span></span>                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="54673-122">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="54673-122">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | <span data-ttu-id="54673-123">Inicializa a abstração de telefone TAPI para uso pelo aplicativo de invocação.</span><span class="sxs-lookup"><span data-stu-id="54673-123">Initializes TAPI phone abstraction for use by the invoking application.</span></span> <span data-ttu-id="54673-124">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-124">Synchronous.</span></span> |
| [<span data-ttu-id="54673-125">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="54673-125">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | <span data-ttu-id="54673-126">Desliga o uso de um aplicativo da abstração de telefone da TAPI.</span><span class="sxs-lookup"><span data-stu-id="54673-126">Shuts down an application's use of TAPI's phone abstraction.</span></span> <span data-ttu-id="54673-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-127">Synchronous.</span></span>            |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="54673-128">Negociação de versão do telefone</span><span class="sxs-lookup"><span data-stu-id="54673-128">Phone Version Negotiation</span></span>



| <span data-ttu-id="54673-129">Função</span><span class="sxs-lookup"><span data-stu-id="54673-129">Function</span></span>                                                     | <span data-ttu-id="54673-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-130">Description</span></span>                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="54673-131">**phoneNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="54673-131">**phoneNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | <span data-ttu-id="54673-132">Permite que um aplicativo negocie uma versão TAPI para usar o.</span><span class="sxs-lookup"><span data-stu-id="54673-132">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="54673-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-133">Synchronous.</span></span> |



 

## <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="54673-134">Abrindo e fechando dispositivos de telefone</span><span class="sxs-lookup"><span data-stu-id="54673-134">Opening and Closing Phone Devices</span></span>



| <span data-ttu-id="54673-135">Função</span><span class="sxs-lookup"><span data-stu-id="54673-135">Function</span></span>                         | <span data-ttu-id="54673-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-136">Description</span></span>                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54673-137">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="54673-137">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | <span data-ttu-id="54673-138">Abre o dispositivo de telefone especificado, concedendo ao aplicativo o proprietário ou o monitor privilégios.</span><span class="sxs-lookup"><span data-stu-id="54673-138">Opens the specified phone device, giving the application either owner or monitor privileges.</span></span> <span data-ttu-id="54673-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-139">Synchronous.</span></span> |
| [<span data-ttu-id="54673-140">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="54673-140">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | <span data-ttu-id="54673-141">Fecha um dispositivo de telefone aberto especificado.</span><span class="sxs-lookup"><span data-stu-id="54673-141">Closes a specified open phone device.</span></span> <span data-ttu-id="54673-142">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-142">Synchronous.</span></span>                                                        |



 

## <a name="phone-status-and-capabilities"></a><span data-ttu-id="54673-143">Status e recursos do telefone</span><span class="sxs-lookup"><span data-stu-id="54673-143">Phone Status and Capabilities</span></span>



| <span data-ttu-id="54673-144">Função</span><span class="sxs-lookup"><span data-stu-id="54673-144">Function</span></span>                                       | <span data-ttu-id="54673-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-145">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54673-146">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="54673-146">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | <span data-ttu-id="54673-147">Retorna os recursos de um determinado dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="54673-147">Returns the capabilities of a given phone device.</span></span> <span data-ttu-id="54673-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-148">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="54673-149">**phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="54673-149">**phoneGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | <span data-ttu-id="54673-150">Retorna uma ID de dispositivo para a classe de dispositivo determinada associada ao dispositivo de telefone especificado.</span><span class="sxs-lookup"><span data-stu-id="54673-150">Returns a device ID for the given device class associated with the specified phone device.</span></span> <span data-ttu-id="54673-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-151">Synchronous.</span></span>                                                          |
| [<span data-ttu-id="54673-152">**phoneGetIcon**</span><span class="sxs-lookup"><span data-stu-id="54673-152">**phoneGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | <span data-ttu-id="54673-153">Permite que um aplicativo recupere um ícone para exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="54673-153">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="54673-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-154">Synchronous.</span></span>                                                                                  |
| [<span data-ttu-id="54673-155">**phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="54673-155">**phoneConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | <span data-ttu-id="54673-156">Faz com que o provedor do dispositivo de telefone especificado exiba uma caixa de diálogo que permite ao usuário configurar parâmetros relacionados ao dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="54673-156">Causes the provider of the specified phone device to display a dialog box that allows the user to configure parameters related to the phone device.</span></span> <span data-ttu-id="54673-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-157">Synchronous.</span></span> |



 

## <a name="hookswitch-devices"></a><span data-ttu-id="54673-158">Dispositivos Hookswitch</span><span class="sxs-lookup"><span data-stu-id="54673-158">Hookswitch Devices</span></span>



| <span data-ttu-id="54673-159">Função</span><span class="sxs-lookup"><span data-stu-id="54673-159">Function</span></span>                                         | <span data-ttu-id="54673-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-160">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54673-161">**phoneSetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="54673-161">**phoneSetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | <span data-ttu-id="54673-162">Define o estado do gancho de dispositivos Hookswitch de um telefone aberto para um modo especificado.</span><span class="sxs-lookup"><span data-stu-id="54673-162">Sets the hook state of an open phone's hookswitch devices to a specified mode.</span></span> <span data-ttu-id="54673-163">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="54673-163">Asynchronous.</span></span>      |
| [<span data-ttu-id="54673-164">**phoneGetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="54673-164">**phoneGetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | <span data-ttu-id="54673-165">Consulta o modo Hookswitch de um dispositivo Hookswitch de um dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="54673-165">Queries the hookswitch mode of a hookswitch device of an open phone device.</span></span> <span data-ttu-id="54673-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-166">Synchronous.</span></span>          |
| [<span data-ttu-id="54673-167">**phoneSetVolume**</span><span class="sxs-lookup"><span data-stu-id="54673-167">**phoneSetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | <span data-ttu-id="54673-168">Define o volume do alto-falante de um dispositivo Hookswitch de um dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="54673-168">Sets the volume of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="54673-169">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="54673-169">Asynchronous.</span></span>           |
| [<span data-ttu-id="54673-170">**phoneGetVolume**</span><span class="sxs-lookup"><span data-stu-id="54673-170">**phoneGetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | <span data-ttu-id="54673-171">Retorna a configuração de volume do alto-falante de um dispositivo Hookswitch de um dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="54673-171">Returns the volume setting of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="54673-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-172">Synchronous.</span></span> |
| [<span data-ttu-id="54673-173">**phoneSetGain**</span><span class="sxs-lookup"><span data-stu-id="54673-173">**phoneSetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | <span data-ttu-id="54673-174">Define o lucro do MIC de um dispositivo Hookswitch de um dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="54673-174">Sets the gain of a hookswitch device's mic of an open phone device.</span></span> <span data-ttu-id="54673-175">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="54673-175">Asynchronous.</span></span>                 |
| [<span data-ttu-id="54673-176">**phoneGetGain**</span><span class="sxs-lookup"><span data-stu-id="54673-176">**phoneGetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | <span data-ttu-id="54673-177">Retorna a configuração de obter do MIC de um dispositivo Hookswitch de um telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="54673-177">Returns the gain setting of a hookswitch device's mic of an open phone.</span></span> <span data-ttu-id="54673-178">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-178">Synchronous.</span></span>              |



 

## <a name="display"></a><span data-ttu-id="54673-179">Monitor</span><span class="sxs-lookup"><span data-stu-id="54673-179">Display</span></span>



| <span data-ttu-id="54673-180">Função</span><span class="sxs-lookup"><span data-stu-id="54673-180">Function</span></span>                                   | <span data-ttu-id="54673-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-181">Description</span></span>                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="54673-182">**phoneSetDisplay**</span><span class="sxs-lookup"><span data-stu-id="54673-182">**phoneSetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | <span data-ttu-id="54673-183">Grava informações na exibição de um dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="54673-183">Writes information to the display of an open phone device.</span></span> <span data-ttu-id="54673-184">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="54673-184">Asynchronous.</span></span> |
| [<span data-ttu-id="54673-185">**phoneGetDisplay**</span><span class="sxs-lookup"><span data-stu-id="54673-185">**phoneGetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | <span data-ttu-id="54673-186">Retorna o conteúdo atual da exibição de um telefone.</span><span class="sxs-lookup"><span data-stu-id="54673-186">Returns the current contents of a phone's display.</span></span> <span data-ttu-id="54673-187">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-187">Synchronous.</span></span>          |



 

## <a name="ring"></a><span data-ttu-id="54673-188">Anel</span><span class="sxs-lookup"><span data-stu-id="54673-188">Ring</span></span>



| <span data-ttu-id="54673-189">Função</span><span class="sxs-lookup"><span data-stu-id="54673-189">Function</span></span>                             | <span data-ttu-id="54673-190">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-190">Description</span></span>                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="54673-191">**phoneSetRing**</span><span class="sxs-lookup"><span data-stu-id="54673-191">**phoneSetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | <span data-ttu-id="54673-192">Toca um dispositivo de telefone aberto de acordo com um determinado modo de toque.</span><span class="sxs-lookup"><span data-stu-id="54673-192">Rings an open phone device according to a given ring mode.</span></span> <span data-ttu-id="54673-193">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="54673-193">Asynchronous.</span></span> |
| [<span data-ttu-id="54673-194">**phoneGetRing**</span><span class="sxs-lookup"><span data-stu-id="54673-194">**phoneGetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | <span data-ttu-id="54673-195">Retorna o modo de toque atual de um dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="54673-195">Returns the current ring mode of an opened phone device.</span></span> <span data-ttu-id="54673-196">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-196">Synchronous.</span></span>    |



 

## <a name="buttons"></a><span data-ttu-id="54673-197">Botões</span><span class="sxs-lookup"><span data-stu-id="54673-197">Buttons</span></span>



| <span data-ttu-id="54673-198">Função</span><span class="sxs-lookup"><span data-stu-id="54673-198">Function</span></span>                                         | <span data-ttu-id="54673-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-199">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="54673-200">**phoneSetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="54673-200">**phoneSetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | <span data-ttu-id="54673-201">Define as informações associadas a um botão em um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="54673-201">Sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="54673-202">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="54673-202">Asynchronous.</span></span> |
| [<span data-ttu-id="54673-203">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="54673-203">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | <span data-ttu-id="54673-204">Retorna informações associadas a um botão em um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="54673-204">Returns information associated with a button on a phone device.</span></span> <span data-ttu-id="54673-205">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-205">Synchronous.</span></span>   |



 

## <a name="lamps"></a><span data-ttu-id="54673-206">Lâmpadas</span><span class="sxs-lookup"><span data-stu-id="54673-206">Lamps</span></span>



| <span data-ttu-id="54673-207">Função</span><span class="sxs-lookup"><span data-stu-id="54673-207">Function</span></span>                             | <span data-ttu-id="54673-208">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-208">Description</span></span>                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54673-209">**phoneSetLamp**</span><span class="sxs-lookup"><span data-stu-id="54673-209">**phoneSetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | <span data-ttu-id="54673-210">Ilumina uma lâmpada em um dispositivo de telefone aberto especificado em um determinado modo de iluminação.</span><span class="sxs-lookup"><span data-stu-id="54673-210">Lights a lamp on a specified open phone device in a given lamp lighting mode.</span></span> <span data-ttu-id="54673-211">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="54673-211">Asynchronous.</span></span> |
| [<span data-ttu-id="54673-212">**phoneGetLamp**</span><span class="sxs-lookup"><span data-stu-id="54673-212">**phoneGetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | <span data-ttu-id="54673-213">Retorna o modo de lâmpada atual da lâmpada especificada.</span><span class="sxs-lookup"><span data-stu-id="54673-213">Returns the current lamp mode of the specified lamp.</span></span> <span data-ttu-id="54673-214">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-214">Synchronous.</span></span>                           |



 

## <a name="data-areas"></a><span data-ttu-id="54673-215">Áreas de dados</span><span class="sxs-lookup"><span data-stu-id="54673-215">Data Areas</span></span>



| <span data-ttu-id="54673-216">Função</span><span class="sxs-lookup"><span data-stu-id="54673-216">Function</span></span>                             | <span data-ttu-id="54673-217">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-217">Description</span></span>                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="54673-218">**phoneSetData**</span><span class="sxs-lookup"><span data-stu-id="54673-218">**phoneSetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | <span data-ttu-id="54673-219">Baixa um buffer de dados para uma determinada área de dados no dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="54673-219">Downloads a buffer of data to a given data area in the phone device.</span></span> <span data-ttu-id="54673-220">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="54673-220">Asynchronous.</span></span>      |
| [<span data-ttu-id="54673-221">**phoneGetData**</span><span class="sxs-lookup"><span data-stu-id="54673-221">**phoneGetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | <span data-ttu-id="54673-222">Carrega o conteúdo de uma determinada área de dados no dispositivo de telefone para um buffer.</span><span class="sxs-lookup"><span data-stu-id="54673-222">Uploads the contents of a given data area in the phone device to a buffer.</span></span> <span data-ttu-id="54673-223">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-223">Synchronous.</span></span> |



 

## <a name="status"></a><span data-ttu-id="54673-224">Status</span><span class="sxs-lookup"><span data-stu-id="54673-224">Status</span></span>



| <span data-ttu-id="54673-225">Função</span><span class="sxs-lookup"><span data-stu-id="54673-225">Function</span></span>                                                 | <span data-ttu-id="54673-226">Descrição</span><span class="sxs-lookup"><span data-stu-id="54673-226">Description</span></span>                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54673-227">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="54673-227">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | <span data-ttu-id="54673-228">Especifica as alterações de status para as quais o aplicativo deseja ser notificado.</span><span class="sxs-lookup"><span data-stu-id="54673-228">Specifies the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="54673-229">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-229">Synchronous.</span></span> |
| [<span data-ttu-id="54673-230">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="54673-230">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | <span data-ttu-id="54673-231">Retorna as alterações de status para as quais o aplicativo deseja ser notificado.</span><span class="sxs-lookup"><span data-stu-id="54673-231">Returns the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="54673-232">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-232">Synchronous.</span></span>   |
| [<span data-ttu-id="54673-233">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="54673-233">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | <span data-ttu-id="54673-234">Retorna o status completo de um dispositivo de telefone aberto.</span><span class="sxs-lookup"><span data-stu-id="54673-234">Returns the complete status of an open phone device.</span></span> <span data-ttu-id="54673-235">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="54673-235">Synchronous.</span></span>                         |



 

 

 



