---
description: Proteção de Recursos do Windows adicionais em chaves do registro
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Proteção de Recursos do Windows adicionais em chaves do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1beeea49f06da182b5ebba38d09227134a6d92c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088774"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a><span data-ttu-id="a9135-103">Proteção de Recursos do Windows adicionais em chaves do registro</span><span class="sxs-lookup"><span data-stu-id="a9135-103">Additional Windows Resource Protection on Registry Keys</span></span>

## <a name="platform"></a><span data-ttu-id="a9135-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="a9135-104">Platform</span></span>

<span data-ttu-id="a9135-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9135-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="a9135-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9135-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="a9135-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="a9135-107">Feature Impact</span></span>

<span data-ttu-id="a9135-108">**Severidade** -média</span><span class="sxs-lookup"><span data-stu-id="a9135-108">**Severity** - Medium</span></span>  
<span data-ttu-id="a9135-109">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="a9135-109">**Frequency** - Low</span></span>  


## <a name="description"></a><span data-ttu-id="a9135-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9135-110">Description</span></span>

<span data-ttu-id="a9135-111">Recursos adicionais do sistema adicionam configurações de Proteção de Recursos do Windows (WRP) no Windows 7, tornando-as configurações somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a9135-111">Additional system resources have added Windows Resource Protection (WRP) settings in Windows 7, making them read-only settings.</span></span> <span data-ttu-id="a9135-112">A grande maioria dos recursos que receberam proteção adicional são as chaves de servidor COM do sistema, embora alguns recursos tenham adicionado a proteção de recursos direcionada.</span><span class="sxs-lookup"><span data-stu-id="a9135-112">The vast majority of resources that received added protection are system COM server keys, although some features have added targeted resource protection.</span></span> <span data-ttu-id="a9135-113">A Microsoft alterou esses recursos para proteger o sistema e outros aplicativos de dividir uns aos outros e fornecer uma plataforma estável e consistente na qual os aplicativos podem ser executados de forma confiável.</span><span class="sxs-lookup"><span data-stu-id="a9135-113">Microsoft changed these resources in order to protect the system and other applications from breaking each other and to provide a consistent, stable platform upon which applications can reliably run.</span></span> <span data-ttu-id="a9135-114">No passado, os aplicativos podiam fornecer arquivos personalizados e usar o registro COM desprotegido para alterar o sistema.</span><span class="sxs-lookup"><span data-stu-id="a9135-114">In the past, applications could provide custom files and use the unprotected COM registration to change the system.</span></span> <span data-ttu-id="a9135-115">No caso de aplicativos mais antigos, isso pode fazer o downgrade de tempos de execução do sistema ou alterar a interface na qual outros aplicativos precisavam funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="a9135-115">In the case of older applications, this can downgrade system runtimes or change the interface upon which other applications needed to work properly.</span></span> <span data-ttu-id="a9135-116">Na pior das hipóteses, essas instalações poderiam causar falha ou degradação do sistema ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="a9135-116">In the worst case, such installations could cause system failure or degradation over time.</span></span> <span data-ttu-id="a9135-117">Para fornecer uma experiência melhor e uma plataforma de aplicativo mais estável, bloqueamos esses registros para que apenas as atualizações da Microsoft pudessem alterar os componentes do sistema.</span><span class="sxs-lookup"><span data-stu-id="a9135-117">To provide a better experience and a more stable application platform, we locked down these registrations so that only Microsoft updates could change system components.</span></span>

