---
description: Saiba mais sobre os conceitos de Windows Installer que começam com a letra A, como A fase de acessibilidade e aquisição.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011119"
---
# <a name="a-windows-installer"></a><span data-ttu-id="740af-103">A (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="740af-103">A (Windows Installer)</span></span>

<span data-ttu-id="740af-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="740af-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="740af-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="740af-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="740af-106">Implementação de design para tornar a interface do usuário do instalador acessível a todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="740af-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="740af-107">Para obter mais informações sobre acessibilidade, consulte o tópico Visão geral: [acessibilidade](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="740af-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="740af-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase de aquisição**</span><span class="sxs-lookup"><span data-stu-id="740af-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="740af-109">Fase de instalação durante a qual o instalador determina o procedimento.</span><span class="sxs-lookup"><span data-stu-id="740af-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="740af-110">A fase de aquisição começa quando um aplicativo ou usuário instrui [*Windows Installer*](m-gly.md) instalar um aplicativo ou recurso.</span><span class="sxs-lookup"><span data-stu-id="740af-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="740af-111">Em seguida, o instalador consulta o [*banco de dados*](i-gly.md) para obter informações à medida que gera o [*script de execução*](e-gly.md) para a instalação.</span><span class="sxs-lookup"><span data-stu-id="740af-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="740af-112">Para obter mais informações sobre as fases de uma instalação, consulte [mecanismo de instalação](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="740af-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="740af-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Action**</span><span class="sxs-lookup"><span data-stu-id="740af-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="740af-114">Muitas das funções executadas por Windows Installer são encapsuladas em ações.</span><span class="sxs-lookup"><span data-stu-id="740af-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="740af-115">Cada ação especifica a execução de uma função específica e o fluxo de procedimento total da instalação é prescrito pela sequência de ações nas tabelas de [*sequência*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="740af-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="740af-116">As [*ações padrão*](s-gly.md) são criadas em Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="740af-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="740af-117">As [*ações personalizadas*](c-gly.md) são gravadas pelo autor do [*pacote*](p-gly.md)de instalação.</span><span class="sxs-lookup"><span data-stu-id="740af-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="740af-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modo de aprovação de administrador**</span><span class="sxs-lookup"><span data-stu-id="740af-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="740af-119">O estado de aprovação habilitado pela proteção de conta de usuário (UAC) que executa todos os usuários com privilégios mínimos, incluindo administradores.</span><span class="sxs-lookup"><span data-stu-id="740af-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="740af-120">Os usuários precisam fornecer consentimento para elevar as instalações que exigem privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="740af-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="740af-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**anuncia**</span><span class="sxs-lookup"><span data-stu-id="740af-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="740af-122">Capacidade de tornar as interfaces necessárias para carregar e tornar um aplicativo disponível sem instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="740af-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="740af-123">Quando um usuário ou aplicativo ativa uma interface anunciada, o instalador continua a instalar os componentes necessários.</span><span class="sxs-lookup"><span data-stu-id="740af-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="740af-124">Os dois tipos de publicidade são [*atribuição*](/windows) e [*publicação*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="740af-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="740af-125">Para obter mais informações, consulte também [*instalar sob demanda*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="740af-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="740af-126">Para obter mais informações sobre como o instalador anuncia aplicativos, consulte [anúncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="740af-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="740af-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**AIS (serviço de informações de aplicativo)**</span><span class="sxs-lookup"><span data-stu-id="740af-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="740af-128">Um serviço de sistema do Windows Vista que facilita a execução de instalações que exigem privilégios elevados para serem executadas.</span><span class="sxs-lookup"><span data-stu-id="740af-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="740af-129">Fornece a IU de consentimento usada pelo controle de conta de usuário para solicitar a autorização de um usuário para o administrador.</span><span class="sxs-lookup"><span data-stu-id="740af-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="740af-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**atribuindo**</span><span class="sxs-lookup"><span data-stu-id="740af-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="740af-131">Disponibiliza um aplicativo e o faz aparecer como se ele fosse instalado em um usuário, sem realmente instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="740af-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="740af-132">A atribuição de adicionar atalhos e ícones ao menu **Iniciar** , associa arquivos apropriados e grava entradas do registro para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="740af-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="740af-133">Quando um usuário tenta abrir um aplicativo atribuído, o instalador instala o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="740af-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="740af-134">A atribuição e a [*publicação*](p-gly.md) são dois métodos de [*publicidade*](/windows).</span><span class="sxs-lookup"><span data-stu-id="740af-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="740af-135">Para obter mais informações, consulte [anúncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="740af-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="740af-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**execução assíncrona**</span><span class="sxs-lookup"><span data-stu-id="740af-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="740af-137">[*Ação personalizada*](c-gly.md) durante a qual o instalador executa threads separados da ação personalizada e a instalação atual simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="740af-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="740af-138">Para obter mais informações, consulte [ações personalizadas síncronas e assíncronas](synchronous-and-asynchronous-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="740af-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 
