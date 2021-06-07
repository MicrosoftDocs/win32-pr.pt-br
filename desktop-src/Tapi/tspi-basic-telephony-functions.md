---
description: Todos os provedores de serviço devem implementar funções de telefonia básicas.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funções de telefonia básicas do TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524150"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="3c073-103">Funções de telefonia básicas do TSPI</span><span class="sxs-lookup"><span data-stu-id="3c073-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="3c073-104">Todos os provedores de serviço devem implementar funções de telefonia básicas.</span><span class="sxs-lookup"><span data-stu-id="3c073-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="3c073-105">Veja a seguir uma lista dessas funções por categoria.</span><span class="sxs-lookup"><span data-stu-id="3c073-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="3c073-106">Uma função é identificada como *assíncrona* se ela indicar conclusão em uma mensagem de resposta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c073-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="3c073-107">Se a função sempre retornar seu resultado imediatamente, a função será considerada *síncrona*.</span><span class="sxs-lookup"><span data-stu-id="3c073-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="3c073-108">Endereços</span><span class="sxs-lookup"><span data-stu-id="3c073-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="3c073-109">Respondendo chamadas de entrada</span><span class="sxs-lookup"><span data-stu-id="3c073-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="3c073-110">Chamar drop Functions</span><span class="sxs-lookup"><span data-stu-id="3c073-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="3c073-111">Estados de chamada e eventos</span><span class="sxs-lookup"><span data-stu-id="3c073-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="3c073-112">Status da linha e recursos</span><span class="sxs-lookup"><span data-stu-id="3c073-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="3c073-113">Negociação de versão de linha</span><span class="sxs-lookup"><span data-stu-id="3c073-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="3c073-114">Fazendo chamadas</span><span class="sxs-lookup"><span data-stu-id="3c073-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="3c073-115">Abrindo e fechando dispositivos de linha</span><span class="sxs-lookup"><span data-stu-id="3c073-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="3c073-116">Negociação de versão do telefone</span><span class="sxs-lookup"><span data-stu-id="3c073-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="3c073-117">Inicialização e desligamento do TSP</span><span class="sxs-lookup"><span data-stu-id="3c073-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="3c073-118">Inicialização e desligamento do TSP</span><span class="sxs-lookup"><span data-stu-id="3c073-118">TSP Initialization and Shutdown</span></span>



