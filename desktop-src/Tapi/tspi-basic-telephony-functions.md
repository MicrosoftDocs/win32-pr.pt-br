---
description: Todos os provedores de serviço devem implementar funções de telefonia básicas.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funções de telefonia básicas do TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837179"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="cd9f2-103">Funções de telefonia básicas do TSPI</span><span class="sxs-lookup"><span data-stu-id="cd9f2-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="cd9f2-104">Todos os provedores de serviço devem implementar funções de telefonia básicas.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="cd9f2-105">Veja a seguir uma lista dessas funções por categoria.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="cd9f2-106">Uma função é identificada como *assíncrona* se ela indicar conclusão em uma mensagem de resposta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="cd9f2-107">Se a função sempre retornar seu resultado imediatamente, a função será considerada *síncrona*.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="cd9f2-108">Endereços</span><span class="sxs-lookup"><span data-stu-id="cd9f2-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="cd9f2-109">Respondendo chamadas de entrada</span><span class="sxs-lookup"><span data-stu-id="cd9f2-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="cd9f2-110">Chamar drop Functions</span><span class="sxs-lookup"><span data-stu-id="cd9f2-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="cd9f2-111">Estados de chamada e eventos</span><span class="sxs-lookup"><span data-stu-id="cd9f2-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="cd9f2-112">Status da linha e recursos</span><span class="sxs-lookup"><span data-stu-id="cd9f2-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="cd9f2-113">Negociação de versão de linha</span><span class="sxs-lookup"><span data-stu-id="cd9f2-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="cd9f2-114">Fazendo chamadas</span><span class="sxs-lookup"><span data-stu-id="cd9f2-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="cd9f2-115">Abrindo e fechando dispositivos de linha</span><span class="sxs-lookup"><span data-stu-id="cd9f2-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="cd9f2-116">Negociação de versão do telefone</span><span class="sxs-lookup"><span data-stu-id="cd9f2-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="cd9f2-117">Inicialização e desligamento do TSP</span><span class="sxs-lookup"><span data-stu-id="cd9f2-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="cd9f2-118">Inicialização e desligamento do TSP</span><span class="sxs-lookup"><span data-stu-id="cd9f2-118">TSP Initialization and Shutdown</span></span>



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="cd9f2-119">**TUISPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-119">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="cd9f2-120">Instala um TSP.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-120">Installs a TSP.</span></span> <span data-ttu-id="cd9f2-121">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-121">Synchronous.</span></span>                              |
| [<span data-ttu-id="cd9f2-122">**TSPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-122">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="cd9f2-123">Instala o TSP.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-123">Installs the TSP.</span></span> <span data-ttu-id="cd9f2-124">Obsoleto com a versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-124">Obsolete with Version 2.0.</span></span> <span data-ttu-id="cd9f2-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-125">Synchronous.</span></span> |
| [<span data-ttu-id="cd9f2-126">**TSPI \_ providerInit**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-126">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="cd9f2-127">Inicializa o TSP.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-127">Initializes the TSP.</span></span> <span data-ttu-id="cd9f2-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-128">Synchronous.</span></span>                         |
| [<span data-ttu-id="cd9f2-129">**TSPI \_ providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-129">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="cd9f2-130">Desliga o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-130">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="cd9f2-131">**TUISPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-131">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="cd9f2-132">Remove um TSP.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-132">Removes a TSP.</span></span> <span data-ttu-id="cd9f2-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-133">Synchronous.</span></span>                               |
| [<span data-ttu-id="cd9f2-134">**TSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-134">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="cd9f2-135">Remove um TSP.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-135">Removes a TSP.</span></span> <span data-ttu-id="cd9f2-136">Obsoleto com a versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-136">Obsolete with Version 2.0.</span></span> <span data-ttu-id="cd9f2-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-137">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="cd9f2-138">Negociação de versão do telefone</span><span class="sxs-lookup"><span data-stu-id="cd9f2-138">Phone Version Negotiation</span></span>



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd9f2-139">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-139">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="cd9f2-140">Retorna a versão SPI mais alta com a qual o provedor de serviços pode operar para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-140">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="cd9f2-141">Negociação de versão de linha</span><span class="sxs-lookup"><span data-stu-id="cd9f2-141">Line Version Negotiation</span></span>



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd9f2-142">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-142">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="cd9f2-143">Permite que um aplicativo negocie uma versão do TSPI para usar com um determinado dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-143">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="cd9f2-144">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-144">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="cd9f2-145">Status da linha e recursos</span><span class="sxs-lookup"><span data-stu-id="cd9f2-145">Line Status and Capabilities</span></span>



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd9f2-146">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="cd9f2-147">Retorna os recursos de um determinado dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-147">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="cd9f2-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-148">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="cd9f2-149">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-149">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="cd9f2-150">Retorna a configuração de um dispositivo de fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-150">Returns configuration of a media stream device.</span></span> <span data-ttu-id="cd9f2-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-151">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="cd9f2-152">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-152">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="cd9f2-153">Retorna o status atual do dispositivo de linha aberta especificado.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-153">Returns current status of the specified open line device.</span></span> <span data-ttu-id="cd9f2-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-154">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="cd9f2-155">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-155">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="cd9f2-156">Define a configuração do dispositivo de fluxo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-156">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="cd9f2-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-157">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="cd9f2-158">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-158">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="cd9f2-159">Especifica as alterações de status para as quais o aplicativo precisa ser notificado.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-159">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="cd9f2-160">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-160">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="cd9f2-161">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-161">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="cd9f2-162">Recupera uma ID de dispositivo associada à linha aberta, ao endereço ou à chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-162">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="cd9f2-163">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-163">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="cd9f2-164">**TSPI \_ lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-164">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="cd9f2-165">Permite que um aplicativo recupere um ícone para exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-165">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="cd9f2-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-166">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="cd9f2-167">**TUISPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-167">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="cd9f2-168">Faz com que o provedor do dispositivo de linha especificado exiba uma caixa de diálogo que permite ao usuário configurar parâmetros relacionados ao dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-168">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="cd9f2-169">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-169">Synchronous.</span></span> |
| [<span data-ttu-id="cd9f2-170">**TUISPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-170">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="cd9f2-171">Exibe uma caixa de diálogo que permite ao usuário alterar as informações de configuração de um dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-171">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="cd9f2-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-172">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="cd9f2-173">Endereços</span><span class="sxs-lookup"><span data-stu-id="cd9f2-173">Addresses</span></span>



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd9f2-174">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-174">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="cd9f2-175">Retorna os recursos de telefonia de um endereço.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="cd9f2-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="cd9f2-177">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-177">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="cd9f2-178">Retorna o status atual de um endereço especificado.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-178">Returns current status of a specified address.</span></span> <span data-ttu-id="cd9f2-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="cd9f2-180">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-180">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="cd9f2-181">Recupera o número de identificadores de endereço com suporte na linha indicada.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-181">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="cd9f2-182">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-182">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="cd9f2-183">Recupera a ID de endereço de um endereço especificado usando um formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-183">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="cd9f2-184">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-184">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="cd9f2-185">Abrindo e fechando dispositivos de linha</span><span class="sxs-lookup"><span data-stu-id="cd9f2-185">Opening and Closing Line Devices</span></span>



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd9f2-186">**TSPI \_ lineOpen**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-186">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="cd9f2-187">Abre um dispositivo de linha especificado para fornecer monitoramento e/ou controle subsequente da linha.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="cd9f2-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-188">Synchronous.</span></span> |
| [<span data-ttu-id="cd9f2-189">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-189">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="cd9f2-190">Fecha um dispositivo de linha aberto especificado.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-190">Closes a specified opened line device.</span></span> <span data-ttu-id="cd9f2-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-191">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="cd9f2-192">Estados de chamada e eventos</span><span class="sxs-lookup"><span data-stu-id="cd9f2-192">Call States and Events</span></span>



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd9f2-193">**TSPI \_ lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-193">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="cd9f2-194">Retorna informações fixas sobre uma chamada.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-194">Returns fixed information about a call.</span></span> <span data-ttu-id="cd9f2-195">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-195">Synchronous.</span></span>                                |
| [<span data-ttu-id="cd9f2-196">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-196">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="cd9f2-197">Retorna informações de status de chamada completas para a chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-197">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="cd9f2-198">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-198">Synchronous.</span></span>       |
| [<span data-ttu-id="cd9f2-199">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-199">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="cd9f2-200">Define o campo específico do aplicativo da estrutura de informações de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-200">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="cd9f2-201">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-201">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="cd9f2-202">Fazendo chamadas</span><span class="sxs-lookup"><span data-stu-id="cd9f2-202">Making Calls</span></span>



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="cd9f2-203">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-203">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="cd9f2-204">Faz uma chamada de saída e retorna um identificador de chamada para ela.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-204">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="cd9f2-205">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-205">Asynchronous.</span></span> |
| [<span data-ttu-id="cd9f2-206">**TSPI \_ lineDial**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-206">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="cd9f2-207">Disca (partes de um ou mais) endereços de discagem.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-207">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="cd9f2-208">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-208">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="cd9f2-209">Respondendo chamadas de entrada</span><span class="sxs-lookup"><span data-stu-id="cd9f2-209">Answering Incoming Calls</span></span>



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="cd9f2-210">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-210">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="cd9f2-211">Responde a uma chamada de entrada.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-211">Answers an incoming call.</span></span> <span data-ttu-id="cd9f2-212">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-212">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="cd9f2-213">Chamar drop Functions</span><span class="sxs-lookup"><span data-stu-id="cd9f2-213">Call Drop Functions</span></span>



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="cd9f2-214">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="cd9f2-214">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="cd9f2-215">Desconecta uma chamada ou abandona uma tentativa de chamada em andamento.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-215">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="cd9f2-216">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="cd9f2-216">Asynchronous.</span></span> |



 

 

 
