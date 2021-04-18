---
description: .
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Serviços de Área de Trabalho Remota (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bd39785526b11ac2e4c0ede26bbb9971aadc9a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105788696"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="48c1f-103">Serviços de Área de Trabalho Remota (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="48c1f-103">Remote Desktop Services (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="48c1f-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="48c1f-104">Affected Platforms</span></span>

<span data-ttu-id="48c1f-105">**Servidores** – windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48c1f-105">**Servers** – Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="48c1f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="48c1f-106">Description</span></span>

<span data-ttu-id="48c1f-107">Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) permite que vários usuários simultâneos acessem o Windows Server para fornecer serviços de Hospedagem de aplicativos e dados usando a tecnologia "virtualização de apresentação" da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="48c1f-107">Remote Desktop Services (formerly known as Terminal Services) allows multiple concurrent users to access Windows Server in order to provide application and data hosting services using Microsoft "Presentation Virtualization" technology.</span></span>

<span data-ttu-id="48c1f-108">Embora a maioria dos aplicativos de 32 bits e 64 bits seja executada como está no Windows Serviços de Área de Trabalho Remota, vários outros não são executados conforme o esperado devido à diferença na plataforma (ambiente de vários usuários, acesso simultâneo por vários usuários e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="48c1f-108">While most 32-bit and 64-bit applications run as is on Windows Remote Desktop Services, several others do not perform as expected due to the difference in the platform (multi-user environment, concurrent access by multiple users, and so on).</span></span>

<span data-ttu-id="48c1f-109">Para obter mais informações sobre a qualidade do aplicativo, leia a *preparação do aplicativo para White Paper de serviços de terminal* .</span><span class="sxs-lookup"><span data-stu-id="48c1f-109">For further information regarding application quality, please read the *Application Readiness for Terminal Services* white paper.</span></span> <span data-ttu-id="48c1f-110">Visite a página do produto Serviços de Área de Trabalho Remota e os sites do TechNet da TS saiba mais sobre Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48c1f-110">Visit the Remote Desktop Services product page and the TS TechNet websites learn more about Remote Desktop Services.</span></span> <span data-ttu-id="48c1f-111">Para saber mais sobre como desenvolver aplicativos para Serviços de Área de Trabalho Remota, examine as *diretrizes de programação dos serviços de terminal*.</span><span class="sxs-lookup"><span data-stu-id="48c1f-111">To learn more about developing applications for Remote Desktop Services, review the *Terminal Services Programming Guidelines*.</span></span> <span data-ttu-id="48c1f-112">(Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.)</span><span class="sxs-lookup"><span data-stu-id="48c1f-112">(These resources may not be available in some languages and countries/regions.)</span></span>

## <a name="manifestation-of-impacts-and-their-mitigations"></a><span data-ttu-id="48c1f-113">Manifestação de impactos e suas atenuações</span><span class="sxs-lookup"><span data-stu-id="48c1f-113">Manifestation of Impacts and Their Mitigations</span></span>

<span data-ttu-id="48c1f-114">Três alterações no Windows 7 afetam os aplicativos no Serviços de Área de Trabalho Remota:</span><span class="sxs-lookup"><span data-stu-id="48c1f-114">Three changes in Windows 7 affect applications on Remote Desktop Services:</span></span>

-   <span data-ttu-id="48c1f-115">O Windows Server 2008 R2 é de 64 bits somente</span><span class="sxs-lookup"><span data-stu-id="48c1f-115">Windows Server 2008 R2 is 64-bit only</span></span>
-   <span data-ttu-id="48c1f-116">Virtualização de IP por sessão</span><span class="sxs-lookup"><span data-stu-id="48c1f-116">Per-session IP Virtualization</span></span>
-   <span data-ttu-id="48c1f-117">Implantações baseadas em MSI – chaves específicas do usuário</span><span class="sxs-lookup"><span data-stu-id="48c1f-117">MSI-based deployments – User-specific keys</span></span>

<span data-ttu-id="48c1f-118">**64 bits somente Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="48c1f-118">**64-bit Only Windows Server 2008 R2**</span></span>

<span data-ttu-id="48c1f-119">Os aplicativos escritos para o servidor de 32 bits serão executados no modo WoW e não nativamente no Windows Server 2008 R2 ou, portanto, no Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48c1f-119">Applications written for 32-bit server will run in WoW mode and not natively on the Windows Server 2008 R2 or, hence, on Remote Desktop Services.</span></span> <span data-ttu-id="48c1f-120">Consulte o tópico Windows 7 64-bit only para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="48c1f-120">See the Windows 7 64-Bit Only topic for details.</span></span>

<span data-ttu-id="48c1f-121">*Mitigações para apenas 64 bits do Windows Server 2008 R2*</span><span class="sxs-lookup"><span data-stu-id="48c1f-121">*Mitigations for 64-bit only Windows Server 2008 R2*</span></span>

<span data-ttu-id="48c1f-122">A maioria dos aplicativos escritos para 32 bits continuará funcionando normalmente no modo WoW.</span><span class="sxs-lookup"><span data-stu-id="48c1f-122">Most applications written for 32-bit will continue to work as normal in WoW mode.</span></span> <span data-ttu-id="48c1f-123">Todos os novos aplicativos escritos para o Windows 7 Serviços de Área de Trabalho Remota devem ser desenvolvidos e testados para implantação em plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="48c1f-123">Any new applications written for Windows 7 Remote Desktop Services should be developed and tested for deployment on 64-bit platforms.</span></span>

<span data-ttu-id="48c1f-124">**Virtualização de IP**</span><span class="sxs-lookup"><span data-stu-id="48c1f-124">**IP Virtualization**</span></span>

<span data-ttu-id="48c1f-125">Virtualização de IP de Área de Trabalho Remota permite que o usuário atribua endereços IP a conexões de área de trabalho remota em uma base por sessão ou por programa:</span><span class="sxs-lookup"><span data-stu-id="48c1f-125">Remote Desktop IP Virtualization allows the user to assign IP addresses to remote desktop connections on a per-session or per-program basis:</span></span>

-   <span data-ttu-id="48c1f-126">Se você atribuir endereços IP em uma base por sessão, todos os aplicativos usarão o endereço IP da sessão.</span><span class="sxs-lookup"><span data-stu-id="48c1f-126">If you assign IP addresses on a per-session basis, all of the applications will use the session IP address.</span></span>
-   <span data-ttu-id="48c1f-127">Se você atribuir endereços IP por programa, somente os aplicativos especificados usarão o endereço IP da sessão e os aplicativos restantes na sessão não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="48c1f-127">If you assign IP addresses on a per-program basis, only the specified applications will use the session IP address and the remaining applications in the session will not be affected.</span></span>
-   <span data-ttu-id="48c1f-128">Se você atribuir endereços IP para vários programas, eles compartilharão um endereço IP de sessão.</span><span class="sxs-lookup"><span data-stu-id="48c1f-128">If you assign IP addresses for multiple programs, they will share a session IP address.</span></span>
-   <span data-ttu-id="48c1f-129">Se você tiver mais de um adaptador de rede no computador, também deverá escolher um deles para Virtualização de IP de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48c1f-129">If you have more than one network adapter on the computer, you must also choose one of them for Remote Desktop IP Virtualization.</span></span>

<span data-ttu-id="48c1f-130">*Mitigações para virtualização de IP*</span><span class="sxs-lookup"><span data-stu-id="48c1f-130">*Mitigations for IP Virtualization*</span></span>

<span data-ttu-id="48c1f-131">Alguns programas exigem um endereço IP exclusivo para cada instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48c1f-131">Some programs require a unique IP address for each instance of the application.</span></span> <span data-ttu-id="48c1f-132">Antes do Windows Server 2008 R2, cada sessão em um servidor de área de trabalho remota compartilhou o mesmo endereço IP, resultando em problemas de compatibilidade para esses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="48c1f-132">Prior to Windows Server 2008 R2, every session on a remote desktop server shared the same IP address, resulting in compatibility issues for these applications.</span></span> <span data-ttu-id="48c1f-133">Virtualização de IP de Área de Trabalho Remota permite que esses aplicativos sejam executados em um servidor Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48c1f-133">Remote Desktop IP Virtualization allows these applications to run on a Remote Desktop Server.</span></span>

<span data-ttu-id="48c1f-134">**Implantações baseadas em MSI**</span><span class="sxs-lookup"><span data-stu-id="48c1f-134">**MSI-based Deployments**</span></span>

<span data-ttu-id="48c1f-135">A compatibilidade do Microsoft Installer RDS é um novo recurso incluído com o Serviços de Área de Trabalho Remota no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="48c1f-135">Microsoft Installer RDS Compatibility is a new feature included with Remote Desktop Services in Windows Server 2008 R2.</span></span> <span data-ttu-id="48c1f-136">Com Serviços de Área de Trabalho Remota no Windows Server 2008 R2, as instalações de aplicativos por usuário são enfileiradas pelo servidor Área de Trabalho Remota e, em seguida, manipuladas pelo Microsoft Installer.</span><span class="sxs-lookup"><span data-stu-id="48c1f-136">With Remote Desktop Services in Windows Server 2008 R2, per-user application installations are queued by the Remote Desktop Server and then handled by the Microsoft Installer.</span></span>

<span data-ttu-id="48c1f-137">No Windows Server 2008 R2, você pode instalar um programa no servidor Área de Trabalho Remota da mesma forma que instalaria o programa em uma área de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="48c1f-137">In Windows Server 2008 R2, you can install a program on the Remote Desktop Server just as you would install the program on a local desktop.</span></span> <span data-ttu-id="48c1f-138">No entanto, certifique-se de que você instale o programa para todos os usuários e instale todos os componentes do programa localmente no servidor de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48c1f-138">Ensure, however, that you install the program for all users and install all components of the program locally on the Remote Desktop Server.</span></span>

<span data-ttu-id="48c1f-139">*Mitigações para implantações baseadas em MSI*</span><span class="sxs-lookup"><span data-stu-id="48c1f-139">*Mitigations for MSI based Deployments*</span></span>

<span data-ttu-id="48c1f-140">Antes da versão do Windows Server 2008 R2 do Serviços de Área de Trabalho Remota, o Windows oferece suporte a apenas uma instalação de Windows Installer por vez.</span><span class="sxs-lookup"><span data-stu-id="48c1f-140">Prior to the Windows Server 2008 R2 version of Remote Desktop Services, Windows supported only one Windows Installer installation at a time.</span></span> <span data-ttu-id="48c1f-141">Para aplicativos que exigiam configurações por usuário, como o Microsoft Office Word, um administrador precisava pré-instalar o aplicativo e os desenvolvedores de aplicativos precisavam testar esses aplicativos no cliente da área de trabalho remota e no Host da Sessão da Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48c1f-141">For applications that required per-user configurations, such as Microsoft Office Word, an administrator needed to pre-install the application, and application developers needed to test these applications on both the remote desktop client and the Remote Desktop Session Host.</span></span> <span data-ttu-id="48c1f-142">Windows Installer recurso de compatibilidade de RDS permite identificar e instalar configurações de usuário ausentes para vários usuários simultaneamente e torna a experiência de instalação do aplicativo no Área de Trabalho Remota Server semelhante àquela em uma área de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="48c1f-142">Windows Installer RDS Compatibility feature allows identifying and installing missing per-user configurations for multiple users simultaneously and makes the application installation experience on Remote Desktop Server similar to that on a local desktop.</span></span>

<span data-ttu-id="48c1f-143">**Windows Server 2008 R2 com a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) habilitada:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="48c1f-143">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="48c1f-144">Uma instalação de vários pacotes usando a [tabela MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) falhará se a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="48c1f-144">A multiple package installation using the [MsiEmbeddedChainer table](../msi/msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="48c1f-145">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="48c1f-145">Links to Other Resources</span></span>

-   [<span data-ttu-id="48c1f-146">Diretrizes de programação dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="48c1f-146">Terminal Services Programming Guidelines</span></span>](../termserv/terminal-services-programming-guidelines.md)
-   [<span data-ttu-id="48c1f-147">home page de produto dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="48c1f-147">Terminal Services product home page</span></span>](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [<span data-ttu-id="48c1f-148">Preparação do aplicativo para white paper de serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="48c1f-148">Application Readiness for Terminal Services white paper</span></span>](/collaborate/connect-redirect)

> [!Note]  
> <span data-ttu-id="48c1f-149">Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.</span><span class="sxs-lookup"><span data-stu-id="48c1f-149">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
