---
description: a API do WUA (agente de Windows Update) pode ser usada por um usuário em um computador remoto ou por um aplicativo em execução em um computador remoto. No entanto, o usuário ou aplicativo remoto deve ter privilégios de administrador.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Usando o WUA de um computador remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a3780099f6ff9707893c9f7b5d5f2f18be1f6a97c33d9133fef4d5d3497087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737775"
---
# <a name="using-wua-from-a-remote-computer"></a>Usando o WUA de um computador remoto

a API do WUA (agente de Windows Update) pode ser usada por um usuário em um computador remoto ou por um aplicativo em execução em um computador remoto. No entanto, o usuário ou aplicativo remoto deve ter privilégios de administrador.

A lista a seguir contém interfaces que estão disponíveis para usuários e aplicativos remotos:

-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**ISearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [**IUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [**IUpdateIdentity**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [**IImageInformation**](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [**Isastringcollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [**ICategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [**ICategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [**IUpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [**IUpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [**IUpdateDownloadContentCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [**IUpdateDownloadContent**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [**IUpdateServiceCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

A lista a seguir contém interfaces e propriedades que não estão disponíveis para usuários e aplicativos remotos:

-   [**IUpdateSession::CreateUpdateDownloader**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [**IUpdateSession::CreateUpdateInstaller**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [**Propriedade WebProxy de IUpdateSession**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [**IUpdateSearcher:: endsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   A [**Propriedade IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** é somente leitura quando é chamada remotamente.)
-   [**IUpdate:: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [**IUpdate::CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IUpdate2::CopyToCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [**IWindowsDriverUpdate2::CopyToCache**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [**IUpdateServiceManager:: AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [**IUpdateServiceManager::RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [**IUpdateServiceManager::UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [**IAutomaticUpdate::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates:: retomar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::ShowSettingsDialog**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [**Configurações Propriedade de IAutomaticUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [**Propriedade não habilitada de IAutomaticUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

as seguintes portas e exceções devem ser adicionadas às configurações de firewall Windows para Windows Vista e Windows Server 2008 para que a API do WUA seja chamada remotamente.

<dl> <dt>

<span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exceção 1
</dt> <dd> <dl> <dd>Porta local: 135</dd> <dd>Porta remota: todas</dd> <dd>Número do protocolo: 6</dd> <dd>Executável:% WINDIR% \\ system32 \\svchost.exe</dd> <dd>Serviço: RPCSS</dd> <dd>Privilégio remoto: administrador</dd> </dl> </dd> <dt>

<span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exceção 2
</dt> <dd> <dl> <dd>Porta local: RPC dinâmico</dd> <dd>Porta remota: todas</dd> <dd>Número do protocolo: 6</dd> <dd>Executável:% WINDIR% \\ system32 \\dllhost.exe</dd> <dd>Privilégio remoto: administrador</dd> </dl> </dd> </dl>

a lista a seguir contém ferramentas que podem ser usadas para definir Windows configurações de Firewall:

-   Firewall do Windows com o snap-in de segurança avançada
-   Política de Grupo
-   Ferramenta de linha de comando netsh advfirewall

para obter mais informações sobre como usar as ferramentas para definir Windows configurações de firewall, consulte [Introdução com o firewall do Windows com segurança avançada](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).

 

 
