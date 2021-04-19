---
description: As APIs de DLP (prevenção de perda de dados) do ponto de extremidade permitem que os aplicativos notifiquem o sistema operacional antes e depois de determinadas operações, como abrir ou salvar um arquivo.
title: Prevenção de perda de dados do ponto de extremidade
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 867e059e0accfc1208c96394c3065d69cf9f576c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495312"
---
# <a name="endpoint-data-loss-prevention"></a><span data-ttu-id="099eb-103">Prevenção de perda de dados do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="099eb-103">Endpoint data loss prevention</span></span>

<span data-ttu-id="099eb-104">O Windows 10 implementa mecanismos que ajudam a evitar a perda de dados para arquivos confidenciais.</span><span class="sxs-lookup"><span data-stu-id="099eb-104">Windows 10 implements mechanisms that help to prevent data loss for sensitive files.</span></span> <span data-ttu-id="099eb-105">As APIs de DLP (prevenção de perda de dados) do ponto de extremidade permitem que os aplicativos notifiquem o sistema operacional antes e depois de determinadas operações, como abrir ou salvar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="099eb-105">The endpoint data loss prevention (DLP) APIs allow applications to notify the OS before and after certain operations, such as opening or saving a file.</span></span> <span data-ttu-id="099eb-106">Essas notificações servem como "dicas" que permitem que o sistema Otimize as operações de perda de dados.</span><span class="sxs-lookup"><span data-stu-id="099eb-106">These notifications serve as "hints" that allow the system to optimize data loss operations.</span></span>

## <a name="location-of-the-dlp-dll"></a><span data-ttu-id="099eb-107">Local da dll DLP</span><span class="sxs-lookup"><span data-stu-id="099eb-107">Location of the DLP dll</span></span>

<span data-ttu-id="099eb-108">Como a DLL do Endpoint DLP não é empacotada com o SDK do Windows, os aplicativos precisarão carregar a dll manualmente no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="099eb-108">Since the endpoint DLP dll isn't bundled with the Windows SDK, applications will need to load the dll manually at runtime.</span></span> <span data-ttu-id="099eb-109">O caminho para o local da dll é armazenado no registro.</span><span class="sxs-lookup"><span data-stu-id="099eb-109">The path to the dll location is stored in the registry.</span></span> <span data-ttu-id="099eb-110">A tabela a seguir lista as chaves e os valores do registro que armazenam essas informações.</span><span class="sxs-lookup"><span data-stu-id="099eb-110">The following table lists the registry keys and values that store this information.</span></span> <span data-ttu-id="099eb-111">Esses caminhos são definidos como constantes na listagem de código de exemplo endpointdlp. h fornecida abaixo como uma conveniência para os desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="099eb-111">These paths are defined as constants in the sample endpointdlp.h code listing provided below as a convenience for developers.</span></span>

