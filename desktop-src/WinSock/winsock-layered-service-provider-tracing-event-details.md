---
description: Detalhes de rastreamento de alteração do catálogo Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Detalhes de rastreamento de alteração do catálogo Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090998"
---
# <a name="winsock-catalog-change-tracing-details"></a><span data-ttu-id="cee80-103">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="cee80-103">Winsock Catalog Change Tracing Details</span></span>

> [!Note]  
> <span data-ttu-id="cee80-104">Os provedores de serviço em camadas são preteridos.</span><span class="sxs-lookup"><span data-stu-id="cee80-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="cee80-105">A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="cee80-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="cee80-106">O rastreamento de eventos de alteração do catálogo Winsock para provedores de serviço em camadas (LSPs) está relacionado à instalação de LSP, remoção de LSP, desabilitação de LSP e operações de redefinição de catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="cee80-106">Winsock Catalog Change event tracing for layered Service providers (LSPs) is related to LSP installation, LSP removal, LSP disable, and Winsock catalog reset operations.</span></span> <span data-ttu-id="cee80-107">Todos os eventos a seguir são gravados no canal *Microsoft-Windows-Winsock-WS2HELP/Operational* que é diferente do outro rastreamento de eventos de rede do Winsock registrado no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="cee80-107">All of the following events are written to the *Microsoft-Windows-Winsock-WS2HELP/Operational* channel which is different from the other Winsock network event tracing logged on Windows Vista and later.</span></span>

<span data-ttu-id="cee80-108">Os detalhes a seguir são cada um dos eventos LSP Winsock que podem ser rastreados e descreve quais parâmetros e informações são registrados.</span><span class="sxs-lookup"><span data-stu-id="cee80-108">The following details each of the Winsock LSP events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="lsp-install"></a><span data-ttu-id="cee80-109">Instalação de LSP</span><span class="sxs-lookup"><span data-stu-id="cee80-109">LSP Install</span></span>

<span data-ttu-id="cee80-110">ID do evento = 1</span><span class="sxs-lookup"><span data-stu-id="cee80-110">Event ID = 1</span></span>

<span data-ttu-id="cee80-111">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="cee80-111">Level = 4 (Information)</span></span>

<span data-ttu-id="cee80-112">Os seguintes eventos de LSP do Winsock são rastreados para uma operação de instalação de LSP:</span><span class="sxs-lookup"><span data-stu-id="cee80-112">The following Winsock LSP events are traced for an LSP install operation:</span></span>

-   <span data-ttu-id="cee80-113">Uma entrada de protocolo é instalada no catálogo do Winsock.</span><span class="sxs-lookup"><span data-stu-id="cee80-113">A protocol entry is installed into the Winsock catalog.</span></span>

<span data-ttu-id="cee80-114">Os seguintes parâmetros são registrados em log para um evento de instalação de LSP:</span><span class="sxs-lookup"><span data-stu-id="cee80-114">The following parameters are logged for a LSP install event:</span></span>



| <span data-ttu-id="cee80-115">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="cee80-115">Parameter</span></span>                                                                                                | <span data-ttu-id="cee80-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="cee80-116">Description</span></span>                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee80-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome do LSP</span><span class="sxs-lookup"><span data-stu-id="cee80-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="cee80-118">O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="cee80-118">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/> |
| <span data-ttu-id="cee80-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span><span class="sxs-lookup"><span data-stu-id="cee80-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="cee80-120">O catálogo do Winsock (32 bits ou 64 bits) em que o LSP está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="cee80-120">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="cee80-121">Este é um valor inteiro que é 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="cee80-121">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="cee80-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador</span><span class="sxs-lookup"><span data-stu-id="cee80-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="cee80-123">O nome de arquivo do módulo do aplicativo que faz a chamada de instalação de LSP.</span><span class="sxs-lookup"><span data-stu-id="cee80-123">The module filename of the application making the LSP install call.</span></span><br/>                                                                                          |
| <span data-ttu-id="cee80-124"><span id="GUID"></span><span id="guid"></span>VOLUME</span><span class="sxs-lookup"><span data-stu-id="cee80-124"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="cee80-125">O valor de GUID do provedor de transporte do Winsock no qual o LSP está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="cee80-125">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span><br/>                                                                      |
| <span data-ttu-id="cee80-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias</span><span class="sxs-lookup"><span data-stu-id="cee80-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="cee80-127">O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="cee80-127">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/>                                |



 

