---
description: .
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Controle de versão do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e71cb671e19463ca6137c9b0ce7af04c2793e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757278"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="df7dd-103">Controle de versão do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="df7dd-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="df7dd-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="df7dd-104">Affected Platforms</span></span>

<span data-ttu-id="df7dd-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="df7dd-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="df7dd-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df7dd-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="df7dd-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="df7dd-107">Feature Impact</span></span>

<span data-ttu-id="df7dd-108">**Severidade** -alta</span><span class="sxs-lookup"><span data-stu-id="df7dd-108">**Severity** - High</span></span>  
<span data-ttu-id="df7dd-109">**Frequência** -alta</span><span class="sxs-lookup"><span data-stu-id="df7dd-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="df7dd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="df7dd-110">Description</span></span>

<span data-ttu-id="df7dd-111">O número de versão interno para o Windows 7 e o Windows Server 2008 R2 é 6,1.</span><span class="sxs-lookup"><span data-stu-id="df7dd-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="df7dd-112">A função GetVersion agora retornará esse número de versão para os aplicativos quando consultada.</span><span class="sxs-lookup"><span data-stu-id="df7dd-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="df7dd-113">Isso é especialmente importante para antivírus, backup, aplicativos de utilitário e proteção de cópia.</span><span class="sxs-lookup"><span data-stu-id="df7dd-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="df7dd-114">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="df7dd-114">Manifestation of Impact</span></span>

<span data-ttu-id="df7dd-115">A manifestação dessa alteração é específica ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="df7dd-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="df7dd-116">Isso significa que qualquer aplicativo que verifica especificamente a versão do sistema operacional terá um número de versão mais alto, o que pode levar a uma ou mais das seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="df7dd-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="df7dd-117">Os instaladores de aplicativo podem não conseguir instalar o aplicativo, e os aplicativos podem não conseguir iniciar</span><span class="sxs-lookup"><span data-stu-id="df7dd-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="df7dd-118">Os aplicativos podem se tornar instáveis ou falhar</span><span class="sxs-lookup"><span data-stu-id="df7dd-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="df7dd-119">Os aplicativos podem gerar mensagens de erro, mas continuar a funcionar corretamente</span><span class="sxs-lookup"><span data-stu-id="df7dd-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="df7dd-120">Atenuação</span><span class="sxs-lookup"><span data-stu-id="df7dd-120">Mitigation</span></span>

<span data-ttu-id="df7dd-121">A maioria dos aplicativos funcionará corretamente no Windows 7 e no Windows Server 2008 R2, pois a compatibilidade de aplicativos no Windows 7 e no Windows Server 2008 R2 é muito alta.</span><span class="sxs-lookup"><span data-stu-id="df7dd-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="df7dd-122">No entanto, o Windows 7 e o Windows Server 2008 R2 incluem uma exibição de compatibilidade para instaladores e aplicativos que verificam a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="df7dd-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="df7dd-123">Para habilitar o modo de exibição de compatibilidade, os usuários podem clicar com o botão direito do mouse no atalho ou no arquivo executável e aplicar o modo de exibição de compatibilidade do Windows XP SP2 ou do Windows Vista na guia compatibilidade. Na maioria dos casos, isso deve permitir que o aplicativo opere corretamente sem a necessidade de qualquer alteração no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="df7dd-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="df7dd-124">Os profissionais de ti também podem aplicar qualquer uma das correções de compatibilidade VersionLie aplicáveis, usando a ferramenta Compatibility Administrator, que é instalada com o kit de ferramentas de compatibilidade de aplicativos (ACT).</span><span class="sxs-lookup"><span data-stu-id="df7dd-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="df7dd-125">Por exemplo, se um aplicativo não funcionar porque está verificando, mas não localizando, as informações de versão do Windows XP® com Service Pack 2 (SP2), o WinXPSP2VersionLie pode ser aplicado para retornar as informações de número de versão apropriadas para o aplicativo, independentemente da versão real do sistema operacional em execução no computador.</span><span class="sxs-lookup"><span data-stu-id="df7dd-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="df7dd-126">As correções de compatibilidade do VersionLie disponíveis são:</span><span class="sxs-lookup"><span data-stu-id="df7dd-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="df7dd-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-127">Win95VersionLie</span></span>
-   <span data-ttu-id="df7dd-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-128">Win98VersionLie</span></span>
-   <span data-ttu-id="df7dd-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="df7dd-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="df7dd-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="df7dd-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="df7dd-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="df7dd-134">WinXPVersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="df7dd-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="df7dd-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="df7dd-137">VistaRTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="df7dd-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="df7dd-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="df7dd-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="df7dd-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="df7dd-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="df7dd-142">Solução</span><span class="sxs-lookup"><span data-stu-id="df7dd-142">Solution</span></span>

<span data-ttu-id="df7dd-143">Em geral, os aplicativos não devem executar verificações de versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="df7dd-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="df7dd-144">Se um aplicativo precisar de um recurso específico, é preferível tentar encontrar o recurso e falhar apenas se o recurso necessário estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="df7dd-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="df7dd-145">No mínimo, os aplicativos devem sempre aceitar números de versão maiores ou iguais à versão mais baixa com suporte do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="df7dd-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="df7dd-146">As exceções devem ocorrer apenas se houver um requisito específico, de negócios ou de componentes do sistema.</span><span class="sxs-lookup"><span data-stu-id="df7dd-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="df7dd-147">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="df7dd-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="df7dd-148">Download do kit de ferramentas de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="df7dd-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="df7dd-149">[Correções de compatibilidade conhecidas, modos de compatibilidade e mensagens AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="df7dd-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