| <span data-ttu-id="099eb-112">Constante</span><span class="sxs-lookup"><span data-stu-id="099eb-112">Constant</span></span> | <span data-ttu-id="099eb-113">Valor</span><span class="sxs-lookup"><span data-stu-id="099eb-113">Value</span></span> | <span data-ttu-id="099eb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="099eb-114">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="099eb-115">ENDPOINTDLP_DLL_NAME</span><span class="sxs-lookup"><span data-stu-id="099eb-115">ENDPOINTDLP_DLL_NAME</span></span> | <span data-ttu-id="099eb-116">"EndpointDlp.dll"</span><span class="sxs-lookup"><span data-stu-id="099eb-116">"EndpointDlp.dll"</span></span> | <span data-ttu-id="099eb-117">O nome da DLL de DLP do ponto de extremidade que fornece a API</span><span class="sxs-lookup"><span data-stu-id="099eb-117">The name of the Endpoint DLP DLL that provides the API</span></span> |
| <span data-ttu-id="099eb-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="099eb-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> | <span data-ttu-id="099eb-119">"SOFTWARE \\ Microsoft \\ Windows Defender"</span><span class="sxs-lookup"><span data-stu-id="099eb-119">"SOFTWARE\\Microsoft\\Windows Defender"</span></span> | <span data-ttu-id="099eb-120">Chave do registro do Windows Defender em HKLM, em que algumas configurações de DLP de ponto de extremidade são armazenadas</span><span class="sxs-lookup"><span data-stu-id="099eb-120">Windows Defender registry key under HKLM where some Endpoint DLP settings are stored</span></span> |
| <span data-ttu-id="099eb-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span><span class="sxs-lookup"><span data-stu-id="099eb-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span></span> | <span data-ttu-id="099eb-122">Valor de ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="099eb-122">Value of ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |  <span data-ttu-id="099eb-123">O caminho do registro na chave HKLM da qual o local de instalação do EndpointDlp.dll pode ser obtido</span><span class="sxs-lookup"><span data-stu-id="099eb-123">The registry path under HKLM key from which the EndpointDlp.dll install location can be obtained</span></span> |
| <span data-ttu-id="099eb-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="099eb-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span></span> | <span data-ttu-id="099eb-125">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="099eb-125">"InstallLocation"</span></span> | <span data-ttu-id="099eb-126">O valor do registro em ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY no qual o local de instalação do EndpointDlp.dll está armazenado</span><span class="sxs-lookup"><span data-stu-id="099eb-126">The registry value under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in which the EndpointDlp.dll install location is stored</span></span> |
| <span data-ttu-id="099eb-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span><span class="sxs-lookup"><span data-stu-id="099eb-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span></span> | <span data-ttu-id="099eb-128">x86</span><span class="sxs-lookup"><span data-stu-id="099eb-128">"x86"</span></span> | <span data-ttu-id="099eb-129">Em plataformas x64, concatene esse diretório para obter a versão x86 do EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="099eb-129">On x64 platforms, concatenate this directory to obtain the x86 version of EndpointDlp.dll</span></span> |

## <a name="check-if-endpoint-dlp-is-enabled"></a><span data-ttu-id="099eb-130">Verificar se o Endpoint DLP está habilitado</span><span class="sxs-lookup"><span data-stu-id="099eb-130">Check if endpoint DLP is enabled</span></span>

<span data-ttu-id="099eb-131">Para determinar se o Endpoint DLP está habilitado no sistema, verifique o seguinte valor de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="099eb-131">To determine if endpoint DLP is enabled on the system, check the following registry key value.</span></span> 

