---
description: Windows Installer é a solução recomendada para a instalação e a instalação de aplicativos no Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guia baseado em função para Windows Installer documentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010704"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a><span data-ttu-id="cb56b-103">Guia baseado em função para Windows Installer documentação</span><span class="sxs-lookup"><span data-stu-id="cb56b-103">Role-based Guide to Windows Installer Documentation</span></span>

<span data-ttu-id="cb56b-104">Windows Installer é a solução recomendada para a instalação e a instalação de aplicativos no Windows.</span><span class="sxs-lookup"><span data-stu-id="cb56b-104">Windows Installer is the recommended solution for the installation and setup of applications on Windows.</span></span> <span data-ttu-id="cb56b-105">Portanto, algumas das informações contidas neste SDK serão de interesse de uma ampla gama de desenvolvimento de software e profissionais de ti.</span><span class="sxs-lookup"><span data-stu-id="cb56b-105">Therefore, some of the information contained in this SDK will be of interest to a wide range of software development and IT professionals.</span></span> <span data-ttu-id="cb56b-106">Esta seção é fornecida como um guia para os leitores que preferem ver links para tópicos organizados por funções profissionais e cenários comuns de tarefas.</span><span class="sxs-lookup"><span data-stu-id="cb56b-106">This section is provided as a guide to readers who prefer to see links to topics organized by professional role and common task scenarios.</span></span> <span data-ttu-id="cb56b-107">Como as funções podem diferir muito entre as organizações, o agrupamento a seguir só deve ser considerado um guia para um local para começar a pesquisar as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="cb56b-107">Because roles can differ greatly between organizations, the following grouping should only be considered as a guide to a location to start searching for the information you need.</span></span>