## <a name="lsp-uninstall"></a><span data-ttu-id="cee80-128">Desinstalação de LSP</span><span class="sxs-lookup"><span data-stu-id="cee80-128">LSP Uninstall</span></span>

<span data-ttu-id="cee80-129">ID do evento = 2</span><span class="sxs-lookup"><span data-stu-id="cee80-129">Event ID = 2</span></span>

<span data-ttu-id="cee80-130">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="cee80-130">Level = 4 (Information)</span></span>

<span data-ttu-id="cee80-131">Os seguintes eventos de LSP do Winsock são rastreados para uma operação de desinstalação de LSP:</span><span class="sxs-lookup"><span data-stu-id="cee80-131">The following Winsock LSP events are traced for an LSP uninstall operation:</span></span>

-   <span data-ttu-id="cee80-132">Uma entrada de protocolo é removida do catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="cee80-132">A protocol entry is removed from the Winsock catalog.</span></span>

<span data-ttu-id="cee80-133">Os seguintes parâmetros são registrados em log para um evento de desinstalação de LSP:</span><span class="sxs-lookup"><span data-stu-id="cee80-133">The following parameters are logged for a LSP uninstall event:</span></span>



| <span data-ttu-id="cee80-134">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="cee80-134">Parameter</span></span>                                                                                                | <span data-ttu-id="cee80-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="cee80-135">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee80-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome do LSP</span><span class="sxs-lookup"><span data-stu-id="cee80-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="cee80-137">O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="cee80-137">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/> |
| <span data-ttu-id="cee80-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span><span class="sxs-lookup"><span data-stu-id="cee80-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="cee80-139">O catálogo Winsock (32 bits ou 64 bits) em que o LSP está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="cee80-139">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="cee80-140">Este é um valor inteiro que é 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="cee80-140">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="cee80-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador</span><span class="sxs-lookup"><span data-stu-id="cee80-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="cee80-142">O nome de arquivo do módulo do aplicativo que faz a chamada de remoção de LSP.</span><span class="sxs-lookup"><span data-stu-id="cee80-142">The module filename of the application making the LSP remove call.</span></span><br/>                                                                                         |
| <span data-ttu-id="cee80-143"><span id="GUID"></span><span id="guid"></span>VOLUME</span><span class="sxs-lookup"><span data-stu-id="cee80-143"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="cee80-144">O valor de GUID do provedor de transporte do Winsock do qual o LSP foi removido.</span><span class="sxs-lookup"><span data-stu-id="cee80-144">The GUID value of the Winsock transport provider that the LSP is removed from.</span></span><br/>                                                                             |
| <span data-ttu-id="cee80-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias</span><span class="sxs-lookup"><span data-stu-id="cee80-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="cee80-146">O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="cee80-146">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/>                                |



 

## <a name="lsp-disable"></a><span data-ttu-id="cee80-147">Desabilitação de LSP</span><span class="sxs-lookup"><span data-stu-id="cee80-147">LSP Disable</span></span>

<span data-ttu-id="cee80-148">ID do evento = 3</span><span class="sxs-lookup"><span data-stu-id="cee80-148">Event ID = 3</span></span>

<span data-ttu-id="cee80-149">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="cee80-149">Level = 4 (Information)</span></span>

<span data-ttu-id="cee80-150">Os seguintes eventos de LSP do Winsock são rastreados para uma operação de desabilitação de LSP:</span><span class="sxs-lookup"><span data-stu-id="cee80-150">The following Winsock LSP events are traced for an LSP disable operation:</span></span>

-   <span data-ttu-id="cee80-151">Uma entrada de protocolo está desabilitada no catálogo do Winsock.</span><span class="sxs-lookup"><span data-stu-id="cee80-151">A protocol entry is disabled in the Winsock catalog.</span></span>

