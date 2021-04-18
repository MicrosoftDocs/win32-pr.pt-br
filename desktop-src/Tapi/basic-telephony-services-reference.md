---
description: As funções de telefonia básicas são listadas por categoria nas tabelas a seguir.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Referência de serviços de telefonia básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789466"
---
# <a name="basic-telephony-services-reference"></a><span data-ttu-id="7d5d4-103">Referência de serviços de telefonia básicos</span><span class="sxs-lookup"><span data-stu-id="7d5d4-103">Basic Telephony Services Reference</span></span>

<span data-ttu-id="7d5d4-104">As funções de telefonia básicas são listadas por categoria nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-104">The Basic Telephony functions are listed by category in the following tables.</span></span> <span data-ttu-id="7d5d4-105">Uma função é identificada como [*assíncrona*](a-tapgloss.md) se ela indicar conclusão em uma mensagem de resposta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="7d5d4-106">Se a função sempre retornar seu resultado ao aplicativo imediatamente, a função será considerada [*síncrona*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="7d5d4-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="7d5d4-107">A seguir está um agrupamento funcional das funções básicas de serviço de telefonia:</span><span class="sxs-lookup"><span data-stu-id="7d5d4-107">Following is a functional grouping of the basic telephony service functions:</span></span>

-   [<span data-ttu-id="7d5d4-108">Formatos de endereço</span><span class="sxs-lookup"><span data-stu-id="7d5d4-108">Address Formats</span></span>](#address-formats)
-   [<span data-ttu-id="7d5d4-109">Endereços</span><span class="sxs-lookup"><span data-stu-id="7d5d4-109">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="7d5d4-110">Respondendo chamadas de entrada</span><span class="sxs-lookup"><span data-stu-id="7d5d4-110">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="7d5d4-111">Chamar drop Functions</span><span class="sxs-lookup"><span data-stu-id="7d5d4-111">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="7d5d4-112">Manipulação de identificador de chamada</span><span class="sxs-lookup"><span data-stu-id="7d5d4-112">Call Handle Manipulation</span></span>](#call-handle-manipulation)
-   [<span data-ttu-id="7d5d4-113">Controle de privilégio de chamada</span><span class="sxs-lookup"><span data-stu-id="7d5d4-113">Call Privilege Control</span></span>](#call-privilege-control)
-   [<span data-ttu-id="7d5d4-114">Estados de chamada e eventos</span><span class="sxs-lookup"><span data-stu-id="7d5d4-114">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="7d5d4-115">Status da linha e recursos</span><span class="sxs-lookup"><span data-stu-id="7d5d4-115">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="7d5d4-116">Negociação de versão de linha</span><span class="sxs-lookup"><span data-stu-id="7d5d4-116">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="7d5d4-117">Informações de localização e país/região</span><span class="sxs-lookup"><span data-stu-id="7d5d4-117">Location and Country/Region Information</span></span>](#location-and-countryregion-information)
-   [<span data-ttu-id="7d5d4-118">Fazendo chamadas</span><span class="sxs-lookup"><span data-stu-id="7d5d4-118">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="7d5d4-119">Abrindo e fechando dispositivos de linha</span><span class="sxs-lookup"><span data-stu-id="7d5d4-119">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="7d5d4-120">Solicitar serviços de destinatário</span><span class="sxs-lookup"><span data-stu-id="7d5d4-120">Request Recipient Services</span></span>](#request-recipient-services)
-   [<span data-ttu-id="7d5d4-121">Inicialização e desligamento TAPI</span><span class="sxs-lookup"><span data-stu-id="7d5d4-121">TAPI Initialization and Shutdown</span></span>](#tapi-initialization-and-shutdown)
-   [<span data-ttu-id="7d5d4-122">Suporte à proteção de Tarifa</span><span class="sxs-lookup"><span data-stu-id="7d5d4-122">Toll Saver Support</span></span>](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a><span data-ttu-id="7d5d4-123">Inicialização e desligamento TAPI</span><span class="sxs-lookup"><span data-stu-id="7d5d4-123">TAPI Initialization and Shutdown</span></span>



| <span data-ttu-id="7d5d4-124">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-124">Function</span></span>                                     | <span data-ttu-id="7d5d4-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-125">Description</span></span>                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-126">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-126">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | <span data-ttu-id="7d5d4-127">Inicializa a abstração de linha TAPI para uso pelo aplicativo de invocação.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-127">Initializes the TAPI line abstraction for use by the invoking application.</span></span> <span data-ttu-id="7d5d4-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-128">Synchronous.</span></span> |
| [<span data-ttu-id="7d5d4-129">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-129">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | <span data-ttu-id="7d5d4-130">Desliga o uso do aplicativo da abstração de linha da TAPI.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-130">Shuts down the application's use of TAPI's line abstraction.</span></span> <span data-ttu-id="7d5d4-131">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-131">Synchronous.</span></span>               |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="7d5d4-132">Negociação de versão de linha</span><span class="sxs-lookup"><span data-stu-id="7d5d4-132">Line Version Negotiation</span></span>



| <span data-ttu-id="7d5d4-133">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-133">Function</span></span>                                                   | <span data-ttu-id="7d5d4-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-134">Description</span></span>                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-135">**lineNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-135">**lineNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | <span data-ttu-id="7d5d4-136">Permite que um aplicativo negocie uma versão TAPI para usar o.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-136">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="7d5d4-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-137">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="7d5d4-138">Status da linha e recursos</span><span class="sxs-lookup"><span data-stu-id="7d5d4-138">Line Status and Capabilities</span></span>



| <span data-ttu-id="7d5d4-139">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-139">Function</span></span>                                               | <span data-ttu-id="7d5d4-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-140">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-141">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-141">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | <span data-ttu-id="7d5d4-142">Retorna os recursos de um determinado dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-142">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="7d5d4-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-143">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="7d5d4-144">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-144">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | <span data-ttu-id="7d5d4-145">Retorna a configuração de um dispositivo de fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-145">Returns configuration of a media stream device.</span></span> <span data-ttu-id="7d5d4-146">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-146">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="7d5d4-147">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-147">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | <span data-ttu-id="7d5d4-148">Retorna o status atual do dispositivo de linha aberta especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-148">Returns current status of the specified open line device.</span></span> <span data-ttu-id="7d5d4-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-149">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="7d5d4-150">**lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-150">**lineSetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | <span data-ttu-id="7d5d4-151">Define a configuração do dispositivo de fluxo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-151">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="7d5d4-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-152">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="7d5d4-153">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-153">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | <span data-ttu-id="7d5d4-154">Especifica as alterações de status para as quais o aplicativo precisa ser notificado.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-154">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="7d5d4-155">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-155">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="7d5d4-156">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-156">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | <span data-ttu-id="7d5d4-157">Retorna as configurações de mensagem de status da linha atual do aplicativo e do endereço.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-157">Returns the application's current line and address status message settings.</span></span> <span data-ttu-id="7d5d4-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-158">Synchronous.</span></span>                                                                       |
| [<span data-ttu-id="7d5d4-159">**lineGetID**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-159">**lineGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | <span data-ttu-id="7d5d4-160">Recupera uma ID de dispositivo associada à linha aberta, ao endereço ou à chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-160">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="7d5d4-161">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-161">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="7d5d4-162">**lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-162">**lineGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | <span data-ttu-id="7d5d4-163">Permite que um aplicativo recupere um ícone para exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-163">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="7d5d4-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-164">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="7d5d4-165">**lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-165">**lineConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | <span data-ttu-id="7d5d4-166">Faz com que o provedor do dispositivo de linha especificado exiba uma caixa de diálogo que permite ao usuário configurar parâmetros relacionados ao dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-166">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="7d5d4-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-167">Synchronous.</span></span> |
| [<span data-ttu-id="7d5d4-168">**lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-168">**lineConfigDialogEdit**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | <span data-ttu-id="7d5d4-169">Exibe uma caixa de diálogo que permite ao usuário alterar as informações de configuração de um dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-169">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="7d5d4-170">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-170">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="7d5d4-171">Endereços</span><span class="sxs-lookup"><span data-stu-id="7d5d4-171">Addresses</span></span>



| <span data-ttu-id="7d5d4-172">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-172">Function</span></span>                                             | <span data-ttu-id="7d5d4-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-173">Description</span></span>                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-174">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-174">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | <span data-ttu-id="7d5d4-175">Retorna os recursos de telefonia de um endereço.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="7d5d4-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="7d5d4-177">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-177">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | <span data-ttu-id="7d5d4-178">Retorna o status atual de um endereço especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-178">Returns current status of a specified address.</span></span> <span data-ttu-id="7d5d4-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="7d5d4-180">**lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-180">**lineGetAddressID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | <span data-ttu-id="7d5d4-181">Recupera a ID de endereço de um endereço especificado usando um formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-181">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="7d5d4-182">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-182">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="7d5d4-183">Abrindo e fechando dispositivos de linha</span><span class="sxs-lookup"><span data-stu-id="7d5d4-183">Opening and Closing Line Devices</span></span>



| <span data-ttu-id="7d5d4-184">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-184">Function</span></span>                       | <span data-ttu-id="7d5d4-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-185">Description</span></span>                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-186">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-186">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | <span data-ttu-id="7d5d4-187">Abre um dispositivo de linha especificado para fornecer monitoramento e/ou controle subsequente da linha.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="7d5d4-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-188">Synchronous.</span></span> |
| [<span data-ttu-id="7d5d4-189">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-189">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose) | <span data-ttu-id="7d5d4-190">Fecha um dispositivo de linha aberto especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-190">Closes a specified opened line device.</span></span> <span data-ttu-id="7d5d4-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-191">Synchronous.</span></span>                                                        |



 

## <a name="address-formats"></a><span data-ttu-id="7d5d4-192">Formatos de endereço</span><span class="sxs-lookup"><span data-stu-id="7d5d4-192">Address Formats</span></span>



| <span data-ttu-id="7d5d4-193">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-193">Function</span></span>                                                 | <span data-ttu-id="7d5d4-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-194">Description</span></span>                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-195">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-195">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | <span data-ttu-id="7d5d4-196">Traduz entre um endereço em formato canônico e um endereço no formato de discagem.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-196">Translates between an address in canonical format and an address in dialable format.</span></span> <span data-ttu-id="7d5d4-197">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-197">Synchronous.</span></span> |
| [<span data-ttu-id="7d5d4-198">**lineSetCurrentLocation**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-198">**lineSetCurrentLocation**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | <span data-ttu-id="7d5d4-199">Define o local usado como contexto para a conversão de endereços.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-199">Sets the location used as the context for address translation.</span></span> <span data-ttu-id="7d5d4-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-200">Synchronous.</span></span>                       |
| [<span data-ttu-id="7d5d4-201">**lineSetTollList**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-201">**lineSetTollList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | <span data-ttu-id="7d5d4-202">Manipula a lista de chamadas.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-202">Manipulates the toll list.</span></span> <span data-ttu-id="7d5d4-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-203">Synchronous.</span></span>                                                           |
| [<span data-ttu-id="7d5d4-204">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-204">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | <span data-ttu-id="7d5d4-205">Retorna recursos de conversão de endereços.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-205">Returns address translation capabilities.</span></span> <span data-ttu-id="7d5d4-206">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-206">Synchronous.</span></span>                                            |



 

## <a name="call-states-and-events"></a><span data-ttu-id="7d5d4-207">Estados de chamada e eventos</span><span class="sxs-lookup"><span data-stu-id="7d5d4-207">Call States and Events</span></span>



| <span data-ttu-id="7d5d4-208">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-208">Function</span></span>                                         | <span data-ttu-id="7d5d4-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-209">Description</span></span>                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-210">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-210">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | <span data-ttu-id="7d5d4-211">Retorna informações fixas sobre uma chamada.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-211">Returns fixed information about a call.</span></span> <span data-ttu-id="7d5d4-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-212">Synchronous.</span></span>                                |
| [<span data-ttu-id="7d5d4-213">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-213">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | <span data-ttu-id="7d5d4-214">Retorna informações de status de chamada completas para a chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-214">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="7d5d4-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-215">Synchronous.</span></span>       |
| [<span data-ttu-id="7d5d4-216">**lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-216">**lineSetAppSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | <span data-ttu-id="7d5d4-217">Define o campo específico do aplicativo da estrutura de informações de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-217">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="7d5d4-218">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-218">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="7d5d4-219">Fazendo chamadas</span><span class="sxs-lookup"><span data-stu-id="7d5d4-219">Making Calls</span></span>



| <span data-ttu-id="7d5d4-220">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-220">Function</span></span>                             | <span data-ttu-id="7d5d4-221">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-221">Description</span></span>                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-222">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-222">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | <span data-ttu-id="7d5d4-223">Faz uma chamada de saída e retorna um identificador de chamada para ela.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-223">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="7d5d4-224">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-224">Asynchronous.</span></span> |
| [<span data-ttu-id="7d5d4-225">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-225">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)         | <span data-ttu-id="7d5d4-226">Disca (partes de um ou mais) endereços de discagem.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-226">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="7d5d4-227">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-227">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="7d5d4-228">Respondendo chamadas de entrada</span><span class="sxs-lookup"><span data-stu-id="7d5d4-228">Answering Incoming Calls</span></span>



| <span data-ttu-id="7d5d4-229">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-229">Function</span></span>                         | <span data-ttu-id="7d5d4-230">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-230">Description</span></span>                             |
|----------------------------------|-----------------------------------------|
| [<span data-ttu-id="7d5d4-231">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-231">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | <span data-ttu-id="7d5d4-232">Responde a uma chamada de entrada.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-232">Answers an incoming call.</span></span> <span data-ttu-id="7d5d4-233">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-233">Asynchronous.</span></span> |



 

## <a name="toll-saver-support"></a><span data-ttu-id="7d5d4-234">Suporte à proteção de Tarifa</span><span class="sxs-lookup"><span data-stu-id="7d5d4-234">Toll Saver Support</span></span>



| <span data-ttu-id="7d5d4-235">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-235">Function</span></span>                                   | <span data-ttu-id="7d5d4-236">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-236">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-237">**lineSetNumRings**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-237">**lineSetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | <span data-ttu-id="7d5d4-238">Indica o número de anéis após o qual as chamadas de entrada devem ser respondidas.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-238">Indicates the number of rings after which incoming calls are to be answered.</span></span> <span data-ttu-id="7d5d4-239">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-239">Synchronous.</span></span>                   |
| [<span data-ttu-id="7d5d4-240">**lineGetNumRings**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-240">**lineGetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | <span data-ttu-id="7d5d4-241">Retorna o número mínimo de anéis solicitados com [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span><span class="sxs-lookup"><span data-stu-id="7d5d4-241">Returns the minimum number of rings requested with [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span></span> <span data-ttu-id="7d5d4-242">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-242">Synchronous.</span></span> |



 

## <a name="call-privilege-control"></a><span data-ttu-id="7d5d4-243">Controle de privilégio de chamada</span><span class="sxs-lookup"><span data-stu-id="7d5d4-243">Call Privilege Control</span></span>



| <span data-ttu-id="7d5d4-244">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-244">Function</span></span>                                             | <span data-ttu-id="7d5d4-245">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-245">Description</span></span>                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-246">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-246">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | <span data-ttu-id="7d5d4-247">Define o privilégio do aplicativo para o privilégio especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-247">Sets the application's privilege to the privilege specified.</span></span> <span data-ttu-id="7d5d4-248">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-248">Synchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="7d5d4-249">Chamar drop Functions</span><span class="sxs-lookup"><span data-stu-id="7d5d4-249">Call Drop Functions</span></span>



| <span data-ttu-id="7d5d4-250">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-250">Function</span></span>                                         | <span data-ttu-id="7d5d4-251">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-251">Description</span></span>                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-252">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-252">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | <span data-ttu-id="7d5d4-253">Desconecta uma chamada ou abandona uma tentativa de chamada em andamento.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-253">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="7d5d4-254">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-254">Asynchronous.</span></span> |
| [<span data-ttu-id="7d5d4-255">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-255">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | <span data-ttu-id="7d5d4-256">Desaloca o identificador de chamada especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-256">Deallocates the specified call handle.</span></span> <span data-ttu-id="7d5d4-257">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-257">Synchronous.</span></span>                       |



 

## <a name="call-handle-manipulation"></a><span data-ttu-id="7d5d4-258">Manipulação de identificador de chamada</span><span class="sxs-lookup"><span data-stu-id="7d5d4-258">Call Handle Manipulation</span></span>



| <span data-ttu-id="7d5d4-259">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-259">Function</span></span>                                                   | <span data-ttu-id="7d5d4-260">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-260">Description</span></span>                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-261">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-261">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | <span data-ttu-id="7d5d4-262">As mãos chamam a propriedade e/ou alteram os privilégios de um aplicativo para uma chamada.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-262">Hands off call ownership and/or changes an application's privileges to a call.</span></span> <span data-ttu-id="7d5d4-263">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-263">Synchronous.</span></span>                                    |
| [<span data-ttu-id="7d5d4-264">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-264">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | <span data-ttu-id="7d5d4-265">Retorna identificadores de chamada para chamadas em uma linha ou endereço especificado para os quais o aplicativo ainda não tem identificadores.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-265">Returns call handles to calls on a specified line or address for which the application does not yet have handles.</span></span> <span data-ttu-id="7d5d4-266">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-266">Synchronous.</span></span> |
| [<span data-ttu-id="7d5d4-267">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-267">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | <span data-ttu-id="7d5d4-268">Retorna uma lista de identificadores de chamada que fazem parte da mesma chamada de conferência que a chamada especificada como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-268">Returns a list of call handles that are part of the same conference call as the call specified as a parameter.</span></span> <span data-ttu-id="7d5d4-269">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-269">Synchronous.</span></span>    |



 

## <a name="location-and-countryregion-information"></a><span data-ttu-id="7d5d4-270">Informações de localização e país/região</span><span class="sxs-lookup"><span data-stu-id="7d5d4-270">Location and Country/Region Information</span></span>



| <span data-ttu-id="7d5d4-271">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-271">Function</span></span>                                           | <span data-ttu-id="7d5d4-272">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-272">Description</span></span>                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-273">**lineTranslateDialog**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-273">**lineTranslateDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | <span data-ttu-id="7d5d4-274">Exibe uma caixa de diálogo que permite ao usuário alterar o local e as informações do cartão de chamada.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-274">Displays a dialog box allowing the user to change location and calling card information.</span></span> <span data-ttu-id="7d5d4-275">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-275">Synchronous.</span></span> |
| [<span data-ttu-id="7d5d4-276">**lineGetCountry**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-276">**lineGetCountry**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | <span data-ttu-id="7d5d4-277">Recupera regras de discagem e outras informações sobre um determinado país/região.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-277">Retrieves dialing rules and other information about a given country/region.</span></span> <span data-ttu-id="7d5d4-278">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-278">Synchronous.</span></span>              |



 

## <a name="request-recipient-services"></a><span data-ttu-id="7d5d4-279">Solicitar serviços de destinatário</span><span class="sxs-lookup"><span data-stu-id="7d5d4-279">Request Recipient Services</span></span>

<span data-ttu-id="7d5d4-280">As duas funções a seguir são usadas apenas no suporte à telefonia assistida.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-280">The following two functions are used only in support of Assisted Telephony.</span></span>



| <span data-ttu-id="7d5d4-281">Função</span><span class="sxs-lookup"><span data-stu-id="7d5d4-281">Function</span></span>                                                             | <span data-ttu-id="7d5d4-282">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d5d4-282">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d4-283">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-283">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="7d5d4-284">Registra ou cancela o registro do aplicativo como um destinatário de solicitação para o modo de solicitação especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-284">Registers or deregisters the application as a request recipient for the specified request mode.</span></span> <span data-ttu-id="7d5d4-285">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-285">Synchronous.</span></span> |
| [<span data-ttu-id="7d5d4-286">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="7d5d4-286">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | <span data-ttu-id="7d5d4-287">Obtém a próxima solicitação da biblioteca de vínculo dinâmico de telefonia.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-287">Gets the next request from the Telephony dynamic link library.</span></span> <span data-ttu-id="7d5d4-288">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7d5d4-288">Synchronous.</span></span>                                  |



 

 

 