| <span data-ttu-id="099eb-132">Constante</span><span class="sxs-lookup"><span data-stu-id="099eb-132">Constant</span></span> | <span data-ttu-id="099eb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="099eb-133">Value</span></span> | <span data-ttu-id="099eb-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="099eb-134">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="099eb-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span><span class="sxs-lookup"><span data-stu-id="099eb-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span></span> |  <span data-ttu-id="099eb-136">" \\ Recursos"</span><span class="sxs-lookup"><span data-stu-id="099eb-136">"\\Features"</span></span> | <span data-ttu-id="099eb-137">O caminho para a chave de sinalizador habilitada para DLP de ponto de extremidade em (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="099eb-137">The path to the Endpoint DLP enabled flag key under (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |
| <span data-ttu-id="099eb-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="099eb-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span></span> | <span data-ttu-id="099eb-139">"SenseDlpEnabled"</span><span class="sxs-lookup"><span data-stu-id="099eb-139">"SenseDlpEnabled"</span></span> | <span data-ttu-id="099eb-140">O valor do registro em ENDPOINTDLP_ENABLED_FLAG_REGKEY que contém a chave do registro de sinalizador habilitado para DLP</span><span class="sxs-lookup"><span data-stu-id="099eb-140">The registry value under ENDPOINTDLP_ENABLED_FLAG_REGKEY containing the DLP enabled flag registry key</span></span>

## <a name="endpoint-dlp-apis"></a><span data-ttu-id="099eb-141">APIs DLP de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="099eb-141">Endpoint DLP APIs</span></span>

<span data-ttu-id="099eb-142">As tabelas a seguir listam as APIs fornecidas pela DLL do Endpoint DLP.</span><span class="sxs-lookup"><span data-stu-id="099eb-142">The following tables list the APIs provided by the endpoint DLP dll.</span></span>

### <a name="initialization-and-versioning"></a><span data-ttu-id="099eb-143">Inicialização e controle de versão</span><span class="sxs-lookup"><span data-stu-id="099eb-143">Initialization and versioning</span></span>

| <span data-ttu-id="099eb-144">API</span><span class="sxs-lookup"><span data-stu-id="099eb-144">API</span></span> | <span data-ttu-id="099eb-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="099eb-145">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="099eb-146">DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="099eb-146">DlpInitializeEnforcementMode</span></span>](endpointdlp-dlpinitializeenforcementmode.md)                       | <span data-ttu-id="099eb-147">Notifica o sistema sobre os modos de imposição desejados para um conjunto de operações de DLP (prevenção de perda de dados) de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="099eb-147">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>                                  |
| [<span data-ttu-id="099eb-148">DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="099eb-148">DlpGetEnforcementApiVersion</span></span>](endpointdlp-dlpgetenforcementapiversion.md)                       | <span data-ttu-id="099eb-149">Recupera a versão da API DLP (prevenção de perda de dados) do ponto de extremidade no dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="099eb-149">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>                                  |


### <a name="document-operations"></a><span data-ttu-id="099eb-150">Operações de documento</span><span class="sxs-lookup"><span data-stu-id="099eb-150">Document operations</span></span>

| <span data-ttu-id="099eb-151">API</span><span class="sxs-lookup"><span data-stu-id="099eb-151">API</span></span> | <span data-ttu-id="099eb-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="099eb-152">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="099eb-153">DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="099eb-153">DlpNotifyPreOpenDocument</span></span>](endpointdlp-dlpnotifypreopendocument.md) | <span data-ttu-id="099eb-154">Fornece ao sistema informações sobre um documento antes que a operação de abertura seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-154">Provides the system with information about a document before the open operation is initiated.</span></span> |
| [<span data-ttu-id="099eb-155">DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="099eb-155">DlpNotifyPostOpenDocument</span></span>](endpointdlp-dlpnotifypostopendocument.md) | <span data-ttu-id="099eb-156">Fornece ao sistema informações sobre um documento após a conclusão da operação de abertura.</span><span class="sxs-lookup"><span data-stu-id="099eb-156">Provides the system with information about a document after the open operation is completed.</span></span>  |
| [<span data-ttu-id="099eb-157">DlpNotifyCloseDocument</span><span class="sxs-lookup"><span data-stu-id="099eb-157">DlpNotifyCloseDocument</span></span>](endpointdlp-dlpnotifyclosedocument.md)                       | <span data-ttu-id="099eb-158">Fornece ao sistema informações sobre um documento antes da operação de fechamento do documento ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-158">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |
| [<span data-ttu-id="099eb-159">DlpNotifyPreOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="099eb-159">DlpNotifyPreOpenDocumentFile</span></span>](endpointdlp-dlpnotifypreopendocumentfile.md)                         | <span data-ttu-id="099eb-160">Fornece ao sistema informações sobre um documento antes que a operação de abertura seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-160">Provides the system with information about a document before the open operation is initiated.</span></span>  |
| [<span data-ttu-id="099eb-161">DlpNotifyPostOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="099eb-161">DlpNotifyPostOpenDocumentFile</span></span>](endpointdlp-dlpnotifypostopendocumentfile.md)                       | <span data-ttu-id="099eb-162">Fornece ao sistema informações sobre um documento após a conclusão da operação de abertura.</span><span class="sxs-lookup"><span data-stu-id="099eb-162">Provides the system with information about a document after the open operation is completed.</span></span>                                  |
| [<span data-ttu-id="099eb-163">DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="099eb-163">DlpNotifyCloseDocumentFile</span></span>](endpointdlp-dlpnotifyclosedocumentfile.md)                       | <span data-ttu-id="099eb-164">Fornece ao sistema informações sobre um documento antes da operação de fechamento do documento ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-164">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |

### <a name="save-as-operations"></a><span data-ttu-id="099eb-165">Salvar como operações</span><span class="sxs-lookup"><span data-stu-id="099eb-165">Save as operations</span></span>
| <span data-ttu-id="099eb-166">API</span><span class="sxs-lookup"><span data-stu-id="099eb-166">API</span></span> | <span data-ttu-id="099eb-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="099eb-167">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="099eb-168">DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="099eb-168">DlpNotifyPreSaveAsDocument</span></span>](endpointdlp-dlpnotifypresaveasdocument.md)                       | <span data-ttu-id="099eb-169">Fornece ao sistema informações sobre um documento antes de uma operação salvar como ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-169">Provides the system with information about a document before a save as operation is initiated.</span></span>                                  |
| [<span data-ttu-id="099eb-170">DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="099eb-170">DlpNotifyPostSaveAsDocument</span></span>](endpointdlp-dlpnotifypostsaveasdocument.md)                       | <span data-ttu-id="099eb-171">Fornece ao sistema informações sobre um documento após a conclusão da operação salvar como.</span><span class="sxs-lookup"><span data-stu-id="099eb-171">Provides the system with information about a document after the save as operation is completed.</span></span>                                  |


### <a name="drag-and-drop-operations"></a><span data-ttu-id="099eb-172">Operações de arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="099eb-172">Drag and drop operations</span></span>

| <span data-ttu-id="099eb-173">API</span><span class="sxs-lookup"><span data-stu-id="099eb-173">API</span></span> | <span data-ttu-id="099eb-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="099eb-174">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="099eb-175">DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="099eb-175">DlpNotifyEnterDropTarget</span></span>](endpointdlp-dlpnotifyenterdroptarget.md)                       | <span data-ttu-id="099eb-176">Fornece ao sistema informações sobre um documento quando um destino de soltar é inserido.</span><span class="sxs-lookup"><span data-stu-id="099eb-176">Provides the system with information about a document when a drop target is entered.</span></span>                                  |
| [<span data-ttu-id="099eb-177">DlpNotifyLeaveDropTarget</span><span class="sxs-lookup"><span data-stu-id="099eb-177">DlpNotifyLeaveDropTarget</span></span>](endpointdlp-dlpnotifyleavedroptarget.md)                       | <span data-ttu-id="099eb-178">Fornece ao sistema informações sobre um documento quando um destino de soltar é encerrado.</span><span class="sxs-lookup"><span data-stu-id="099eb-178">Provides the system with information about a document when a drop target is exited.</span></span>                                  |
| [<span data-ttu-id="099eb-179">DlpNotifyPreDragDrop</span><span class="sxs-lookup"><span data-stu-id="099eb-179">DlpNotifyPreDragDrop</span></span>](endpointdlp-dlpnotifypredragdrop.md)                         | <span data-ttu-id="099eb-180">Fornece ao sistema informações sobre um documento antes de uma operação arrastar e soltar ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-180">Provides the system with information about a document before a drag drop operation is initiated.</span></span>  |
| [<span data-ttu-id="099eb-181">DlpNotifyPostDragDrop</span><span class="sxs-lookup"><span data-stu-id="099eb-181">DlpNotifyPostDragDrop</span></span>](endpointdlp-dlpnotifypostdragdrop.md)                         | <span data-ttu-id="099eb-182">Fornece ao sistema informações sobre um documento após a conclusão de uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="099eb-182">Provides the system with information about a document after a drag drop operation is completed.</span></span>  |


### <a name="clipboard-operations"></a><span data-ttu-id="099eb-183">opções de Área de Transferência</span><span class="sxs-lookup"><span data-stu-id="099eb-183">Clipboard operations</span></span>

| <span data-ttu-id="099eb-184">API</span><span class="sxs-lookup"><span data-stu-id="099eb-184">API</span></span> | <span data-ttu-id="099eb-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="099eb-185">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="099eb-186">DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="099eb-186">DlpNotifyPreCopyToClipboard</span></span>](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | <span data-ttu-id="099eb-187">Fornece ao sistema informações sobre um documento antes de uma operação de cópia para a área de transferência ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-187">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="099eb-188">DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="099eb-188">DlpNotifyPostCopyToClipboard</span></span>](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | <span data-ttu-id="099eb-189">Fornece ao sistema informações sobre um documento após a conclusão de uma operação de cópia para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="099eb-189">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>  |
| [<span data-ttu-id="099eb-190">DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="099eb-190">DlpNotifyPrePasteFromClipboard</span></span>](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | <span data-ttu-id="099eb-191">Fornece ao sistema informações sobre um documento antes de uma operação colar da área de transferência ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-191">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="099eb-192">DlpNotifyPostPasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="099eb-192">DlpNotifyPostPasteFromClipboard</span></span>](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | <span data-ttu-id="099eb-193">Fornece ao sistema informações sobre um documento após a conclusão de uma operação colar da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="099eb-193">Provides the system with information about a document after a paste from clipboard operation has completed.</span></span>                                  |
| [<span data-ttu-id="099eb-194">DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="099eb-194">DlpNotifyPostStashClipboard</span></span>](endpointdlp-dlpnotifypoststashclipboard.md)                       | <span data-ttu-id="099eb-195">Fornece o sistema com informações de status após a conclusão de uma operação de área de transferência de stash.</span><span class="sxs-lookup"><span data-stu-id="099eb-195">Provides the system with status information after a stash clipboard operation is completed.</span></span>                                  |
| [<span data-ttu-id="099eb-196">DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="099eb-196">DlpNotifyPreStashClipboard</span></span>](endpointdlp-dlpnotifyprestashclipboard.md)                       | <span data-ttu-id="099eb-197">Notifica o sistema antes que uma operação de área de transferência de stash seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-197">Notifies the system before a stash clipboard operation is initiated.</span></span>                                  |
| [<span data-ttu-id="099eb-198">DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="099eb-198">DlpMustPasteFromSystemClipboard</span></span>](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | <span data-ttu-id="099eb-199">Determina se o aplicativo deve extrair os dados da área de transferência do sistema em vez de retirá-los de seu cache interno.</span><span class="sxs-lookup"><span data-stu-id="099eb-199">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>                                  |

### <a name="print-operations"></a><span data-ttu-id="099eb-200">Operações de impressão</span><span class="sxs-lookup"><span data-stu-id="099eb-200">Print operations</span></span>

| <span data-ttu-id="099eb-201">API</span><span class="sxs-lookup"><span data-stu-id="099eb-201">API</span></span> | <span data-ttu-id="099eb-202">Descrição</span><span class="sxs-lookup"><span data-stu-id="099eb-202">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="099eb-203">DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="099eb-203">DlpNotifyPrePrint</span></span>](endpointdlp-dlpnotifypreprint.md)                         | <span data-ttu-id="099eb-204">Fornece ao sistema informações sobre um documento antes de uma operação de impressão ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="099eb-204">Provides the system with information about a document before a print operation is initiated.</span></span>  |
| [<span data-ttu-id="099eb-205">DlpNotifyPostStartPrint</span><span class="sxs-lookup"><span data-stu-id="099eb-205">DlpNotifyPostStartPrint</span></span>](endpointdlp-dlpnotifypoststartprint.md)                       | <span data-ttu-id="099eb-206">Fornece ao sistema informações sobre um documento após o início de uma operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="099eb-206">Provides the system with information about a document after an print operation has started.</span></span>                                  |
| [<span data-ttu-id="099eb-207">DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="099eb-207">DlpNotifyPostPrint</span></span>](endpointdlp-dlpnotifypostprint.md)                       | <span data-ttu-id="099eb-208">Fornece ao sistema informações sobre um documento após a conclusão de uma operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="099eb-208">Provides the system with information about a document after a print operation has completed.</span></span>                                  |

## <a name="endpoint-dlp-example-header"></a><span data-ttu-id="099eb-209">Cabeçalho de exemplo do Endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="099eb-209">Endpoint DLP example header</span></span>

<span data-ttu-id="099eb-210">Como o cabeçalho de DLP do ponto de extremidade não está incluído no SDK do Windows, você deve criar o arquivo de cabeçalho por conta própria para obter assinaturas de API para usar em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="099eb-210">Because the endpoint DLP header is not included in the Windows SDK, you must create the header file yourself to get API signatures to use in your implementation.</span></span> <span data-ttu-id="099eb-211">Para sua conveniência, estamos fornecendo um código de exemplo que você pode copiar e colar em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="099eb-211">For your convenience we're providing example code that you can copy and paste into your application.</span></span> <span data-ttu-id="099eb-212">Além das declarações de função, essa listagem de código também define constantes úteis, como informações de controle de versão e caminhos de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="099eb-212">In addition to function declarations, this code listing also defines useful constants such as versioning information and registry key paths.</span></span>

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


```