<span data-ttu-id="cee80-152">Os seguintes parâmetros são registrados em log para um evento de desabilitação de LSP:</span><span class="sxs-lookup"><span data-stu-id="cee80-152">The following parameters are logged for a LSP disable event:</span></span>



| <span data-ttu-id="cee80-153">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="cee80-153">Parameter</span></span>                                                                                                | <span data-ttu-id="cee80-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="cee80-154">Description</span></span>                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee80-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome do LSP</span><span class="sxs-lookup"><span data-stu-id="cee80-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="cee80-156">O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="cee80-156">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/> |
| <span data-ttu-id="cee80-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span><span class="sxs-lookup"><span data-stu-id="cee80-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="cee80-158">O catálogo Winsock (32 bits ou 64 bits) em que o LSP está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="cee80-158">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="cee80-159">Este é um valor inteiro que é 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="cee80-159">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="cee80-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador</span><span class="sxs-lookup"><span data-stu-id="cee80-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="cee80-161">O nome de arquivo do módulo do aplicativo que faz a chamada de desabilitação de LSP.</span><span class="sxs-lookup"><span data-stu-id="cee80-161">The module filename of the application making the LSP disable call.</span></span><br/>                                                                                         |
| <span data-ttu-id="cee80-162"><span id="GUID"></span><span id="guid"></span>VOLUME</span><span class="sxs-lookup"><span data-stu-id="cee80-162"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="cee80-163">O valor de GUID do provedor de transporte do Winsock em que o LSP está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="cee80-163">The GUID value of the Winsock transport provider where the LSP is being disabled.</span></span><br/>                                                                           |
| <span data-ttu-id="cee80-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias</span><span class="sxs-lookup"><span data-stu-id="cee80-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="cee80-165">O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.</span><span class="sxs-lookup"><span data-stu-id="cee80-165">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/>                                |



 

## <a name="winsock-catalog-reset"></a><span data-ttu-id="cee80-166">Redefinição de catálogo do Winsock</span><span class="sxs-lookup"><span data-stu-id="cee80-166">Winsock Catalog Reset</span></span>

<span data-ttu-id="cee80-167">ID do evento = 4</span><span class="sxs-lookup"><span data-stu-id="cee80-167">Event ID = 4</span></span>

<span data-ttu-id="cee80-168">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="cee80-168">Level = 4 (Information)</span></span>

<span data-ttu-id="cee80-169">Os seguintes eventos de LSP do Winsock são rastreados para uma operação de redefinição de catálogo do Winsock:</span><span class="sxs-lookup"><span data-stu-id="cee80-169">The following Winsock LSP events are traced for a Winsock catalog reset operation:</span></span>

-   <span data-ttu-id="cee80-170">O catálogo do Winsock é redefinido.</span><span class="sxs-lookup"><span data-stu-id="cee80-170">The Winsock catalog is reset.</span></span>

<span data-ttu-id="cee80-171">Os seguintes parâmetros são registrados em log para um evento de redefinição de catálogo do Winsock:</span><span class="sxs-lookup"><span data-stu-id="cee80-171">The following parameters are logged for a Winsock catalog reset event:</span></span>



| <span data-ttu-id="cee80-172">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="cee80-172">Parameter</span></span>                                                                                        | <span data-ttu-id="cee80-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="cee80-173">Description</span></span>                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee80-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span><span class="sxs-lookup"><span data-stu-id="cee80-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/> | <span data-ttu-id="cee80-175">O catálogo do Winsock (32 bits ou 64 bits) que está sendo redefinido.</span><span class="sxs-lookup"><span data-stu-id="cee80-175">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="cee80-176">Este é um valor inteiro que é 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="cee80-176">This is an integer value that is either 32 or 64.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="cee80-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cee80-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee80-178">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="cee80-178">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="cee80-179">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="cee80-179">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="cee80-180">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="cee80-180">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="cee80-181">Detalhes de rastreamento de eventos de rede do Winsock</span><span class="sxs-lookup"><span data-stu-id="cee80-181">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