-   [<span data-ttu-id="cb56b-108">Desenvolvedores de aplicativos</span><span class="sxs-lookup"><span data-stu-id="cb56b-108">Application Developers</span></span>](#application-developers)
-   [<span data-ttu-id="cb56b-109">Autores de instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-109">Setup Authors</span></span>](#setup-authors)
-   [<span data-ttu-id="cb56b-110">Profissionais de TI</span><span class="sxs-lookup"><span data-stu-id="cb56b-110">IT Professionals</span></span>](#it-professionals)
-   [<span data-ttu-id="cb56b-111">Desenvolvedores de infraestrutura</span><span class="sxs-lookup"><span data-stu-id="cb56b-111">Infrastructure Developers</span></span>](#infrastructure-developers)

<span data-ttu-id="cb56b-112">Esta documentação destina-se a desenvolvedores de software que desejam criar aplicativos que usam Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-112">This documentation is intended for software developers who want to make applications that use Windows Installer.</span></span> <span data-ttu-id="cb56b-113">Como a principal fonte de material de referência para o instalador, o SDK fornece informações sobre pacotes de instalação e o serviço do instalador.</span><span class="sxs-lookup"><span data-stu-id="cb56b-113">As the primary source of reference material for the installer, the SDK provides information about installation packages and the installer service.</span></span> <span data-ttu-id="cb56b-114">Ele contém descrições completas da API (interface de programação de aplicativo) e dos elementos do banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="cb56b-114">It contains complete descriptions of the application programming interface (API) and the elements of the installer database.</span></span>

<span data-ttu-id="cb56b-115">Para obter mais informações, consulte [outras fontes de Windows Installer informações](other-sources-of-windows-installer-information.md).</span><span class="sxs-lookup"><span data-stu-id="cb56b-115">For more information, see [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).</span></span>

## <a name="application-developers"></a><span data-ttu-id="cb56b-116">Desenvolvedores de aplicativos</span><span class="sxs-lookup"><span data-stu-id="cb56b-116">Application Developers</span></span>

<span data-ttu-id="cb56b-117">Os desenvolvedores de aplicativos criam aplicativos que chamam a interface de programação de aplicativo Windows Installer e instalam pacotes do Windows Installer em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="cb56b-117">Application developers create applications that call the Windows Installer application programming interface and install Windows installer packages at run time.</span></span> <span data-ttu-id="cb56b-118">O Windows Installer pode funcionar em um aplicativo como o autoreparo e a instalação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="cb56b-118">The Windows Installer can do work in an application such as self-repair and installation-on-demand.</span></span> <span data-ttu-id="cb56b-119">Normalmente, os desenvolvedores de aplicativos fazem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-119">Typically, application Developers do the following:</span></span>

-   <span data-ttu-id="cb56b-120">Habilite a instalação sob demanda de aplicativos em tempo de execução de dentro de outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cb56b-120">Enable installation-on-demand of applications at run time from within another application.</span></span>

    <span data-ttu-id="cb56b-121">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-121">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-122">Usando funções do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-122">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="cb56b-123">Referência de função do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-123">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-124">Instalação sob demanda</span><span class="sxs-lookup"><span data-stu-id="cb56b-124">Installation-On-Demand</span></span>](installation-on-demand.md)
    -   [<span data-ttu-id="cb56b-125">Gerenciamento de componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-125">Component Management</span></span>](component-management.md)
    -   [<span data-ttu-id="cb56b-126">Editando atalhos do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-126">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="cb56b-127">**Propriedade OLEAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="cb56b-127">**OLEAdvtSupport Property**</span></span>](oleadvtsupport.md)
    -   [<span data-ttu-id="cb56b-128">Suporte de plataforma do anúncio</span><span class="sxs-lookup"><span data-stu-id="cb56b-128">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)

-   <span data-ttu-id="cb56b-129">Habilite o reparo automático de aplicativos reinstalando os componentes conforme necessário no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="cb56b-129">Enable self-repair of applications by reinstalling components as needed at run time.</span></span>

    <span data-ttu-id="cb56b-130">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-130">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-131">Usando funções do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-131">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="cb56b-132">Referência de função do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-132">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-133">Resiliência</span><span class="sxs-lookup"><span data-stu-id="cb56b-133">Resiliency</span></span>](resiliency.md)
    -   [<span data-ttu-id="cb56b-134">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="cb56b-134">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="cb56b-135">Pesquisando um componente ou recurso desfeito</span><span class="sxs-lookup"><span data-stu-id="cb56b-135">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="cb56b-136">Substituindo arquivos existentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-136">Replacing Existing Files</span></span>](replacing-existing-files.md)

-   <span data-ttu-id="cb56b-137">Exiba uma interface do usuário para coletar informações de usuário e preferências de configuração na primeira vez que um aplicativo for instalado ou executado.</span><span class="sxs-lookup"><span data-stu-id="cb56b-137">Display a user interface to collect user information and configuration preferences the first time an application is installed or run.</span></span> <span data-ttu-id="cb56b-138">A interface do usuário deve ser adicionada pelo autor da instalação do pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-138">The user interface must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="cb56b-139">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-139">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-140">Usando funções do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-140">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="cb56b-141">Inicializando um aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb56b-141">Initializing an Application</span></span>](initializing-an-application.md)
    -   [<span data-ttu-id="cb56b-142">Caixa de diálogo FirstRun</span><span class="sxs-lookup"><span data-stu-id="cb56b-142">FirstRun Dialog</span></span>](firstrun-dialog.md)
    -   [<span data-ttu-id="cb56b-143">Sobre a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="cb56b-143">About the User Interface</span></span>](about-the-user-interface.md)

-   <span data-ttu-id="cb56b-144">Crie aplicativos que usam um modelo de indireção para se referir a componentes com funcionalidade paralela.</span><span class="sxs-lookup"><span data-stu-id="cb56b-144">Create applications that use an indirection model to refer to components with parallel functionality.</span></span> <span data-ttu-id="cb56b-145">As categorias de componentes qualificados devem ser adicionadas pelo autor da instalação do pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-145">The qualified component categories must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="cb56b-146">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-146">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-147">Componentes qualificados</span><span class="sxs-lookup"><span data-stu-id="cb56b-147">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="cb56b-148">Usando componentes qualificados</span><span class="sxs-lookup"><span data-stu-id="cb56b-148">Using Qualified Components</span></span>](using-qualified-components.md)

-   <span data-ttu-id="cb56b-149">Use assemblies privados e lado a lado para isolar aplicativos e reduzir conflitos de DLL.</span><span class="sxs-lookup"><span data-stu-id="cb56b-149">Use private and side-by-side assemblies to isolate applications and reduce DLL conflicts.</span></span>

    <span data-ttu-id="cb56b-150">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-150">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-151">Assemblies</span><span class="sxs-lookup"><span data-stu-id="cb56b-151">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="cb56b-152">Chaves do registro de assembly gravadas por Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-152">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="cb56b-153">Instalando assemblies do Win32 para compartilhamento lado a lado no Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb56b-153">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [<span data-ttu-id="cb56b-154">Instalando assemblies do Win32 para o uso particular de um aplicativo no Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb56b-154">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [<span data-ttu-id="cb56b-155">Tabela MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="cb56b-155">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="cb56b-156">Tabela MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="cb56b-156">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="cb56b-157">**MsiProvideAssembly**</span><span class="sxs-lookup"><span data-stu-id="cb56b-157">**MsiProvideAssembly**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [<span data-ttu-id="cb56b-158">**Propriedade MsiWin32AssemblySupport**</span><span class="sxs-lookup"><span data-stu-id="cb56b-158">**MsiWin32AssemblySupport Property**</span></span>](msiwin32assemblysupport.md)
    -   [<span data-ttu-id="cb56b-159">**Propriedade MsiNetAssemblySupport**</span><span class="sxs-lookup"><span data-stu-id="cb56b-159">**MsiNetAssemblySupport Property**</span></span>](msinetassemblysupport.md)
    -   [<span data-ttu-id="cb56b-160">**Componentes isolados**</span><span class="sxs-lookup"><span data-stu-id="cb56b-160">**Isolated Components**</span></span>](isolated-components.md)

-   <span data-ttu-id="cb56b-161">Prepare o aplicativo para instalar suas próprias atualizações importantes abrangentes.</span><span class="sxs-lookup"><span data-stu-id="cb56b-161">Prepare the application to install its own comprehensive major upgrades.</span></span>

    <span data-ttu-id="cb56b-162">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-162">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-163">Aplicação de patch e atualizações</span><span class="sxs-lookup"><span data-stu-id="cb56b-163">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="cb56b-164">Principais atualizações</span><span class="sxs-lookup"><span data-stu-id="cb56b-164">Major Upgrades</span></span>](major-upgrades.md)
    -   [<span data-ttu-id="cb56b-165">**Propriedade UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="cb56b-165">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="cb56b-166">**Usando um UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="cb56b-166">**Using an UpgradeCode**</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="cb56b-167">Impedindo que um pacote antigo seja instalado em uma versão mais recente</span><span class="sxs-lookup"><span data-stu-id="cb56b-167">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   <span data-ttu-id="cb56b-168">Prepare o aplicativo para instalar suas próprias atualizações secundárias, pequenas atualizações ou correções.</span><span class="sxs-lookup"><span data-stu-id="cb56b-168">Prepare the application to install its own minor upgrades, small updates, or fixes.</span></span>

    <span data-ttu-id="cb56b-169">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-169">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-170">Aplicação de patch e atualizações</span><span class="sxs-lookup"><span data-stu-id="cb56b-170">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="cb56b-171">Pequenas atualizações</span><span class="sxs-lookup"><span data-stu-id="cb56b-171">Small Updates</span></span>](small-updates.md)
    -   [<span data-ttu-id="cb56b-172">Atualizações secundárias</span><span class="sxs-lookup"><span data-stu-id="cb56b-172">Minor Upgrades</span></span>](minor-upgrades.md)

-   <span data-ttu-id="cb56b-173">Organize os recursos do aplicativo em componentes que podem funcionar com o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-173">Organize application resources into components that can work with the Windows Installer.</span></span>

    <span data-ttu-id="cb56b-174">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-174">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-175">Componentes do Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-175">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="cb56b-176">Trabalhando com recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-176">Working with Features and Components</span></span>](working-with-features-and-components.md)
    -   [<span data-ttu-id="cb56b-177">Usando componentes transitivos</span><span class="sxs-lookup"><span data-stu-id="cb56b-177">Using Transitive Components</span></span>](using-transitive-components.md)
    -   [<span data-ttu-id="cb56b-178">O que acontece se as regras de componente forem interrompidas?</span><span class="sxs-lookup"><span data-stu-id="cb56b-178">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="cb56b-179">Organizando aplicativos em componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-179">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="cb56b-180">Componentes isolados</span><span class="sxs-lookup"><span data-stu-id="cb56b-180">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="cb56b-181">Componentes qualificados</span><span class="sxs-lookup"><span data-stu-id="cb56b-181">Qualified Components</span></span>](qualified-components.md)

## <a name="setup-authors"></a><span data-ttu-id="cb56b-182">Autores de instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-182">Setup Authors</span></span>

<span data-ttu-id="cb56b-183">Os autores de instalação criam pacotes de Windows Installer (arquivos. msi) que contêm a lógica de instalação e as informações necessárias para instalar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cb56b-183">Setup Authors create Windows Installer packages (.msi files) that contain the setup logic and information needed to install an application.</span></span> <span data-ttu-id="cb56b-184">Normalmente, eles usam ferramentas de criação como [Orca.exe](orca-exe.md) para popular o banco de dados de Windows Installer com a lógica de instalação e as informações.</span><span class="sxs-lookup"><span data-stu-id="cb56b-184">They typically use authoring tools such as [Orca.exe](orca-exe.md) to populate the Windows Installer database with the setup logic and information.</span></span> <span data-ttu-id="cb56b-185">Normalmente, os autores da instalação fazem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-185">Typically, Setup Authors do the following:</span></span>

-   <span data-ttu-id="cb56b-186">Determine a funcionalidade disponível com diferentes versões de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-186">Determine the functionality available with different Windows Installer versions.</span></span>

    <span data-ttu-id="cb56b-187">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-187">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-188">Determinando a versão de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-188">Determining the Windows Installer Version</span></span>](determining-the-windows-installer-version.md)
    -   [<span data-ttu-id="cb56b-189">Versões lançadas do Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-189">Released Versions of Windows Installer</span></span>](released-versions-of-windows-installer.md)
    -   [<span data-ttu-id="cb56b-190">O que há de novo no Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-190">What's New in Windows Installer</span></span>](what-s-new-in-windows-installer.md)

-   <span data-ttu-id="cb56b-191">Organize os recursos do aplicativo em Windows Installer componentes.</span><span class="sxs-lookup"><span data-stu-id="cb56b-191">Organize application resources into Windows Installer components.</span></span>

    <span data-ttu-id="cb56b-192">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-192">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-193">Componentes do Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-193">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="cb56b-194">Organizando aplicativos em componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-194">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="cb56b-195">Alterando o código do componente</span><span class="sxs-lookup"><span data-stu-id="cb56b-195">Changing the Component Code</span></span>](changing-the-component-code.md)
    -   [<span data-ttu-id="cb56b-196">O que acontece se as regras de componente forem interrompidas?</span><span class="sxs-lookup"><span data-stu-id="cb56b-196">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="cb56b-197">Exemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-197">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="cb56b-198">Use ferramentas de criação de pacote Windows Installer de terceiros ou ferramentas de SDK, como [Orca.exe](orca-exe.md) para popular um banco de dados de instalação e criar um pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-198">Use third-party Windows Installer package authoring tools or SDK tools such as [Orca.exe](orca-exe.md) to populate an installation database and create a Windows Installer package.</span></span>

    <span data-ttu-id="cb56b-199">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-199">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-200">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-200">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="cb56b-201">Pacote de instalação, sobre o banco de dados do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-201">Installation Package, About the Installer Database</span></span>](installation-package.md)
    -   [<span data-ttu-id="cb56b-202">Extensões de arquivo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-202">Windows Installer File Extensions</span></span>](windows-installer-file-extensions.md)
    -   [<span data-ttu-id="cb56b-203">Tabelas de banco de dados</span><span class="sxs-lookup"><span data-stu-id="cb56b-203">Database Tables</span></span>](database-tables.md)
    -   [<span data-ttu-id="cb56b-204">Códigos de pacote</span><span class="sxs-lookup"><span data-stu-id="cb56b-204">Package Codes</span></span>](package-codes.md)
    -   [<span data-ttu-id="cb56b-205">Criando um pacote grande</span><span class="sxs-lookup"><span data-stu-id="cb56b-205">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="cb56b-206">Windows Installer em sistemas operacionais de 64 bits</span><span class="sxs-lookup"><span data-stu-id="cb56b-206">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="cb56b-207">Nomeando tabelas, propriedades e ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="cb56b-207">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
    -   [<span data-ttu-id="cb56b-208">Limitações de OLE em fluxos</span><span class="sxs-lookup"><span data-stu-id="cb56b-208">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
    -   [<span data-ttu-id="cb56b-209">Formato de definição de coluna</span><span class="sxs-lookup"><span data-stu-id="cb56b-209">Column Definition Format</span></span>](column-definition-format.md)
    -   [<span data-ttu-id="cb56b-210">Reduzindo o tamanho de um arquivo. msi</span><span class="sxs-lookup"><span data-stu-id="cb56b-210">Reducing the Size of an .msi File</span></span>](reducing-the-size-of-an--msi-file.md)

-   <span data-ttu-id="cb56b-211">Crie o banco de dados Windows Installer para instalar arquivos.</span><span class="sxs-lookup"><span data-stu-id="cb56b-211">Author the Windows Installer database to install files.</span></span>

    <span data-ttu-id="cb56b-212">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-212">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-213">Grupo de tabelas principais</span><span class="sxs-lookup"><span data-stu-id="cb56b-213">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="cb56b-214">Grupo de tabelas de arquivos</span><span class="sxs-lookup"><span data-stu-id="cb56b-214">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="cb56b-215">File Table</span><span class="sxs-lookup"><span data-stu-id="cb56b-215">File Table</span></span>](file-table.md)
    -   [<span data-ttu-id="cb56b-216">Pesquisa de arquivos</span><span class="sxs-lookup"><span data-stu-id="cb56b-216">File Searching</span></span>](file-searching.md)
    -   [<span data-ttu-id="cb56b-217">Custo do arquivo</span><span class="sxs-lookup"><span data-stu-id="cb56b-217">File Costing</span></span>](file-costing.md)
    -   [<span data-ttu-id="cb56b-218">Instalação de arquivo</span><span class="sxs-lookup"><span data-stu-id="cb56b-218">File Installation</span></span>](file-installation.md)
    -   [<span data-ttu-id="cb56b-219">Arquivos complementares</span><span class="sxs-lookup"><span data-stu-id="cb56b-219">Companion Files</span></span>](companion-files.md)
    -   [<span data-ttu-id="cb56b-220">Regras de controle de versão de arquivo</span><span class="sxs-lookup"><span data-stu-id="cb56b-220">File Versioning Rules</span></span>](file-versioning-rules.md)
    -   [<span data-ttu-id="cb56b-221">Controle de versão de arquivo padrão</span><span class="sxs-lookup"><span data-stu-id="cb56b-221">Default File Versioning</span></span>](default-file-versioning.md)
    -   [<span data-ttu-id="cb56b-222">Substituindo arquivos existentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-222">Replacing Existing Files</span></span>](replacing-existing-files.md)
    -   [<span data-ttu-id="cb56b-223">Usando gabinetes e fontes compactadas</span><span class="sxs-lookup"><span data-stu-id="cb56b-223">Using Cabinets and Compressed Sources</span></span>](using-cabinets-and-compressed-sources.md)
    -   [<span data-ttu-id="cb56b-224">Removendo arquivos perdidos</span><span class="sxs-lookup"><span data-stu-id="cb56b-224">Removing Stranded Files</span></span>](removing-stranded-files.md)
    -   [<span data-ttu-id="cb56b-225">Instalando componentes, arquivos, fontes e chaves do registro permanentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-225">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="cb56b-226">Tabela FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="cb56b-226">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
    -   [<span data-ttu-id="cb56b-227">Procurando um arquivo e criando uma propriedade que contém o caminho do arquivo</span><span class="sxs-lookup"><span data-stu-id="cb56b-227">Searching for a File and Creating a Property Holding the File's Path</span></span>](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [<span data-ttu-id="cb56b-228">Procurando um diretório e um arquivo no diretório</span><span class="sxs-lookup"><span data-stu-id="cb56b-228">Searching for a Directory and a File in the Directory</span></span>](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [<span data-ttu-id="cb56b-229">Exemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-229">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="cb56b-230">Crie um banco de dados Windows Installer que instala uma estrutura de diretório e pastas.</span><span class="sxs-lookup"><span data-stu-id="cb56b-230">Author a Windows Installer database that installs a directory structure and folders.</span></span>

    <span data-ttu-id="cb56b-231">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-231">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-232">Grupo de tabelas principais</span><span class="sxs-lookup"><span data-stu-id="cb56b-232">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="cb56b-233">Grupo de tabelas de arquivos</span><span class="sxs-lookup"><span data-stu-id="cb56b-233">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="cb56b-234">Tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-234">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="cb56b-235">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="cb56b-235">Directory Table</span></span>](directory-table.md)
    -   [<span data-ttu-id="cb56b-236">Usando a tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="cb56b-236">Using the Directory Table</span></span>](using-the-directory-table.md)
    -   [<span data-ttu-id="cb56b-237">Usando uma propriedade de diretório em um caminho</span><span class="sxs-lookup"><span data-stu-id="cb56b-237">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)
    -   [<span data-ttu-id="cb56b-238">Propriedades da pasta do sistema</span><span class="sxs-lookup"><span data-stu-id="cb56b-238">System Folder Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="cb56b-239">Tabela CreateFolder</span><span class="sxs-lookup"><span data-stu-id="cb56b-239">CreateFolder Table</span></span>](createfolder-table.md)
    -   [<span data-ttu-id="cb56b-240">Tabela LockPermissions</span><span class="sxs-lookup"><span data-stu-id="cb56b-240">LockPermissions Table</span></span>](lockpermissions-table.md)
    -   [<span data-ttu-id="cb56b-241">Tabela MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="cb56b-241">MsiLockPermissionsEx Table</span></span>](msilockpermissionsex-table.md)
    -   [<span data-ttu-id="cb56b-242">Alterando o local de destino de um diretório</span><span class="sxs-lookup"><span data-stu-id="cb56b-242">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="cb56b-243">Exemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-243">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="cb56b-244">Crie um banco de dados Windows Installer que instala chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="cb56b-244">Author a Windows Installer database that installs registry keys.</span></span>

    <span data-ttu-id="cb56b-245">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-245">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-246">Grupo de tabelas principais</span><span class="sxs-lookup"><span data-stu-id="cb56b-246">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="cb56b-247">Grupo de tabelas do registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-247">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="cb56b-248">Tabela do registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-248">Registry Table</span></span>](registry-table.md)
    -   [<span data-ttu-id="cb56b-249">Modificando o registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-249">Modifying the Registry</span></span>](modifying-the-registry.md)
    -   [<span data-ttu-id="cb56b-250">Adicionando ou removendo chaves do registro na instalação ou remoção de componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-250">Adding or Removing Registry Keys on the Installation or Removal of Components</span></span>](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [<span data-ttu-id="cb56b-251">Adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-251">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="cb56b-252">Instalando componentes, arquivos, fontes e chaves do registro permanentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-252">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="cb56b-253">Pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-253">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [<span data-ttu-id="cb56b-254">Procurando uma entrada de registro e criando uma propriedade que contém o valor do registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-254">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [<span data-ttu-id="cb56b-255">Chaves do registro do assembly gravadas pelo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-255">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="cb56b-256">Desinstalar chave do registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-256">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
    -   [<span data-ttu-id="cb56b-257">Tabela SelfReg</span><span class="sxs-lookup"><span data-stu-id="cb56b-257">SelfReg Table</span></span>](selfreg-table.md)
    -   [<span data-ttu-id="cb56b-258">Especificando a ordem de auto-registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-258">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
    -   [<span data-ttu-id="cb56b-259">Exemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-259">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="cb56b-260">Crie um banco de dados Windows Installer que instala serviços.</span><span class="sxs-lookup"><span data-stu-id="cb56b-260">Author a Windows Installer database that installs services.</span></span>

    <span data-ttu-id="cb56b-261">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-261">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-262">Tabela de desinstalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-262">ServiceInstall Table</span></span>](serviceinstall-table.md)
    -   [<span data-ttu-id="cb56b-263">Tabela de UserControl</span><span class="sxs-lookup"><span data-stu-id="cb56b-263">ServiceControl Table</span></span>](servicecontrol-table.md)
    -   [<span data-ttu-id="cb56b-264">Tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-264">Component Table</span></span>](component-table.md)

-   <span data-ttu-id="cb56b-265">Crie um banco de dados Windows Installer que instala componentes isolados ou componentes COM.</span><span class="sxs-lookup"><span data-stu-id="cb56b-265">Author a Windows Installer database that installs isolated components or COM components.</span></span>

    <span data-ttu-id="cb56b-266">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-266">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-267">Grupo de tabelas do registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-267">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="cb56b-268">Tabela de classes</span><span class="sxs-lookup"><span data-stu-id="cb56b-268">Class Table</span></span>](class-table.md)
    -   [<span data-ttu-id="cb56b-269">Tabela ComPlus</span><span class="sxs-lookup"><span data-stu-id="cb56b-269">Complus Table</span></span>](complus-table.md)
    -   [<span data-ttu-id="cb56b-270">Componentes isolados</span><span class="sxs-lookup"><span data-stu-id="cb56b-270">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="cb56b-271">Usando componentes isolados</span><span class="sxs-lookup"><span data-stu-id="cb56b-271">Using Isolated Components</span></span>](using-isolated-components.md)
    -   [<span data-ttu-id="cb56b-272">Instalação de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="cb56b-272">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
    -   [<span data-ttu-id="cb56b-273">Reinstalação de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="cb56b-273">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
    -   [<span data-ttu-id="cb56b-274">Remoção de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="cb56b-274">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
    -   [<span data-ttu-id="cb56b-275">Instalando um componente COM em um local privado</span><span class="sxs-lookup"><span data-stu-id="cb56b-275">Installing a COM Component to a Private Location</span></span>](installing-a-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="cb56b-276">Tornar um componente COM em um pacote existente privado</span><span class="sxs-lookup"><span data-stu-id="cb56b-276">Make a COM Component in an Existing Package Private</span></span>](make-a-com-component-in-an-existing-package-private.md)
    -   [<span data-ttu-id="cb56b-277">Instalando um aplicativo COM+ com o Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-277">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
    -   [<span data-ttu-id="cb56b-278">Instalando um componente não COM em um local privado</span><span class="sxs-lookup"><span data-stu-id="cb56b-278">Installing a non-COM Component to a Private Location</span></span>](installing-a-non-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="cb56b-279">Tornar um componente não-COM em um pacote particular existente</span><span class="sxs-lookup"><span data-stu-id="cb56b-279">Make a non-COM Component in an Existing Package Private</span></span>](make-a-non-com-component-in-an-existing-package-private.md)

-   <span data-ttu-id="cb56b-280">Crie um banco de dados Windows Installer que instala assemblies.</span><span class="sxs-lookup"><span data-stu-id="cb56b-280">Author a Windows Installer database that installs assemblies.</span></span>

    <span data-ttu-id="cb56b-281">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-281">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-282">Tabela MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="cb56b-282">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="cb56b-283">Tabela MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="cb56b-283">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="cb56b-284">Assemblies</span><span class="sxs-lookup"><span data-stu-id="cb56b-284">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="cb56b-285">Chaves do registro do assembly gravadas pelo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-285">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="cb56b-286">Instalação de assemblies Win32</span><span class="sxs-lookup"><span data-stu-id="cb56b-286">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)

-   <span data-ttu-id="cb56b-287">Crie um banco de dados Windows Installer que instala drivers e tradutores ODBC.</span><span class="sxs-lookup"><span data-stu-id="cb56b-287">Author a Windows Installer database that installs ODBC drivers and translators.</span></span>

    <span data-ttu-id="cb56b-288">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-288">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-289">Tabela ODBCattribute</span><span class="sxs-lookup"><span data-stu-id="cb56b-289">ODBCAttribute Table</span></span>](odbcattribute-table.md)
    -   [<span data-ttu-id="cb56b-290">Tabela ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="cb56b-290">ODBCDriver Table</span></span>](odbcdriver-table.md)
    -   [<span data-ttu-id="cb56b-291">Tabela ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="cb56b-291">ODBCTranslator Table</span></span>](odbctranslator-table.md)
    -   [<span data-ttu-id="cb56b-292">Tabela ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="cb56b-292">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
    -   [<span data-ttu-id="cb56b-293">Tabela ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="cb56b-293">ODBCSourceAttribute Table</span></span>](odbcsourceattribute-table.md)

-   <span data-ttu-id="cb56b-294">Crie um banco de dados Windows Installer que instala MIME.</span><span class="sxs-lookup"><span data-stu-id="cb56b-294">Author a Windows Installer database that installs MIME.</span></span>

    <span data-ttu-id="cb56b-295">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-295">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-296">Tabela MIME</span><span class="sxs-lookup"><span data-stu-id="cb56b-296">MIME Table</span></span>](mime-table.md)
    -   [<span data-ttu-id="cb56b-297">Tabela de extensão</span><span class="sxs-lookup"><span data-stu-id="cb56b-297">Extension Table</span></span>](extension-table.md)
    -   [<span data-ttu-id="cb56b-298">Modificando o registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-298">Modifying the Registry</span></span>](modifying-the-registry.md)

-   <span data-ttu-id="cb56b-299">Crie um banco de dados Windows Installer que instala variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="cb56b-299">Author a Windows Installer database that installs environment variables.</span></span>

    <span data-ttu-id="cb56b-300">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-300">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-301">Tabela de ambiente</span><span class="sxs-lookup"><span data-stu-id="cb56b-301">Environment Table</span></span>](environment-table.md)

-   <span data-ttu-id="cb56b-302">Crie um banco de dados Windows Installer que instala atalhos.</span><span class="sxs-lookup"><span data-stu-id="cb56b-302">Author a Windows Installer database that installs shortcuts.</span></span>

    <span data-ttu-id="cb56b-303">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-303">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-304">Tabela de atalho</span><span class="sxs-lookup"><span data-stu-id="cb56b-304">Shortcut Table</span></span>](shortcut-table.md)
    -   [<span data-ttu-id="cb56b-305">Tabela MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="cb56b-305">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
    -   [<span data-ttu-id="cb56b-306">Editando atalhos do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-306">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="cb56b-307">Exemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-307">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="cb56b-308">Crie um banco de dados Windows Installer que instala várias instâncias de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="cb56b-308">Author a Windows Installer database that installs multiple instances of applications.</span></span>

    <span data-ttu-id="cb56b-309">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-309">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-310">Instalando várias instâncias de produtos e patches</span><span class="sxs-lookup"><span data-stu-id="cb56b-310">Installing Multiple Instances of Products and Patches</span></span>](installing-multiple-instances-of-products-and-patches.md)
    -   [<span data-ttu-id="cb56b-311">Criando várias instâncias com transformações de instância</span><span class="sxs-lookup"><span data-stu-id="cb56b-311">Authoring Multiple Instances with Instance Transforms</span></span>](authoring-multiple-instances-with-instance-transforms.md)
    -   [<span data-ttu-id="cb56b-312">Instalando várias instâncias com transformações de instância</span><span class="sxs-lookup"><span data-stu-id="cb56b-312">Installing Multiple Instances with Instance Transforms</span></span>](installing-multiple-instances-with-instance-transforms.md)

-   <span data-ttu-id="cb56b-313">Especifique opções e Estados de seleção de recursos padrão.</span><span class="sxs-lookup"><span data-stu-id="cb56b-313">Specify default feature selection states and options.</span></span>

    <span data-ttu-id="cb56b-314">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-314">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-315">Grupo de tabelas principais</span><span class="sxs-lookup"><span data-stu-id="cb56b-315">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="cb56b-316">Tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-316">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="cb56b-317">Tabela de recursos</span><span class="sxs-lookup"><span data-stu-id="cb56b-317">Feature Table</span></span>](feature-table.md)
    -   [<span data-ttu-id="cb56b-318">Tabela FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="cb56b-318">FeatureComponents Table</span></span>](featurecomponents-table.md)
    -   [<span data-ttu-id="cb56b-319">Controlando Estados de seleção de recursos</span><span class="sxs-lookup"><span data-stu-id="cb56b-319">Controlling Feature Selection States</span></span>](controlling-feature-selection-states.md)
    -   [<span data-ttu-id="cb56b-320">Propriedades de opções de instalação de recurso</span><span class="sxs-lookup"><span data-stu-id="cb56b-320">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="cb56b-321">Especifique as condições que devem ser atendidas para instalar um aplicativo ou componentes selecionados.</span><span class="sxs-lookup"><span data-stu-id="cb56b-321">Specify conditions that must be met to install an application or selected components.</span></span>

    <span data-ttu-id="cb56b-322">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-322">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-323">Tabela de condição</span><span class="sxs-lookup"><span data-stu-id="cb56b-323">Condition Table</span></span>](condition-table.md)
    -   [<span data-ttu-id="cb56b-324">Tabela LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="cb56b-324">LaunchCondition Table</span></span>](launchcondition-table.md)
    -   [<span data-ttu-id="cb56b-325">Tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-325">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="cb56b-326">Usando propriedades em instruções condicionais</span><span class="sxs-lookup"><span data-stu-id="cb56b-326">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="cb56b-327">Sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="cb56b-327">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="cb56b-328">Ações de condicionamento a serem executadas durante a remoção</span><span class="sxs-lookup"><span data-stu-id="cb56b-328">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="cb56b-329">Exemplos de sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="cb56b-329">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)

-   <span data-ttu-id="cb56b-330">Crie a sequência de ações usadas para instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cb56b-330">Author the sequence of actions used to install the application.</span></span>

    <span data-ttu-id="cb56b-331">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-331">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-332">Usando uma tabela de sequência</span><span class="sxs-lookup"><span data-stu-id="cb56b-332">Using a Sequence Table</span></span>](using-a-sequence-table.md)
    -   [<span data-ttu-id="cb56b-333">Grupo de tabelas de procedimento de instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-333">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)
    -   [<span data-ttu-id="cb56b-334">Exemplo detalhado da tabela de sequência</span><span class="sxs-lookup"><span data-stu-id="cb56b-334">Sequence Table Detailed Example</span></span>](sequence-table-detailed-example.md)
    -   [<span data-ttu-id="cb56b-335">Ações com restrições de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="cb56b-335">Actions with Sequencing Restrictions</span></span>](actions-with-sequencing-restrictions.md)
    -   [<span data-ttu-id="cb56b-336">Ações sem restrições de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="cb56b-336">Actions without Sequencing Restrictions</span></span>](actions-without-sequencing-restrictions.md)
    -   [<span data-ttu-id="cb56b-337">Usando propriedades em instruções condicionais</span><span class="sxs-lookup"><span data-stu-id="cb56b-337">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="cb56b-338">Sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="cb56b-338">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="cb56b-339">Exemplos de sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="cb56b-339">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
    -   [<span data-ttu-id="cb56b-340">Ações de condicionamento a serem executadas durante a remoção</span><span class="sxs-lookup"><span data-stu-id="cb56b-340">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="cb56b-341">Ações padrão</span><span class="sxs-lookup"><span data-stu-id="cb56b-341">Standard Actions</span></span>](standard-actions.md)
    -   [<span data-ttu-id="cb56b-342">Exemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-342">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="cb56b-343">Prepare o pacote de instalação do aplicativo para atualizações futuras do aplicativo pelo serviço de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-343">Prepare the installation package of the application for future upgrades of the application by the Windows Installer service.</span></span>

    <span data-ttu-id="cb56b-344">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-344">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-345">Aplicação de patch e atualizações</span><span class="sxs-lookup"><span data-stu-id="cb56b-345">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="cb56b-346">Preparando um aplicativo para atualizações principais futuras</span><span class="sxs-lookup"><span data-stu-id="cb56b-346">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
    -   [<span data-ttu-id="cb56b-347">Usando um UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="cb56b-347">Using an UpgradeCode</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="cb56b-348">Atualizar tabela</span><span class="sxs-lookup"><span data-stu-id="cb56b-348">Upgrade Table</span></span>](upgrade-table.md)
    -   [<span data-ttu-id="cb56b-349">**Propriedade UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="cb56b-349">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="cb56b-350">Impedindo que um pacote antigo seja instalado em uma versão mais recente</span><span class="sxs-lookup"><span data-stu-id="cb56b-350">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [<span data-ttu-id="cb56b-351">Alterando o código do produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-351">Changing the Product Code</span></span>](changing-the-product-code.md)
    -   [<span data-ttu-id="cb56b-352">Atualizando assemblies</span><span class="sxs-lookup"><span data-stu-id="cb56b-352">Updating Assemblies</span></span>](updating-assemblies.md)
    -   [<span data-ttu-id="cb56b-353">Exemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-353">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="cb56b-354">Solucionar problemas Windows Installer pacotes em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="cb56b-354">Troubleshoot Windows Installer packages under development.</span></span>

    <span data-ttu-id="cb56b-355">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-355">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-356">Validação do pacote</span><span class="sxs-lookup"><span data-stu-id="cb56b-356">Package Validation</span></span>](package-validation.md)
    -   [<span data-ttu-id="cb56b-357">Avaliadores de consistência internos-ICEs</span><span class="sxs-lookup"><span data-stu-id="cb56b-357">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
    -   [<span data-ttu-id="cb56b-358">Log de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-358">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="cb56b-359">Verificando a instalação de recursos, componentes, arquivos</span><span class="sxs-lookup"><span data-stu-id="cb56b-359">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="cb56b-360">Criando um pacote grande</span><span class="sxs-lookup"><span data-stu-id="cb56b-360">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="cb56b-361">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="cb56b-361">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="cb56b-362">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-362">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="cb56b-363">Validando módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="cb56b-363">Validating Merge Modules</span></span>](validating-merge-modules.md)
    -   [<span data-ttu-id="cb56b-364">Validando um banco de dados de instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-364">Validating an Installation Database</span></span>](validating-an-installation-database.md)
    -   [<span data-ttu-id="cb56b-365">Validando uma atualização de instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-365">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)
    -   [<span data-ttu-id="cb56b-366">Pesquisando um componente ou recurso desfeito</span><span class="sxs-lookup"><span data-stu-id="cb56b-366">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="cb56b-367">Windows Installer mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="cb56b-367">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="cb56b-368">Registro em log de solicitações de reinicialização</span><span class="sxs-lookup"><span data-stu-id="cb56b-368">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="cb56b-369">Garanta uma instalação e instalação seguras do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cb56b-369">Ensure a secure setup and installation of the application.</span></span>

    <span data-ttu-id="cb56b-370">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-370">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-371">Diretrizes para a criação de instalações seguras</span><span class="sxs-lookup"><span data-stu-id="cb56b-371">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="cb56b-372">Diretrizes para proteger ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="cb56b-372">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="cb56b-373">Segurança de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="cb56b-373">Custom Action Security</span></span>](custom-action-security.md)
    -   [<span data-ttu-id="cb56b-374">Diretrizes para proteger pacotes em computadores bloqueados</span><span class="sxs-lookup"><span data-stu-id="cb56b-374">Guidelines for Securing Packages on Locked-Down Computers</span></span>](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [<span data-ttu-id="cb56b-375">Criando uma instalação assinada totalmente verificada usando a automação</span><span class="sxs-lookup"><span data-stu-id="cb56b-375">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [<span data-ttu-id="cb56b-376">Um exemplo de instalação do Windows Installer baseado em URL</span><span class="sxs-lookup"><span data-stu-id="cb56b-376">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="cb56b-377">Criando a interface do usuário para entrada de senha</span><span class="sxs-lookup"><span data-stu-id="cb56b-377">Authoring the User Interface for Password Input</span></span>](authoring-the-user-interface-for-password-input.md)
    -   [<span data-ttu-id="cb56b-378">Assinaturas digitais e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-378">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
    -   [<span data-ttu-id="cb56b-379">Usando Windows Installer com o UAC</span><span class="sxs-lookup"><span data-stu-id="cb56b-379">Using Windows Installer with UAC</span></span>](using-windows-installer-with-uac.md)
    -   [<span data-ttu-id="cb56b-380">Aplicação de patch de UAC (controle de conta de usuário)</span><span class="sxs-lookup"><span data-stu-id="cb56b-380">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
    -   [<span data-ttu-id="cb56b-381">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="cb56b-381">Msicert.exe</span></span>](msicert-exe.md)
    -   [<span data-ttu-id="cb56b-382">**Propriedade AdminUser**</span><span class="sxs-lookup"><span data-stu-id="cb56b-382">**AdminUser property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="cb56b-383">**Propriedade privilegiada**</span><span class="sxs-lookup"><span data-stu-id="cb56b-383">**Privileged property**</span></span>](privileged.md)
    -   [<span data-ttu-id="cb56b-384">**Propriedade SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="cb56b-384">**SecureCustomProperties property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="cb56b-385">Crie uma interface do usuário para apresentar opções para configurar a instalação e obter informações do usuário sobre o processo de instalação pendente.</span><span class="sxs-lookup"><span data-stu-id="cb56b-385">Create a user interface to present options to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="cb56b-386">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-386">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-387">Sobre a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="cb56b-387">About the User Interface</span></span>](about-the-user-interface.md)
    -   [<span data-ttu-id="cb56b-388">Adicionando controles e texto</span><span class="sxs-lookup"><span data-stu-id="cb56b-388">Adding Controls and Text</span></span>](adding-controls-and-text.md)
    -   [<span data-ttu-id="cb56b-389">Criando um controle ProgressBar</span><span class="sxs-lookup"><span data-stu-id="cb56b-389">Authoring a ProgressBar Control</span></span>](authoring-a-progressbar-control.md)
    -   [<span data-ttu-id="cb56b-390">Criando mensagens de prompt de disco</span><span class="sxs-lookup"><span data-stu-id="cb56b-390">Authoring Disk Prompt Messages</span></span>](authoring-disk-prompt-messages.md)
    -   [<span data-ttu-id="cb56b-391">Criando uma condicional "Aguarde..." Caixa de mensagem</span><span class="sxs-lookup"><span data-stu-id="cb56b-391">Authoring a Conditional "Please Wait . . ." Message Box</span></span>](authoring-a-conditional-please-wait-------message-box.md)
    -   [<span data-ttu-id="cb56b-392">Visualizando a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="cb56b-392">Previewing the User Interface</span></span>](previewing-the-user-interface.md)
    -   [<span data-ttu-id="cb56b-393">Adicionando texto armazenado em uma propriedade</span><span class="sxs-lookup"><span data-stu-id="cb56b-393">Adding Text Stored in a Property</span></span>](adding-text-stored-in-a-property.md)
    -   [<span data-ttu-id="cb56b-394">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="cb56b-394">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   <span data-ttu-id="cb56b-395">Crie uma interface de usuário externa para apresentar uma interface de usuário personalizada para configurar a instalação e obter informações do usuário sobre o processo de instalação pendente.</span><span class="sxs-lookup"><span data-stu-id="cb56b-395">Create an external user interface to present a custom user interface to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="cb56b-396">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-396">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-397">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="cb56b-397">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [<span data-ttu-id="cb56b-398">Monitorando uma instalação usando o MsiSetExternalUIRecord</span><span class="sxs-lookup"><span data-stu-id="cb56b-398">Monitoring an Installation Using MsiSetExternalUIRecord</span></span>](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [<span data-ttu-id="cb56b-399">Analisando mensagens de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-399">Parsing Windows Installer Messages</span></span>](parsing-windows-installer-messages.md)
    -   [<span data-ttu-id="cb56b-400">Retornando valores de um manipulador de interface do usuário externo</span><span class="sxs-lookup"><span data-stu-id="cb56b-400">Returning Values from an External User Interface Handler</span></span>](returning-values-from-an-external-user-interface-handler.md)
    -   [<span data-ttu-id="cb56b-401">manipulador de INSTALLUI \_</span><span class="sxs-lookup"><span data-stu-id="cb56b-401">INSTALLUI\_HANDLER</span></span>](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [<span data-ttu-id="cb56b-402">Manipulando mensagens de progresso usando MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="cb56b-402">Handling Progress Messages Using MsiSetExternalUI</span></span>](handling-progress-messages-using-msisetexternalui.md)
    -   [<span data-ttu-id="cb56b-403">Monitorando uma instalação usando o MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="cb56b-403">Monitoring an Installation Using MsiSetExternalUI</span></span>](monitoring-an-installation-using-msisetexternalui.md)

-   <span data-ttu-id="cb56b-404">Definir informações para o aplicativo em **Adicionar/remover programas** (ARP.)</span><span class="sxs-lookup"><span data-stu-id="cb56b-404">Set information for the application in **Add/Remove Programs** (ARP.)</span></span>

    <span data-ttu-id="cb56b-405">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-405">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-406">Configurando adicionar/remover programas com Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-406">Configuring Add/Remove Programs with Windows Installer</span></span>](configuring-add-remove-programs-with-windows-installer.md)
    -   [<span data-ttu-id="cb56b-407">Adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-407">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="cb56b-408">Desinstalar chave do registro</span><span class="sxs-lookup"><span data-stu-id="cb56b-408">Uninstall Registry Key</span></span>](uninstall-registry-key.md)

-   <span data-ttu-id="cb56b-409">Grave ações personalizadas para lidar com a lógica de instalação que não tem suporte nativo do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-409">Write custom actions to handle setup logic that is not natively supported by Windows Installer.</span></span>

    <span data-ttu-id="cb56b-410">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-410">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-411">Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="cb56b-411">Custom Actions</span></span>](custom-actions.md)
    -   [<span data-ttu-id="cb56b-412">Lista de Resumo de todos os tipos de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="cb56b-412">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)
    -   [<span data-ttu-id="cb56b-413">Diretrizes para proteger ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="cb56b-413">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="cb56b-414">Referência de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="cb56b-414">Custom Action Reference</span></span>](custom-action-reference.md)
    -   [<span data-ttu-id="cb56b-415">Usando uma ação personalizada para criar contas de usuário em um computador local</span><span class="sxs-lookup"><span data-stu-id="cb56b-415">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="cb56b-416">Usando uma ação personalizada para iniciar um arquivo instalado no final da instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-416">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [<span data-ttu-id="cb56b-417">Acessando um banco de dados ou sessão de dentro de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="cb56b-417">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="cb56b-418">Acessando a sessão do instalador atual de dentro de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="cb56b-418">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="cb56b-419">Alterando o estado do sistema usando uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="cb56b-419">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)

-   <span data-ttu-id="cb56b-420">Inicialize o Windows Installer no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="cb56b-420">Bootstrap the Windows Installer onto a user's computer.</span></span>

    <span data-ttu-id="cb56b-421">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-421">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-422">Inicialização</span><span class="sxs-lookup"><span data-stu-id="cb56b-422">Bootstrapping</span></span>](bootstrapping.md)
    -   [<span data-ttu-id="cb56b-423">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="cb56b-423">Instmsi.exe</span></span>](instmsi-exe.md)
    -   [<span data-ttu-id="cb56b-424">Inicialização de download da Internet</span><span class="sxs-lookup"><span data-stu-id="cb56b-424">Internet Download Bootstrapping</span></span>](internet-download-bootstrapping.md)
    -   [<span data-ttu-id="cb56b-425">Msistuff.exe</span><span class="sxs-lookup"><span data-stu-id="cb56b-425">Msistuff.exe</span></span>](msistuff-exe.md)
    -   [<span data-ttu-id="cb56b-426">Um exemplo de instalação do Windows Installer baseado em URL</span><span class="sxs-lookup"><span data-stu-id="cb56b-426">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="cb56b-427">Configurando os recursos de Setup.exe</span><span class="sxs-lookup"><span data-stu-id="cb56b-427">Configuring the Setup.exe Resources</span></span>](configuring-the-setup-exe-resources.md)
    -   [<span data-ttu-id="cb56b-428">Baixando uma instalação da Internet</span><span class="sxs-lookup"><span data-stu-id="cb56b-428">Downloading an Installation from the Internet</span></span>](downloading-an-installation-from-the-internet.md)

-   <span data-ttu-id="cb56b-429">Siga as diretrizes de Acessibilidade Ativa ao gravar Windows Installer pacotes.</span><span class="sxs-lookup"><span data-stu-id="cb56b-429">Adhere to Active Accessibility guidelines when writing Windows Installer packages.</span></span>

    <span data-ttu-id="cb56b-430">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-430">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-431">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="cb56b-431">Accessibility</span></span>](accessibility.md)

-   <span data-ttu-id="cb56b-432">Prepare-se para a internacionalização de uma instalação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cb56b-432">Prepare for the internationalization of an application setup.</span></span>

    <span data-ttu-id="cb56b-433">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-433">For more information, see the following:</span></span>

    -   <span data-ttu-id="cb56b-434">[Preparando um pacote de Windows Installer para localização](preparing-a-windows-installer-package-for-localization.md),</span><span class="sxs-lookup"><span data-stu-id="cb56b-434">[Preparing a Windows Installer Package for Localization](preparing-a-windows-installer-package-for-localization.md),</span></span>
    -   [<span data-ttu-id="cb56b-435">Localizando um pacote de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-435">Localizing a Windows Installer Package</span></span>](localizing-a-windows-installer-package.md)
    -   [<span data-ttu-id="cb56b-436">Manipulação de página de código (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="cb56b-436">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
    -   [<span data-ttu-id="cb56b-437">Adicionando recursos localizados</span><span class="sxs-lookup"><span data-stu-id="cb56b-437">Adding Localized Resources</span></span>](adding-localized-resources.md)
    -   [<span data-ttu-id="cb56b-438">Um exemplo de localização</span><span class="sxs-lookup"><span data-stu-id="cb56b-438">A Localization Example</span></span>](a-localization-example.md)
    -   [<span data-ttu-id="cb56b-439">Localizando as tabelas Error e ActionText</span><span class="sxs-lookup"><span data-stu-id="cb56b-439">Localizing the Error and ActionText Tables</span></span>](localizing-the-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="cb56b-440">Localizando colunas de banco de dados</span><span class="sxs-lookup"><span data-stu-id="cb56b-440">Localizing Database Columns</span></span>](localizing-database-columns.md)
    -   [<span data-ttu-id="cb56b-441">Criando um banco de dados com uma página de código neutra</span><span class="sxs-lookup"><span data-stu-id="cb56b-441">Creating a Database with a Neutral Code Page</span></span>](creating-a-database-with-a-neutral-code-page.md)
    -   [<span data-ttu-id="cb56b-442">Manipulação de página de código de tabelas importadas e exportadas</span><span class="sxs-lookup"><span data-stu-id="cb56b-442">Code Page Handling of Imported and Exported Tables</span></span>](code-page-handling-of-imported-and-exported-tables.md)
    -   [<span data-ttu-id="cb56b-443">Localizando o idioma exibido por caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="cb56b-443">Localizing the Language Displayed by Dialogs</span></span>](localizing-the-language-displayed-by-dialogs.md)
    -   [<span data-ttu-id="cb56b-444">Importando tabelas de erro e ActionText localizadas</span><span class="sxs-lookup"><span data-stu-id="cb56b-444">Importing Localized Error and ActionText Tables</span></span>](importing-localized-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="cb56b-445">Atualizando Propriedades ProductLanguage e ProductCode</span><span class="sxs-lookup"><span data-stu-id="cb56b-445">Updating ProductLanguage and ProductCode Properties</span></span>](updating-productlanguage-and-productcode-properties.md)
    -   [<span data-ttu-id="cb56b-446">Atualizando um fluxo de informações de resumo</span><span class="sxs-lookup"><span data-stu-id="cb56b-446">Updating a Summary Information Stream</span></span>](updating-a-summary-information-stream.md)
    -   [<span data-ttu-id="cb56b-447">Componentes qualificados</span><span class="sxs-lookup"><span data-stu-id="cb56b-447">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="cb56b-448">Tabela UIText</span><span class="sxs-lookup"><span data-stu-id="cb56b-448">UIText Table</span></span>](uitext-table.md)
    -   [<span data-ttu-id="cb56b-449">Gerenciar idioma e página de código</span><span class="sxs-lookup"><span data-stu-id="cb56b-449">Manage Language and Codepage</span></span>](manage-language-and-codepage.md)
    -   [<span data-ttu-id="cb56b-450">Verificando a página de código do banco de dados de instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-450">Checking the Installation Database Code Page</span></span>](checking-the-installation-database-code-page.md)

-   <span data-ttu-id="cb56b-451">Crie pacotes de Windows Installer para plataformas de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cb56b-451">Create Windows Installer packages for 32-bit and 64-bit platforms.</span></span>

    <span data-ttu-id="cb56b-452">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-452">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-453">Windows Installer em sistemas operacionais de 64 bits</span><span class="sxs-lookup"><span data-stu-id="cb56b-453">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="cb56b-454">Ações personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="cb56b-454">64-Bit Custom Actions</span></span>](64-bit-custom-actions.md)
    -   [<span data-ttu-id="cb56b-455">Usando ações personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="cb56b-455">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)
    -   [<span data-ttu-id="cb56b-456">Usando módulos de mesclagem de 64 bits</span><span class="sxs-lookup"><span data-stu-id="cb56b-456">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)

-   <span data-ttu-id="cb56b-457">Redistribua os componentes de Windows Installer compartilhados e a lógica de instalação como módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="cb56b-457">Redistribute shared Windows Installer components and setup logic as merge modules.</span></span>

    <span data-ttu-id="cb56b-458">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-458">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-459">Mesclar módulos</span><span class="sxs-lookup"><span data-stu-id="cb56b-459">Merge Modules</span></span>](merge-modules.md)
    -   [<span data-ttu-id="cb56b-460">Criando uma transformação de idioma para um módulo de mesclagem de vários idiomas</span><span class="sxs-lookup"><span data-stu-id="cb56b-460">Authoring a Language Transform for a Multiple Language Merge Module</span></span>](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [<span data-ttu-id="cb56b-461">Aplicando um módulo de mesclagem configurável com personalizações</span><span class="sxs-lookup"><span data-stu-id="cb56b-461">Applying a Configurable Merge Module with Customizations</span></span>](applying-a-configurable-merge-module-with-customizations.md)

-   <span data-ttu-id="cb56b-462">Agendar ou suprimir reinicializações durante uma instalação de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-462">Schedule or suppress reboots during a Windows Installer installation.</span></span>

    <span data-ttu-id="cb56b-463">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-463">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-464">Reinicializações do sistema</span><span class="sxs-lookup"><span data-stu-id="cb56b-464">System Reboots</span></span>](system-reboots.md)
    -   [<span data-ttu-id="cb56b-465">Registro em log de solicitações de reinicialização</span><span class="sxs-lookup"><span data-stu-id="cb56b-465">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="cb56b-466">Crie atualizações ou correções para um aplicativo existente criando um patch.</span><span class="sxs-lookup"><span data-stu-id="cb56b-466">Create updates or fixes for an existing application by creating a patch.</span></span>

    <span data-ttu-id="cb56b-467">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-467">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-468">Criando um patch de atualização pequena</span><span class="sxs-lookup"><span data-stu-id="cb56b-468">Creating a Small Update Patch</span></span>](creating-a-small-update-patch.md)
    -   [<span data-ttu-id="cb56b-469">Um exemplo de aplicação de patch de atualização pequena</span><span class="sxs-lookup"><span data-stu-id="cb56b-469">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

-   <span data-ttu-id="cb56b-470">Crie um pacote de uso duplo que seja capaz de instalar um aplicativo somente para o usuário atual ou para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="cb56b-470">Author a dual-purpose package capable of installing an application either for only the current user or for all users of the computer.</span></span>

    <span data-ttu-id="cb56b-471">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-471">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-472">Contexto de instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-472">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="cb56b-473">Criação de pacote único</span><span class="sxs-lookup"><span data-stu-id="cb56b-473">Single Package Authoring</span></span>](single-package-authoring.md)
    -   [<span data-ttu-id="cb56b-474">Exemplo de criação de pacote único</span><span class="sxs-lookup"><span data-stu-id="cb56b-474">Single Package Authoring Example</span></span>](single-package-authoring-example.md)

-   <span data-ttu-id="cb56b-475">Personalize os serviços no computador usando o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-475">Customize services on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="cb56b-476">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-476">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-477">Usando a configuração de serviços</span><span class="sxs-lookup"><span data-stu-id="cb56b-477">Using Services Configuration</span></span>](using-services-configuration.md)

-   <span data-ttu-id="cb56b-478">Proteja os recursos no computador usando o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-478">Secure resources on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="cb56b-479">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-479">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-480">Diretrizes para a criação de instalações seguras</span><span class="sxs-lookup"><span data-stu-id="cb56b-480">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="cb56b-481">Protegendo recursos</span><span class="sxs-lookup"><span data-stu-id="cb56b-481">Securing Resources</span></span>](securing-resources-.md)

-   <span data-ttu-id="cb56b-482">Enumere todos os componentes instalados no computador e obtenha o caminho de chave para o componente.</span><span class="sxs-lookup"><span data-stu-id="cb56b-482">Enumerate all components installed on the computer and obtain the key path for the component.</span></span>

    <span data-ttu-id="cb56b-483">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-483">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-484">Enumerando componentes</span><span class="sxs-lookup"><span data-stu-id="cb56b-484">Enumerating Components</span></span>](enumerating-components-.md)

-   <span data-ttu-id="cb56b-485">Instale vários pacotes usando o [*processamento de transações*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cb56b-485">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="cb56b-486">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-486">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-487">Instalações de vários pacotes</span><span class="sxs-lookup"><span data-stu-id="cb56b-487">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="cb56b-488">Insira uma interface do usuário personalizada no pacote Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-488">Embed a custom user interface in the Windows Installer package.</span></span>

    <span data-ttu-id="cb56b-489">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-489">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-490">Usando a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="cb56b-490">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="cb56b-491">Usando uma interface do usuário inserida</span><span class="sxs-lookup"><span data-stu-id="cb56b-491">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="it-professionals"></a><span data-ttu-id="cb56b-492">Profissionais de TI</span><span class="sxs-lookup"><span data-stu-id="cb56b-492">IT Professionals</span></span>

<span data-ttu-id="cb56b-493">Os profissionais de ti e os administradores personalizam e implantam pacotes de Windows Installer existentes.</span><span class="sxs-lookup"><span data-stu-id="cb56b-493">IT Professionals and Administrators customize and deploy existing Windows Installer packages.</span></span> <span data-ttu-id="cb56b-494">Esses usuários reempacotam as configurações para aplicativos existentes em Windows Installer pacotes de instalação e instalam e mantêm imagens administrativas de Windows Installer instalações em redes.</span><span class="sxs-lookup"><span data-stu-id="cb56b-494">These users repackage setups for existing applications into Windows Installer installation packages, and install and maintain administrative images of Windows Installer installations on networks.</span></span>

-   <span data-ttu-id="cb56b-495">Personalizar os aplicativos e a instalação gerando e aplicando transformações Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-495">Customize applications and setup by generating and applying Windows Installer transforms</span></span>

    <span data-ttu-id="cb56b-496">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-496">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-497">Personalização</span><span class="sxs-lookup"><span data-stu-id="cb56b-497">Customization</span></span>](customization.md)
    -   [<span data-ttu-id="cb56b-498">Transformações de banco de dados</span><span class="sxs-lookup"><span data-stu-id="cb56b-498">Database Transforms</span></span>](database-transforms.md)
    -   [<span data-ttu-id="cb56b-499">Um exemplo de transformação de personalização</span><span class="sxs-lookup"><span data-stu-id="cb56b-499">A Customization Transform Example</span></span>](a-customization-transform-example.md)
    -   [<span data-ttu-id="cb56b-500">Mesclagens e transformações</span><span class="sxs-lookup"><span data-stu-id="cb56b-500">Merges and Transforms</span></span>](merges-and-transforms.md)
    -   [<span data-ttu-id="cb56b-501">Usando transformações para adicionar recursos</span><span class="sxs-lookup"><span data-stu-id="cb56b-501">Using Transforms to Add Resources</span></span>](using-transforms-to-add-resources.md)
    -   [<span data-ttu-id="cb56b-502">Gerar uma transformação</span><span class="sxs-lookup"><span data-stu-id="cb56b-502">Generate a Transform</span></span>](generate-a-transform.md)
    -   [<span data-ttu-id="cb56b-503">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="cb56b-503">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="cb56b-504">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="cb56b-504">Msitran.exe</span></span>](msitran-exe.md)
    -   [<span data-ttu-id="cb56b-505">Aplicar uma transformação</span><span class="sxs-lookup"><span data-stu-id="cb56b-505">Apply a Transform</span></span>](apply-a-transform.md)
    -   [<span data-ttu-id="cb56b-506">Exibir uma transformação</span><span class="sxs-lookup"><span data-stu-id="cb56b-506">View a Transform</span></span>](view-a-transform.md)
    -   [<span data-ttu-id="cb56b-507">Exibir diferenças entre dois bancos de dados</span><span class="sxs-lookup"><span data-stu-id="cb56b-507">View Differences Between Two Databases</span></span>](view-differences-between-two-databases.md)
    -   [<span data-ttu-id="cb56b-508">Aplicação de patch em aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="cb56b-508">Patching Customized Applications</span></span>](patching-customized-applications.md)

-   <span data-ttu-id="cb56b-509">Implante um pacote de instalação Windows Installer, atualização ou patch.</span><span class="sxs-lookup"><span data-stu-id="cb56b-509">Deploy a Windows Installer installation package, update, or patch.</span></span>

    <span data-ttu-id="cb56b-510">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-510">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-511">Instalando um aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb56b-511">Installing an Application</span></span>](installing-an-application.md)
    -   [<span data-ttu-id="cb56b-512">Aplicação de patch e atualizações</span><span class="sxs-lookup"><span data-stu-id="cb56b-512">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="cb56b-513">Transformações</span><span class="sxs-lookup"><span data-stu-id="cb56b-513">Transforms</span></span>](transforms.md)
    -   [<span data-ttu-id="cb56b-514">Instalando um pacote com privilégios elevados para um não administrador</span><span class="sxs-lookup"><span data-stu-id="cb56b-514">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="cb56b-515">Aplicando as principais atualizações por meio da aplicação de patch na instalação local do produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-515">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="cb56b-516">Aplicando as principais atualizações instalando o produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-516">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="cb56b-517">Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-517">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="cb56b-518">Aplicando pequenas atualizações reinstalando o produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-518">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="cb56b-519">Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa</span><span class="sxs-lookup"><span data-stu-id="cb56b-519">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="cb56b-520">Aplicação de patch nas instalações iniciais</span><span class="sxs-lookup"><span data-stu-id="cb56b-520">Patching Initial Installations</span></span>](patching-initial-installations.md)
    -   [<span data-ttu-id="cb56b-521">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="cb56b-521">Command Line Options</span></span>](command-line-options.md)

-   <span data-ttu-id="cb56b-522">Solucionar problemas de pacotes Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-522">Troubleshoot Windows Installer packages.</span></span>

    <span data-ttu-id="cb56b-523">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-523">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-524">Log de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-524">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="cb56b-525">Verificando a instalação de recursos, componentes, arquivos</span><span class="sxs-lookup"><span data-stu-id="cb56b-525">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="cb56b-526">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="cb56b-526">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="cb56b-527">Pesquisando um componente ou recurso desfeito</span><span class="sxs-lookup"><span data-stu-id="cb56b-527">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="cb56b-528">Windows Installer mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="cb56b-528">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="cb56b-529">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="cb56b-529">Msicert.exe</span></span>](msicert-exe.md)

-   <span data-ttu-id="cb56b-530">Use scripts para consultar Windows Installer pacotes para obter informações sobre um produto e modificar a instalação.</span><span class="sxs-lookup"><span data-stu-id="cb56b-530">Use scripting to query Windows Installer packages for information about a product and modify the installation.</span></span>

    <span data-ttu-id="cb56b-531">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-531">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-532">Interface de automação</span><span class="sxs-lookup"><span data-stu-id="cb56b-532">Automation Interface</span></span>](automation-interface.md)
    -   [<span data-ttu-id="cb56b-533">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb56b-533">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
    -   [<span data-ttu-id="cb56b-534">Usando Windows Installer com WMI</span><span class="sxs-lookup"><span data-stu-id="cb56b-534">Using Windows Installer with WMI</span></span>](using-windows-installer-with-wmi.md)

-   <span data-ttu-id="cb56b-535">Crie e mantenha instalações administrativas.</span><span class="sxs-lookup"><span data-stu-id="cb56b-535">Create and maintain administrative installations.</span></span>

    <span data-ttu-id="cb56b-536">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-536">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-537">Instalação administrativa</span><span class="sxs-lookup"><span data-stu-id="cb56b-537">Administrative Installation</span></span>](administrative-installation.md)
    -   [<span data-ttu-id="cb56b-538">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="cb56b-538">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="cb56b-539">**Propriedade adminproperties**</span><span class="sxs-lookup"><span data-stu-id="cb56b-539">**AdminProperties Property**</span></span>](adminproperties.md)
    -   [<span data-ttu-id="cb56b-540">Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa</span><span class="sxs-lookup"><span data-stu-id="cb56b-540">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="cb56b-541">Aplicando um pacote de patch a uma instalação administrativa</span><span class="sxs-lookup"><span data-stu-id="cb56b-541">Applying a Patch Package to an Administrative Installation</span></span>](applying-a-patch-package-to-an-administrative-installation.md)
    -   [<span data-ttu-id="cb56b-542">Ordem de execução da ação</span><span class="sxs-lookup"><span data-stu-id="cb56b-542">Action Execution Order</span></span>](action-execution-order.md)
    -   [<span data-ttu-id="cb56b-543">**Propriedade IsAdminPackage**</span><span class="sxs-lookup"><span data-stu-id="cb56b-543">**IsAdminPackage Property**</span></span>](isadminpackage.md)
    -   [<span data-ttu-id="cb56b-544">Ordem de precedência de propriedade</span><span class="sxs-lookup"><span data-stu-id="cb56b-544">Order of Property Precedence</span></span>](order-of-property-precedence.md)
    -   [<span data-ttu-id="cb56b-545">**Propriedade adminproperties**</span><span class="sxs-lookup"><span data-stu-id="cb56b-545">**AdminProperties Property**</span></span>](adminproperties.md)

-   <span data-ttu-id="cb56b-546">Disponibilizar um aplicativo para todos os usuários de um computador ou apenas para um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="cb56b-546">Make an application available to all users of a computer or to a specified user only.</span></span>

    <span data-ttu-id="cb56b-547">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-547">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-548">Contexto de instalação</span><span class="sxs-lookup"><span data-stu-id="cb56b-548">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="cb56b-549">**Propriedade ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="cb56b-549">**ALLUSERS Property**</span></span>](allusers.md)

-   <span data-ttu-id="cb56b-550">Interprete pacotes, instale produtos e configure opções de recursos usando uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="cb56b-550">Interpret packages, install products, and configure feature options using a command line.</span></span>

    <span data-ttu-id="cb56b-551">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-551">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-552">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="cb56b-552">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="cb56b-553">Definindo valores de propriedade pública na linha de comando</span><span class="sxs-lookup"><span data-stu-id="cb56b-553">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
    -   [<span data-ttu-id="cb56b-554">Obtendo e definindo propriedades</span><span class="sxs-lookup"><span data-stu-id="cb56b-554">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
    -   [<span data-ttu-id="cb56b-555">Reinstalando um recurso ou aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb56b-555">Reinstalling a Feature or Application</span></span>](reinstalling-a-feature-or-application.md)
    -   [<span data-ttu-id="cb56b-556">Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-556">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="cb56b-557">Aplicando pequenas atualizações reinstalando o produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-557">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="cb56b-558">Alterando o local de destino de um diretório</span><span class="sxs-lookup"><span data-stu-id="cb56b-558">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="cb56b-559">Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa</span><span class="sxs-lookup"><span data-stu-id="cb56b-559">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="cb56b-560">Aplicando as principais atualizações instalando o produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-560">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="cb56b-561">Propriedades de configuração</span><span class="sxs-lookup"><span data-stu-id="cb56b-561">Configuration Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="cb56b-562">Propriedades de opções de instalação de recurso</span><span class="sxs-lookup"><span data-stu-id="cb56b-562">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="cb56b-563">Trabalhe com a política para gerenciar direitos de acesso e permissões.</span><span class="sxs-lookup"><span data-stu-id="cb56b-563">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="cb56b-564">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-564">For more information, see the following:</span></span>

    -   <span data-ttu-id="cb56b-565">[Políticas de máquina](machine-policies.md),</span><span class="sxs-lookup"><span data-stu-id="cb56b-565">[Machine Policies](machine-policies.md),</span></span>
    -   <span data-ttu-id="cb56b-566">[Políticas de usuário](user-policies.md),</span><span class="sxs-lookup"><span data-stu-id="cb56b-566">[User Policies](user-policies.md),</span></span>
    -   [<span data-ttu-id="cb56b-567">Instalando um pacote com privilégios elevados para um não administrador</span><span class="sxs-lookup"><span data-stu-id="cb56b-567">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="cb56b-568">Anunciando um aplicativo Per-User para ser instalado com privilégios elevados</span><span class="sxs-lookup"><span data-stu-id="cb56b-568">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="cb56b-569">Usando uma ação personalizada para criar contas de usuário em um computador local</span><span class="sxs-lookup"><span data-stu-id="cb56b-569">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="cb56b-570">**Propriedade AdminUser**</span><span class="sxs-lookup"><span data-stu-id="cb56b-570">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="cb56b-571">**Propriedade privilegiada**</span><span class="sxs-lookup"><span data-stu-id="cb56b-571">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="cb56b-572">**Propriedade EnableUserControl**</span><span class="sxs-lookup"><span data-stu-id="cb56b-572">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="cb56b-573">**Propriedade UserID**</span><span class="sxs-lookup"><span data-stu-id="cb56b-573">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="cb56b-574">**Propriedade SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="cb56b-574">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="cb56b-575">Instale vários pacotes usando o [*processamento de transações*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cb56b-575">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="cb56b-576">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-576">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-577">Instalações de vários pacotes</span><span class="sxs-lookup"><span data-stu-id="cb56b-577">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="cb56b-578">Inserir uma interface do usuário personalizada em um pacote Windows Installer..</span><span class="sxs-lookup"><span data-stu-id="cb56b-578">Embed a custom user interface within a Windows Installer package..</span></span>

    <span data-ttu-id="cb56b-579">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-579">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-580">Usando a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="cb56b-580">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="cb56b-581">Usando uma interface do usuário inserida</span><span class="sxs-lookup"><span data-stu-id="cb56b-581">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a><span data-ttu-id="cb56b-582">Desenvolvedores de infraestrutura</span><span class="sxs-lookup"><span data-stu-id="cb56b-582">Infrastructure Developers</span></span>

<span data-ttu-id="cb56b-583">Os desenvolvedores de infraestrutura podem criar plataformas unificadas para a implantação e o gerenciamento de software que usa o serviço de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb56b-583">Infrastructure Developers can create unified platforms for the deployment and management of software that uses the Windows Installer service.</span></span> <span data-ttu-id="cb56b-584">Eles podem usar a interface de programação de Windows Installer para consultar, gerenciar e distribuir aplicativos, patches e fontes em um sistema.</span><span class="sxs-lookup"><span data-stu-id="cb56b-584">They can use the Windows Installer programming interface to query, manage, and distribute applications, patches, and sources on a system.</span></span>

-   <span data-ttu-id="cb56b-585">Localize, inventaria e consulte o estado, as informações e os clientes dos componentes.</span><span class="sxs-lookup"><span data-stu-id="cb56b-585">Locate, inventory and query for the state, information, and clients of components.</span></span>

    <span data-ttu-id="cb56b-586">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-586">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-587">Funções específicas do componente</span><span class="sxs-lookup"><span data-stu-id="cb56b-587">Component-Specific Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-588">Funções de status do sistema</span><span class="sxs-lookup"><span data-stu-id="cb56b-588">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-589">Objeto do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-589">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="cb56b-590">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="cb56b-590">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="cb56b-591">Objeto patch</span><span class="sxs-lookup"><span data-stu-id="cb56b-591">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="cb56b-592">Inventário e consulta de informações e o estado dos produtos e recursos.</span><span class="sxs-lookup"><span data-stu-id="cb56b-592">Inventory and query for information and the state of products and features.</span></span>

    <span data-ttu-id="cb56b-593">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-593">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-594">Produtos e patches de inventário</span><span class="sxs-lookup"><span data-stu-id="cb56b-594">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="cb56b-595">Funções de status do sistema</span><span class="sxs-lookup"><span data-stu-id="cb56b-595">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-596">Funções de consulta de produto</span><span class="sxs-lookup"><span data-stu-id="cb56b-596">Product Query Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-597">Objeto do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-597">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="cb56b-598">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="cb56b-598">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="cb56b-599">Objeto patch</span><span class="sxs-lookup"><span data-stu-id="cb56b-599">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="cb56b-600">Melhore a resiliência da origem usando o Windows Installer para inventariar, consultar e modificar a lista de origem de aplicativos, atualizações e patches.</span><span class="sxs-lookup"><span data-stu-id="cb56b-600">Improve source resiliency by using the Windows Installer to inventory, query, and modify the source list of applications, upgrades, and patches.</span></span>

    <span data-ttu-id="cb56b-601">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-601">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-602">**Propriedade SOURCElist**</span><span class="sxs-lookup"><span data-stu-id="cb56b-602">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="cb56b-603">**Resiliência de origem**</span><span class="sxs-lookup"><span data-stu-id="cb56b-603">**Source Resiliency**</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="cb56b-604">Funções de instalação e configuração</span><span class="sxs-lookup"><span data-stu-id="cb56b-604">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-605">Objeto do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-605">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="cb56b-606">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="cb56b-606">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="cb56b-607">Objeto patch</span><span class="sxs-lookup"><span data-stu-id="cb56b-607">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="cb56b-608">Melhore a resiliência da origem usando o Windows Installer para inventariar, consultar e modificar as fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="cb56b-608">Improve source resiliency by using the Windows Installer to inventory, query, and modify media sources.</span></span>

    <span data-ttu-id="cb56b-609">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-609">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-610">**Propriedade SOURCElist**</span><span class="sxs-lookup"><span data-stu-id="cb56b-610">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="cb56b-611">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="cb56b-611">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="cb56b-612">Funções de instalação e configuração</span><span class="sxs-lookup"><span data-stu-id="cb56b-612">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-613">Objeto Product</span><span class="sxs-lookup"><span data-stu-id="cb56b-613">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="cb56b-614">Objeto patch</span><span class="sxs-lookup"><span data-stu-id="cb56b-614">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="cb56b-615">Inventário e consulta de informações e o estado dos patches.</span><span class="sxs-lookup"><span data-stu-id="cb56b-615">Inventory and query for information and the state of patches.</span></span>

    <span data-ttu-id="cb56b-616">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-616">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-617">Produtos e patches de inventário</span><span class="sxs-lookup"><span data-stu-id="cb56b-617">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="cb56b-618">Referência de função do instalador</span><span class="sxs-lookup"><span data-stu-id="cb56b-618">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="cb56b-619">Objeto patch</span><span class="sxs-lookup"><span data-stu-id="cb56b-619">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="cb56b-620">Trabalhe com a política para gerenciar direitos de acesso e permissões.</span><span class="sxs-lookup"><span data-stu-id="cb56b-620">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="cb56b-621">Para saber mais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cb56b-621">For more information, see the following:</span></span>

    -   [<span data-ttu-id="cb56b-622">Políticas do computador</span><span class="sxs-lookup"><span data-stu-id="cb56b-622">Machine Policies</span></span>](machine-policies.md)
    -   [<span data-ttu-id="cb56b-623">Políticas de usuário</span><span class="sxs-lookup"><span data-stu-id="cb56b-623">User Policies</span></span>](user-policies.md)
    -   [<span data-ttu-id="cb56b-624">Instalando um pacote com privilégios elevados para um não administrador</span><span class="sxs-lookup"><span data-stu-id="cb56b-624">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="cb56b-625">Anunciando um aplicativo Per-User para ser instalado com privilégios elevados</span><span class="sxs-lookup"><span data-stu-id="cb56b-625">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="cb56b-626">Usando uma ação personalizada para criar contas de usuário em um computador local</span><span class="sxs-lookup"><span data-stu-id="cb56b-626">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="cb56b-627">**Propriedade AdminUser**</span><span class="sxs-lookup"><span data-stu-id="cb56b-627">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="cb56b-628">**Propriedade privilegiada**</span><span class="sxs-lookup"><span data-stu-id="cb56b-628">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="cb56b-629">**Propriedade EnableUserControl**</span><span class="sxs-lookup"><span data-stu-id="cb56b-629">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="cb56b-630">**Propriedade UserID**</span><span class="sxs-lookup"><span data-stu-id="cb56b-630">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="cb56b-631">**Propriedade SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="cb56b-631">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

 

 



