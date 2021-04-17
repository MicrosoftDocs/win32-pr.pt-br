---
description: A API do WUA (agente de Windows Update) pode ser usada por um usuário em um computador remoto ou por um aplicativo em execução em um computador remoto. No entanto, o usuário ou aplicativo remoto deve ter privilégios de administrador.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Usando o WUA de um computador remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764026"
---
# <a name="using-wua-from-a-remote-computer"></a><span data-ttu-id="6bcc7-104">Usando o WUA de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="6bcc7-104">Using WUA From a Remote Computer</span></span>

<span data-ttu-id="6bcc7-105">A API do WUA (agente de Windows Update) pode ser usada por um usuário em um computador remoto ou por um aplicativo em execução em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="6bcc7-105">The Windows Update Agent (WUA) API can be used by a user on a remote computer or by an application that is running on a remote computer.</span></span> <span data-ttu-id="6bcc7-106">No entanto, o usuário ou aplicativo remoto deve ter privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="6bcc7-106">However, the remote user or application must have administrator privileges.</span></span>

<span data-ttu-id="6bcc7-107">A lista a seguir contém interfaces que estão disponíveis para usuários e aplicativos remotos:</span><span class="sxs-lookup"><span data-stu-id="6bcc7-107">The following list contains interfaces that are available to remote users and applications:</span></span>