<span data-ttu-id="a9135-118">Como a maioria dos recursos alterados são chaves COM usadas pelo sistema, essa alteração não afetará a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a9135-118">Since most resources changed are COM keys used by the system, this change will not affect the majority of applications.</span></span> <span data-ttu-id="a9135-119">Embora esperamos que a maioria dos aplicativos tenha uma experiência melhor no Windows 7 como resultado dessas alterações, um pequeno subconjunto de aplicativos pode ser afetado negativamente.</span><span class="sxs-lookup"><span data-stu-id="a9135-119">While we expect most applications to have a better experience on Windows 7 as a result of these changes, a small subset of applications may be negatively affected.</span></span> <span data-ttu-id="a9135-120">As camadas de compatibilidade de aplicativos do sistema resolverão automaticamente os problemas de instalação, sempre informando ao aplicativo que ele teve êxito na alteração de uma configuração, mesmo que ela tenha falhado devido a um recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="a9135-120">The system's application compatibility layers will automatically resolve setup problems by always telling the application that it succeeded in changing a setting, even if it failed due to it being a protected resource.</span></span> <span data-ttu-id="a9135-121">Isso impede que as configurações de aplicativo sejam interrompidas, mas podem causar problemas se a configuração precisar ser alterada para que o aplicativo funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="a9135-121">This prevents application setups from breaking but may cause problems if the setting needed to be changed in order for the application to function properly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a9135-122">Manifestação</span><span class="sxs-lookup"><span data-stu-id="a9135-122">Manifestation</span></span>

<span data-ttu-id="a9135-123">Os aplicativos podem ter modificado essas configurações antes do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a9135-123">Applications may have modified these settings prior to Windows 7.</span></span> <span data-ttu-id="a9135-124">Ao instalar no Windows 7, os aplicativos podem encontrar determinados recursos que não funcionam mais porque as configurações não refletiram o que o aplicativo esperava.</span><span class="sxs-lookup"><span data-stu-id="a9135-124">Upon installing on Windows 7, applications may find certain features no longer work because the settings did not reflect what the application expected.</span></span>

<span data-ttu-id="a9135-125">Há dois cenários em que os aplicativos podem encontrar problemas relacionados a essa proteção adicional:</span><span class="sxs-lookup"><span data-stu-id="a9135-125">There are two scenarios in which applications may encounter problems related to this added protection:</span></span>

-   <span data-ttu-id="a9135-126">Aplicativos que podem ter usado as configurações agora protegidas como um armazenamento de dados ou como um ponto de extensibilidade raro ou indesejado</span><span class="sxs-lookup"><span data-stu-id="a9135-126">Applications that may have been using the now-protected settings as a data store or as a rare or unintended extensibility point</span></span>
-   <span data-ttu-id="a9135-127">Em casos raros, o mecanismo de detecção usado para identificar as configurações do aplicativo pode não reconhecer uma configuração específica e, portanto, a camada de mitigação da compatibilidade de aplicativos pode não ser aplicada</span><span class="sxs-lookup"><span data-stu-id="a9135-127">In rare cases, the detection mechanism used to identify application setups may not recognize a particular setup and so the application compatibility mitigation layer may not be applied</span></span>

## <a name="mitigation"></a><span data-ttu-id="a9135-128">Atenuação</span><span class="sxs-lookup"><span data-stu-id="a9135-128">Mitigation</span></span>

<span data-ttu-id="a9135-129">O principal meio de mitigação é a camada de compatibilidade de aplicativos do sistema, que é aplicada automaticamente às configurações do aplicativo quando detectada.</span><span class="sxs-lookup"><span data-stu-id="a9135-129">The primary means of mitigation is the system's application compatibility layer, which is automatically applied to application setups when detected.</span></span> <span data-ttu-id="a9135-130">Você também pode aplicá-lo manualmente a qualquer aplicativo usando a guia Compatibilidade nas propriedades do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a9135-130">You can also manually apply it to any application using the compatibility tab in the application's properties.</span></span>