|  <span data-ttu-id="3c073-119">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-119">Function</span></span>                                                         |   <span data-ttu-id="3c073-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-120">Description</span></span>                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="3c073-121">**TUISPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="3c073-121">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="3c073-122">Instala um TSP.</span><span class="sxs-lookup"><span data-stu-id="3c073-122">Installs a TSP.</span></span> <span data-ttu-id="3c073-123">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-123">Synchronous.</span></span>                              |
| [<span data-ttu-id="3c073-124">**TSPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="3c073-124">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="3c073-125">Instala o TSP.</span><span class="sxs-lookup"><span data-stu-id="3c073-125">Installs the TSP.</span></span> <span data-ttu-id="3c073-126">Obsoleto com a versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="3c073-126">Obsolete with Version 2.0.</span></span> <span data-ttu-id="3c073-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-127">Synchronous.</span></span> |
| [<span data-ttu-id="3c073-128">**TSPI \_ providerInit**</span><span class="sxs-lookup"><span data-stu-id="3c073-128">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="3c073-129">Inicializa o TSP.</span><span class="sxs-lookup"><span data-stu-id="3c073-129">Initializes the TSP.</span></span> <span data-ttu-id="3c073-130">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-130">Synchronous.</span></span>                         |
| [<span data-ttu-id="3c073-131">**TSPI \_ providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="3c073-131">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="3c073-132">Desliga o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3c073-132">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="3c073-133">**TUISPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="3c073-133">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="3c073-134">Remove um TSP.</span><span class="sxs-lookup"><span data-stu-id="3c073-134">Removes a TSP.</span></span> <span data-ttu-id="3c073-135">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-135">Synchronous.</span></span>                               |
| [<span data-ttu-id="3c073-136">**TSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="3c073-136">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="3c073-137">Remove um TSP.</span><span class="sxs-lookup"><span data-stu-id="3c073-137">Removes a TSP.</span></span> <span data-ttu-id="3c073-138">Obsoleto com a versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="3c073-138">Obsolete with Version 2.0.</span></span> <span data-ttu-id="3c073-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-139">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="3c073-140">Negociação de versão do telefone</span><span class="sxs-lookup"><span data-stu-id="3c073-140">Phone Version Negotiation</span></span>



|  <span data-ttu-id="3c073-141">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-141">Function</span></span>                                                         |   <span data-ttu-id="3c073-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-142">Description</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c073-143">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="3c073-143">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="3c073-144">Retorna a versão SPI mais alta com a qual o provedor de serviços pode operar para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c073-144">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="3c073-145">Negociação de versão de linha</span><span class="sxs-lookup"><span data-stu-id="3c073-145">Line Version Negotiation</span></span>



|  <span data-ttu-id="3c073-146">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-146">Function</span></span>                                                         |   <span data-ttu-id="3c073-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-147">Description</span></span>                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c073-148">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="3c073-148">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="3c073-149">Permite que um aplicativo negocie uma versão do TSPI para usar com um determinado dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3c073-149">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="3c073-150">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-150">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="3c073-151">Status da linha e recursos</span><span class="sxs-lookup"><span data-stu-id="3c073-151">Line Status and Capabilities</span></span>



|  <span data-ttu-id="3c073-152">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-152">Function</span></span>                                                         |   <span data-ttu-id="3c073-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-153">Description</span></span>                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c073-154">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="3c073-154">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="3c073-155">Retorna os recursos de um determinado dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3c073-155">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="3c073-156">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-156">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="3c073-157">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="3c073-157">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="3c073-158">Retorna a configuração de um dispositivo de fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3c073-158">Returns configuration of a media stream device.</span></span> <span data-ttu-id="3c073-159">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-159">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="3c073-160">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="3c073-160">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="3c073-161">Retorna o status atual do dispositivo de linha aberta especificado.</span><span class="sxs-lookup"><span data-stu-id="3c073-161">Returns current status of the specified open line device.</span></span> <span data-ttu-id="3c073-162">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-162">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="3c073-163">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="3c073-163">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="3c073-164">Define a configuração do dispositivo de fluxo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="3c073-164">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="3c073-165">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-165">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="3c073-166">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="3c073-166">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="3c073-167">Especifica as alterações de status para as quais o aplicativo precisa ser notificado.</span><span class="sxs-lookup"><span data-stu-id="3c073-167">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="3c073-168">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-168">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="3c073-169">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="3c073-169">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="3c073-170">Recupera uma ID de dispositivo associada à linha aberta, ao endereço ou à chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="3c073-170">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="3c073-171">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-171">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="3c073-172">**TSPI \_ lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="3c073-172">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="3c073-173">Permite que um aplicativo recupere um ícone para exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3c073-173">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="3c073-174">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-174">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="3c073-175">**TUISPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="3c073-175">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="3c073-176">Faz com que o provedor do dispositivo de linha especificado exiba uma caixa de diálogo que permite ao usuário configurar parâmetros relacionados ao dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3c073-176">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="3c073-177">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-177">Synchronous.</span></span> |
| [<span data-ttu-id="3c073-178">**TUISPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="3c073-178">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="3c073-179">Exibe uma caixa de diálogo que permite ao usuário alterar as informações de configuração de um dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3c073-179">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="3c073-180">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-180">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="3c073-181">Endereços</span><span class="sxs-lookup"><span data-stu-id="3c073-181">Addresses</span></span>



|  <span data-ttu-id="3c073-182">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-182">Function</span></span>                                                         |   <span data-ttu-id="3c073-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-183">Description</span></span>                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c073-184">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="3c073-184">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="3c073-185">Retorna os recursos de telefonia de um endereço.</span><span class="sxs-lookup"><span data-stu-id="3c073-185">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="3c073-186">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-186">Synchronous.</span></span>                           |
| [<span data-ttu-id="3c073-187">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="3c073-187">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="3c073-188">Retorna o status atual de um endereço especificado.</span><span class="sxs-lookup"><span data-stu-id="3c073-188">Returns current status of a specified address.</span></span> <span data-ttu-id="3c073-189">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-189">Synchronous.</span></span>                              |
| [<span data-ttu-id="3c073-190">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="3c073-190">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="3c073-191">Recupera o número de identificadores de endereço com suporte na linha indicada.</span><span class="sxs-lookup"><span data-stu-id="3c073-191">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="3c073-192">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="3c073-192">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="3c073-193">Recupera a ID de endereço de um endereço especificado usando um formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="3c073-193">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="3c073-194">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-194">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="3c073-195">Abrindo e fechando dispositivos de linha</span><span class="sxs-lookup"><span data-stu-id="3c073-195">Opening and Closing Line Devices</span></span>



|  <span data-ttu-id="3c073-196">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-196">Function</span></span>                                                         |   <span data-ttu-id="3c073-197">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-197">Description</span></span>                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c073-198">**TSPI \_ lineOpen**</span><span class="sxs-lookup"><span data-stu-id="3c073-198">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="3c073-199">Abre um dispositivo de linha especificado para fornecer monitoramento e/ou controle subsequente da linha.</span><span class="sxs-lookup"><span data-stu-id="3c073-199">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="3c073-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-200">Synchronous.</span></span> |
| [<span data-ttu-id="3c073-201">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="3c073-201">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="3c073-202">Fecha um dispositivo de linha aberta especificado.</span><span class="sxs-lookup"><span data-stu-id="3c073-202">Closes a specified opened line device.</span></span> <span data-ttu-id="3c073-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-203">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="3c073-204">Chamar estados e eventos</span><span class="sxs-lookup"><span data-stu-id="3c073-204">Call States and Events</span></span>



|  <span data-ttu-id="3c073-205">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-205">Function</span></span>                                                         |   <span data-ttu-id="3c073-206">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-206">Description</span></span>                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c073-207">**Linha \_ TSPIGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="3c073-207">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="3c073-208">Retorna informações fixas sobre uma chamada.</span><span class="sxs-lookup"><span data-stu-id="3c073-208">Returns fixed information about a call.</span></span> <span data-ttu-id="3c073-209">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-209">Synchronous.</span></span>                                |
| [<span data-ttu-id="3c073-210">**Linha \_ TSPIGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="3c073-210">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="3c073-211">Retorna informações completas de status de chamada para a chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="3c073-211">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="3c073-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-212">Synchronous.</span></span>       |
| [<span data-ttu-id="3c073-213">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="3c073-213">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="3c073-214">Define o campo específico do aplicativo da estrutura de informações de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="3c073-214">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="3c073-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="3c073-215">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="3c073-216">Fazendo chamadas</span><span class="sxs-lookup"><span data-stu-id="3c073-216">Making Calls</span></span>



|  <span data-ttu-id="3c073-217">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-217">Function</span></span>                                                         |   <span data-ttu-id="3c073-218">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-218">Description</span></span>                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="3c073-219">**Linha \_ TSPIMakeCall**</span><span class="sxs-lookup"><span data-stu-id="3c073-219">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="3c073-220">Faz uma chamada de saída e retorna um alça de chamada para ela.</span><span class="sxs-lookup"><span data-stu-id="3c073-220">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="3c073-221">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="3c073-221">Asynchronous.</span></span> |
| [<span data-ttu-id="3c073-222">**TSPI \_ lineDial**</span><span class="sxs-lookup"><span data-stu-id="3c073-222">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="3c073-223">Disca (partes de um ou mais) endereços discáveis.</span><span class="sxs-lookup"><span data-stu-id="3c073-223">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="3c073-224">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="3c073-224">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="3c073-225">Respondendo chamadas de entrada</span><span class="sxs-lookup"><span data-stu-id="3c073-225">Answering Incoming Calls</span></span>



|  <span data-ttu-id="3c073-226">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-226">Function</span></span>                                                         |   <span data-ttu-id="3c073-227">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-227">Description</span></span>                                                        |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="3c073-228">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="3c073-228">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="3c073-229">Responde a uma chamada de entrada.</span><span class="sxs-lookup"><span data-stu-id="3c073-229">Answers an incoming call.</span></span> <span data-ttu-id="3c073-230">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="3c073-230">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="3c073-231">Funções de soltar chamada</span><span class="sxs-lookup"><span data-stu-id="3c073-231">Call Drop Functions</span></span>



|  <span data-ttu-id="3c073-232">Função</span><span class="sxs-lookup"><span data-stu-id="3c073-232">Function</span></span>                                                         |   <span data-ttu-id="3c073-233">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c073-233">Description</span></span>                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="3c073-234">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="3c073-234">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="3c073-235">Desconecta uma chamada ou abandonará uma tentativa de chamada em andamento.</span><span class="sxs-lookup"><span data-stu-id="3c073-235">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="3c073-236">Assíncrono.</span><span class="sxs-lookup"><span data-stu-id="3c073-236">Asynchronous.</span></span> |



 

 

 