-   [<span data-ttu-id="6bcc7-108">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-108">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [<span data-ttu-id="6bcc7-109">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-109">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="6bcc7-110">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-110">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [<span data-ttu-id="6bcc7-111">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-111">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="6bcc7-112">**ISearchResult**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-112">**ISearchResult**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [<span data-ttu-id="6bcc7-113">**IUpdateCollection**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-113">**IUpdateCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [<span data-ttu-id="6bcc7-114">**IUpdate**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-114">**IUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [<span data-ttu-id="6bcc7-115">**IUpdate2**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-115">**IUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [<span data-ttu-id="6bcc7-116">**IWindowsDriverUpdate**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-116">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [<span data-ttu-id="6bcc7-117">**IWindowsDriverUpdate2**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-117">**IWindowsDriverUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [<span data-ttu-id="6bcc7-118">**IUpdateIdentity**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-118">**IUpdateIdentity**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [<span data-ttu-id="6bcc7-119">**IImageInformation**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-119">**IImageInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [<span data-ttu-id="6bcc7-120">**IInstallationBehavior**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-120">**IInstallationBehavior**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [<span data-ttu-id="6bcc7-121">**Isastringcollection**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-121">**IStringCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [<span data-ttu-id="6bcc7-122">**IUpdateHistoryEntryCollection**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-122">**IUpdateHistoryEntryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [<span data-ttu-id="6bcc7-123">**IUpdateHistoryEntry**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-123">**IUpdateHistoryEntry**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [<span data-ttu-id="6bcc7-124">**ICategoryCollection**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-124">**ICategoryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [<span data-ttu-id="6bcc7-125">**ICategory**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-125">**ICategory**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [<span data-ttu-id="6bcc7-126">**IUpdateExceptionCollection**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-126">**IUpdateExceptionCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [<span data-ttu-id="6bcc7-127">**IUpdateException**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-127">**IUpdateException**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [<span data-ttu-id="6bcc7-128">**IUpdateDownloadContentCollection**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-128">**IUpdateDownloadContentCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [<span data-ttu-id="6bcc7-129">**IUpdateDownloadContent**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-129">**IUpdateDownloadContent**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [<span data-ttu-id="6bcc7-130">**IUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-130">**IUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [<span data-ttu-id="6bcc7-131">**IUpdateServiceCollection**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-131">**IUpdateServiceCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [<span data-ttu-id="6bcc7-132">**IUpdateService**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-132">**IUpdateService**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [<span data-ttu-id="6bcc7-133">**IWindowsUpdateAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-133">**IWindowsUpdateAgentInfo**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

<span data-ttu-id="6bcc7-134">A lista a seguir contém interfaces e propriedades que não estão disponíveis para usuários e aplicativos remotos:</span><span class="sxs-lookup"><span data-stu-id="6bcc7-134">The following list contains interfaces and properties that are not available to remote users and applications:</span></span>

-   [<span data-ttu-id="6bcc7-135">**IUpdateSession::CreateUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-135">**IUpdateSession::CreateUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [<span data-ttu-id="6bcc7-136">**IUpdateSession::CreateUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-136">**IUpdateSession::CreateUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [<span data-ttu-id="6bcc7-137">**Propriedade WebProxy de IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-137">**WebProxy Property of IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [<span data-ttu-id="6bcc7-138">**IUpdateSearcher::BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-138">**IUpdateSearcher::BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [<span data-ttu-id="6bcc7-139">**IUpdateSearcher:: endsearch**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-139">**IUpdateSearcher::EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   <span data-ttu-id="6bcc7-140">A [**Propriedade IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** é somente leitura quando é chamada remotamente.)</span><span class="sxs-lookup"><span data-stu-id="6bcc7-140">[**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** is read-only when it is called remotely.)</span></span>
-   [<span data-ttu-id="6bcc7-141">**IUpdate:: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-141">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [<span data-ttu-id="6bcc7-142">**IUpdate::CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-142">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="6bcc7-143">**IUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-143">**IUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [<span data-ttu-id="6bcc7-144">**IWindowsDriverUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-144">**IWindowsDriverUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [<span data-ttu-id="6bcc7-145">**IUpdateServiceManager:: AddService**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-145">**IUpdateServiceManager::AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [<span data-ttu-id="6bcc7-146">**IUpdateServiceManager::RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-146">**IUpdateServiceManager::RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [<span data-ttu-id="6bcc7-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [<span data-ttu-id="6bcc7-148">**IAutomaticUpdate::P ause**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-148">**IAutomaticUpdate::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="6bcc7-149">**IAutomaticUpdates:: retomar**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-149">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="6bcc7-150">**IAutomaticUpdates::ShowSettingsDialog**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-150">**IAutomaticUpdates::ShowSettingsDialog**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [<span data-ttu-id="6bcc7-151">**Propriedade Settings de IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-151">**Settings Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [<span data-ttu-id="6bcc7-152">**Propriedade não habilitada de IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-152">**ServiceEnabled Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [<span data-ttu-id="6bcc7-153">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-153">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="6bcc7-154">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="6bcc7-154">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

<span data-ttu-id="6bcc7-155">As seguintes portas e exceções devem ser adicionadas às configurações do firewall do Windows para Windows Vista e Windows Server 2008 para que a API do WUA seja chamada remotamente.</span><span class="sxs-lookup"><span data-stu-id="6bcc7-155">The following ports and exceptions must be added to the Windows firewall settings for Windows Vista and Windows Server 2008 for the WUA API to be called remotely.</span></span>

<dl> <dt>

<span data-ttu-id="6bcc7-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exceção 1</span><span class="sxs-lookup"><span data-stu-id="6bcc7-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exception 1</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="6bcc7-157">Porta local: 135</span><span class="sxs-lookup"><span data-stu-id="6bcc7-157">Local port: 135</span></span></dd> <dd><span data-ttu-id="6bcc7-158">Porta remota: todas</span><span class="sxs-lookup"><span data-stu-id="6bcc7-158">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="6bcc7-159">Número do protocolo: 6</span><span class="sxs-lookup"><span data-stu-id="6bcc7-159">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="6bcc7-160">Executável:% WINDIR% \\ system32 \\svchost.exe</span><span class="sxs-lookup"><span data-stu-id="6bcc7-160">Executable: %windir%\\system32\\svchost.exe</span></span></dd> <dd><span data-ttu-id="6bcc7-161">Serviço: RPCSS</span><span class="sxs-lookup"><span data-stu-id="6bcc7-161">Service: rpcss</span></span></dd> <dd><span data-ttu-id="6bcc7-162">Privilégio remoto: administrador</span><span class="sxs-lookup"><span data-stu-id="6bcc7-162">Remote privilege: Administrator</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="6bcc7-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exceção 2</span><span class="sxs-lookup"><span data-stu-id="6bcc7-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exception 2</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="6bcc7-164">Porta local: RPC dinâmico</span><span class="sxs-lookup"><span data-stu-id="6bcc7-164">Local port: Dynamic RPC</span></span></dd> <dd><span data-ttu-id="6bcc7-165">Porta remota: todas</span><span class="sxs-lookup"><span data-stu-id="6bcc7-165">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="6bcc7-166">Número do protocolo: 6</span><span class="sxs-lookup"><span data-stu-id="6bcc7-166">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="6bcc7-167">Executável:% WINDIR% \\ system32 \\dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="6bcc7-167">Executable: %windir%\\system32\\dllhost.exe</span></span></dd> <dd><span data-ttu-id="6bcc7-168">Privilégio remoto: administrador</span><span class="sxs-lookup"><span data-stu-id="6bcc7-168">Remote privilege: Administrator</span></span></dd> </dl> </dd> </dl>

<span data-ttu-id="6bcc7-169">A lista a seguir contém ferramentas que podem ser usadas para definir as configurações do firewall do Windows:</span><span class="sxs-lookup"><span data-stu-id="6bcc7-169">The following list contains tools that can be used to configure Windows Firewall settings:</span></span>

-   <span data-ttu-id="6bcc7-170">Firewall do Windows com o snap-in de segurança avançada</span><span class="sxs-lookup"><span data-stu-id="6bcc7-170">Windows Firewall with Advanced Security snap-in</span></span>
-   <span data-ttu-id="6bcc7-171">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="6bcc7-171">Group Policy</span></span>
-   <span data-ttu-id="6bcc7-172">Ferramenta de linha de comando netsh advfirewall</span><span class="sxs-lookup"><span data-stu-id="6bcc7-172">Netsh advfirewall command-line tool</span></span>

<span data-ttu-id="6bcc7-173">Para obter mais informações sobre como usar as ferramentas para definir as configurações do firewall do Windows, consulte [introdução com o Firewall do Windows com segurança avançada](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="6bcc7-173">For more information about how to use tools to configure Windows Firewall settings, see [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span></span>

 

 