<span data-ttu-id="a9135-131">Essa camada resolve o problema interceptando operações de registro.</span><span class="sxs-lookup"><span data-stu-id="a9135-131">This layer resolves the problem by intercepting registry operations.</span></span> <span data-ttu-id="a9135-132">No caso em que o aplicativo estava tentando modificar uma configuração somente leitura (WRP), a camada sempre retorna êxito, embora a configuração não tenha sido realmente alterada.</span><span class="sxs-lookup"><span data-stu-id="a9135-132">In the case where the application was attempting to modify a read-only (WRP) setting, the layer always returns success, even though the setting was not really changed.</span></span> <span data-ttu-id="a9135-133">Para a maioria dos aplicativos, isso não causará nenhum problema.</span><span class="sxs-lookup"><span data-stu-id="a9135-133">For most applications, this will cause no problems.</span></span> <span data-ttu-id="a9135-134">No entanto, há uma possibilidade de que o aplicativo precise que a configuração seja alterada para funcionar corretamente, que é o primeiro cenário descrito acima.</span><span class="sxs-lookup"><span data-stu-id="a9135-134">However, there is a possibility that the application needed that setting changed in order to function properly, which is the first scenario described above.</span></span>

## <a name="solution"></a><span data-ttu-id="a9135-135">Solução</span><span class="sxs-lookup"><span data-stu-id="a9135-135">Solution</span></span>

<span data-ttu-id="a9135-136">Para os dois cenários identificados acima:</span><span class="sxs-lookup"><span data-stu-id="a9135-136">For the two scenarios identified above:</span></span>

-   <span data-ttu-id="a9135-137">Se o aplicativo exigir que a chave seja gravável para poder funcionar ou usar o armazenamento de dados, não haverá nenhuma solução diferente de alterar o aplicativo para que ele não grave mais nesse local.</span><span class="sxs-lookup"><span data-stu-id="a9135-137">If the application requires the key to be writable in order to function or use the data store, there is no solution other than changing the application so that it no longer writes to that location.</span></span>
-   <span data-ttu-id="a9135-138">Se a camada de compatibilidade não tiver sido aplicada a uma configuração, a falha de instalação deverá ser detectada e executada novamente.</span><span class="sxs-lookup"><span data-stu-id="a9135-138">If the compatibility layer was not applied to a setup, the setup failure should be detected and offered to be applied and re-run.</span></span> <span data-ttu-id="a9135-139">Os aplicativos também podem ser executados no modo de compatibilidade. nesse caso, a camada de mitigação sempre é aplicada.</span><span class="sxs-lookup"><span data-stu-id="a9135-139">Applications can also run in compatibility mode, in which case the mitigation layer is always applied.</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="a9135-140">Testes de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="a9135-140">Compatibility Tests</span></span>

<span data-ttu-id="a9135-141">Como detectar se um aplicativo tinha mitigação de WRP aplicada a ele:</span><span class="sxs-lookup"><span data-stu-id="a9135-141">How to detect if an application had WRP mitigation applied to it:</span></span>

-   <span data-ttu-id="a9135-142">Windows Installer está ciente da WRP; Ele ignora automaticamente e silenciosamente as tentativas de gravar ou modificar um recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="a9135-142">Windows Installer is aware of WRP; it automatically and silently ignores attempts to write or modify a protected resource.</span></span> <span data-ttu-id="a9135-143">Se o aplicativo tiver sido instalado com Windows Installer e o registro em log tiver sido habilitado, um aviso será registrado para cada operação de gravação da chave do registro que foi ignorada porque ele é um recurso protegido por WRP.</span><span class="sxs-lookup"><span data-stu-id="a9135-143">If the application was installed with Windows Installer and logging was enabled, then a warning will be logged for each registry key write operation that was ignored due to its being a WRP-protected resource.</span></span>
-   <span data-ttu-id="a9135-144">A API WRP incorpora SfCIsKeyProtected, que pode consultar se uma chave do registro é protegida por WRP no sistema atual.</span><span class="sxs-lookup"><span data-stu-id="a9135-144">The WRP API incorporates SfCIsKeyProtected, which can query if a registry key is WRP-protected on the current system.</span></span> <span data-ttu-id="a9135-145">Consulte a entrada WRP no MSDN nos links abaixo para obter informações adicionais sobre como usar essa API.</span><span class="sxs-lookup"><span data-stu-id="a9135-145">See the WRP entry in MSDN in the links below for additional information on using this API.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="a9135-146">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="a9135-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="a9135-147">Proteção de Recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="a9135-147">Windows Resource Protection</span></span>](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
