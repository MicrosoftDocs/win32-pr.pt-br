---
description: Uma lista do conteúdo de referência para a API do Windows.
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Índice de API do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cace235af1c729e450bdf99b276eca1bfc000
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105807288"
---
# <a name="windows-api-index"></a><span data-ttu-id="a5d2b-103">Índice de API do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-103">Windows API index</span></span>

<span data-ttu-id="a5d2b-104">A seguir está uma lista do conteúdo de referência para a API (interface de programação de aplicativo) do Windows para aplicativos de desktop e de servidor.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-104">The following is a list of the reference content for the Windows application programming interface (API) for desktop and server applications.</span></span>

<span data-ttu-id="a5d2b-105">Usando a API do Windows, você pode desenvolver aplicativos que são executados com êxito em todas as versões do Windows, aproveitando os recursos e as funcionalidades exclusivos de cada versão.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-105">Using the Windows API, you can develop applications that run successfully on all versions of Windows while taking advantage of the features and capabilities unique to each version.</span></span> <span data-ttu-id="a5d2b-106">(Observe que isso era chamado anteriormente de API do Win32.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-106">(Note that this was formerly called the Win32 API.</span></span> <span data-ttu-id="a5d2b-107">O nome API do Windows reflete com mais precisão suas raízes no Windows de 16 bits e seu suporte no Windows de 64 bits.)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-107">The name Windows API more accurately reflects its roots in 16-bit Windows and its support on 64-bit Windows.)</span></span>

## <a name="user-interface"></a><span data-ttu-id="a5d2b-108">Interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a5d2b-108">User interface</span></span>

<span data-ttu-id="a5d2b-109">A API da interface do usuário do Windows cria e usa o Windows para exibir a saída, solicitar a entrada do usuário e executar as outras tarefas que dão suporte à interação com o usuário.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-109">The Windows UI API create and use windows to display output, prompt for user input, and carry out the other tasks that support interaction with the user.</span></span> <span data-ttu-id="a5d2b-110">A maioria dos aplicativos cria pelo menos uma janela.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-110">Most applications create at least one window.</span></span>

-   [<span data-ttu-id="a5d2b-111">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="a5d2b-111">Accessibility</span></span>](../winauto/windows-accessibility-features-reference.md)
-   [<span data-ttu-id="a5d2b-112">Gerenciador de Janelas da Área de Trabalho (DWM)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-112">Desktop Window Manager (DWM)</span></span>](../dwm/reference.md)
-   [<span data-ttu-id="a5d2b-113">Serviços de globalização</span><span class="sxs-lookup"><span data-stu-id="a5d2b-113">Globalization Services</span></span>](../intl/globalization-services.md)
-   [<span data-ttu-id="a5d2b-114">DPI alto</span><span class="sxs-lookup"><span data-stu-id="a5d2b-114">High DPI</span></span>](../hidpi/high-dpi-reference.md)
-   [<span data-ttu-id="a5d2b-115">MUI (Multilingual User interface)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-115">Multilingual User Interface (MUI)</span></span>](../intl/multilingual-user-interface-reference.md)
-   [<span data-ttu-id="a5d2b-116">NLS (suporte ao idioma nacional)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-116">National Language Support (NLS)</span></span>](../intl/national-language-support-reference.md)
-   <span data-ttu-id="a5d2b-117">[Elementos da interface do usuário](../devnotes/user-interface.md):</span><span class="sxs-lookup"><span data-stu-id="a5d2b-117">[User Interface elements](../devnotes/user-interface.md):</span></span>

    -   [<span data-ttu-id="a5d2b-118">Botões</span><span class="sxs-lookup"><span data-stu-id="a5d2b-118">Buttons</span></span>](../controls/bumper-button-button-control-reference.md)
    -   [<span data-ttu-id="a5d2b-119">Interpolação</span><span class="sxs-lookup"><span data-stu-id="a5d2b-119">Carets</span></span>](../menurc/caret-functions.md)
    -   [<span data-ttu-id="a5d2b-120">Caixas de combinação</span><span class="sxs-lookup"><span data-stu-id="a5d2b-120">Combo Boxes</span></span>](../controls/bumper-combobox-combobox-control-reference.md)
    -   [<span data-ttu-id="a5d2b-121">Caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="a5d2b-121">Common Dialog Boxes</span></span>](../dlgbox/common-dialog-box-reference.md)
    -   [<span data-ttu-id="a5d2b-122">Controles comuns</span><span class="sxs-lookup"><span data-stu-id="a5d2b-122">Common Controls</span></span>](../controls/individual-control-info.md)
    -   [<span data-ttu-id="a5d2b-123">Cursores</span><span class="sxs-lookup"><span data-stu-id="a5d2b-123">Cursors</span></span>](../menurc/cursor-reference.md)
    -   [<span data-ttu-id="a5d2b-124">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="a5d2b-124">Dialog Boxes</span></span>](../dlgbox/dialog-box-reference.md)
    -   [<span data-ttu-id="a5d2b-125">Editar controles</span><span class="sxs-lookup"><span data-stu-id="a5d2b-125">Edit Controls</span></span>](../controls/bumper-edit-control-edit-control-reference.md)
    -   [<span data-ttu-id="a5d2b-126">Controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a5d2b-126">Header Controls</span></span>](../controls/bumper-header-control-header-control-reference.md)
    -   [<span data-ttu-id="a5d2b-127">Ícones</span><span class="sxs-lookup"><span data-stu-id="a5d2b-127">Icons</span></span>](../menurc/icon-reference.md)
    -   [<span data-ttu-id="a5d2b-128">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="a5d2b-128">Keyboard Accelerators</span></span>](../menurc/keyboard-accelerator-reference.md)
    -   [<span data-ttu-id="a5d2b-129">Caixas de listagem</span><span class="sxs-lookup"><span data-stu-id="a5d2b-129">List Boxes</span></span>](../controls/bumper-list-box-list-box-control-reference.md)
    -   [<span data-ttu-id="a5d2b-130">Controles de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="a5d2b-130">List-View Controls</span></span>](../controls/bumper-list-view-list-view-control-reference.md)
    -   [<span data-ttu-id="a5d2b-131">Menus</span><span class="sxs-lookup"><span data-stu-id="a5d2b-131">Menus</span></span>](../menurc/menu-reference.md)
    -   [<span data-ttu-id="a5d2b-132">Barras de progresso</span><span class="sxs-lookup"><span data-stu-id="a5d2b-132">Progress Bars</span></span>](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [<span data-ttu-id="a5d2b-133">Folhas de propriedades</span><span class="sxs-lookup"><span data-stu-id="a5d2b-133">Property Sheets</span></span>](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [<span data-ttu-id="a5d2b-134">Controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="a5d2b-134">Rich Edit Controls</span></span>](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [<span data-ttu-id="a5d2b-135">Barras de rolagem</span><span class="sxs-lookup"><span data-stu-id="a5d2b-135">Scroll Bars</span></span>](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [<span data-ttu-id="a5d2b-136">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-136">Static Controls</span></span>](../controls/bumper-static-control-static-control-reference.md)
    -   [<span data-ttu-id="a5d2b-137">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="a5d2b-137">Strings</span></span>](../menurc/string-reference.md)
    -   [<span data-ttu-id="a5d2b-138">Barras de Ferramentas</span><span class="sxs-lookup"><span data-stu-id="a5d2b-138">Toolbars</span></span>](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [<span data-ttu-id="a5d2b-139">Dicas de ferramentas</span><span class="sxs-lookup"><span data-stu-id="a5d2b-139">Tooltips</span></span>](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [<span data-ttu-id="a5d2b-140">Trackbars</span><span class="sxs-lookup"><span data-stu-id="a5d2b-140">Trackbars</span></span>](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [<span data-ttu-id="a5d2b-141">Controles de exibição de árvore</span><span class="sxs-lookup"><span data-stu-id="a5d2b-141">Tree-View Controls</span></span>](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [<span data-ttu-id="a5d2b-142">Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-142">Windows Animation Manager</span></span>](../uianimation/windows-animation-reference.md)
-   [<span data-ttu-id="a5d2b-143">Estrutura da faixa de dasgem do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-143">Windows Ribbon Framework</span></span>](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a><span data-ttu-id="a5d2b-144">Ambiente do Windows (Shell)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-144">Windows environment (Shell)</span></span>

-   [<span data-ttu-id="a5d2b-145">Sistema de propriedades do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-145">Windows Property System</span></span>](../properties/property-system-reference.md)
-   <span data-ttu-id="a5d2b-146">[Shell do Windows](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-146">[Windows Shell](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-147">Windows Search</span><span class="sxs-lookup"><span data-stu-id="a5d2b-147">Windows Search</span></span>](../search/-search-reference-entry-page.md)
-   [<span data-ttu-id="a5d2b-148">Consoles</span><span class="sxs-lookup"><span data-stu-id="a5d2b-148">Consoles</span></span>](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a><span data-ttu-id="a5d2b-149">Entrada e mensagens do usuário</span><span class="sxs-lookup"><span data-stu-id="a5d2b-149">User input and messaging</span></span>

-   [<span data-ttu-id="a5d2b-150">Interação do usuário</span><span class="sxs-lookup"><span data-stu-id="a5d2b-150">User Interaction</span></span>](../user-interaction.md)
    -   [<span data-ttu-id="a5d2b-151">Manipulação direta</span><span class="sxs-lookup"><span data-stu-id="a5d2b-151">Direct Manipulation</span></span>](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [<span data-ttu-id="a5d2b-152">Entrada à tinta</span><span class="sxs-lookup"><span data-stu-id="a5d2b-152">Ink input</span></span>](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [<span data-ttu-id="a5d2b-153">Configuração de comentários de entrada</span><span class="sxs-lookup"><span data-stu-id="a5d2b-153">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [<span data-ttu-id="a5d2b-154">Contexto de interação</span><span class="sxs-lookup"><span data-stu-id="a5d2b-154">Interaction Context</span></span>](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [<span data-ttu-id="a5d2b-155">Pilha de entrada do dispositivo ponteiro</span><span class="sxs-lookup"><span data-stu-id="a5d2b-155">Pointer Device Input Stack</span></span>](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [<span data-ttu-id="a5d2b-156">Notificações e mensagens de entrada do ponteiro</span><span class="sxs-lookup"><span data-stu-id="a5d2b-156">Pointer Input Messages and Notifications</span></span>](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [<span data-ttu-id="a5d2b-157">Entrada do controlador radial</span><span class="sxs-lookup"><span data-stu-id="a5d2b-157">Radial controller input</span></span>](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [<span data-ttu-id="a5d2b-158">Estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="a5d2b-158">Text Services Framework</span></span>](../tsf/text-services-framework.md)
    -   [<span data-ttu-id="a5d2b-159">Teste de colisão de toque</span><span class="sxs-lookup"><span data-stu-id="a5d2b-159">Touch Hit Testing</span></span>](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [<span data-ttu-id="a5d2b-160">Injeção de toque</span><span class="sxs-lookup"><span data-stu-id="a5d2b-160">Touch Injection</span></span>](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [<span data-ttu-id="a5d2b-161">Interação do usuário herdada</span><span class="sxs-lookup"><span data-stu-id="a5d2b-161">Legacy User Interaction</span></span>](../legacy-user-interaction-features.md)
    -   [<span data-ttu-id="a5d2b-162">Entrada por toque</span><span class="sxs-lookup"><span data-stu-id="a5d2b-162">Touch Input</span></span>](../wintouch/windows-touch-portal.md)
    -   [<span data-ttu-id="a5d2b-163">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="a5d2b-163">Keyboard Input</span></span>](../inputdev/keyboard-input.md)
    -   [<span data-ttu-id="a5d2b-164">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="a5d2b-164">Mouse Input</span></span>](../inputdev/mouse-input.md)
    -   [<span data-ttu-id="a5d2b-165">Entrada bruta</span><span class="sxs-lookup"><span data-stu-id="a5d2b-165">Raw Input</span></span>](../inputdev/raw-input.md)
-   <span data-ttu-id="a5d2b-166">[Windows e mensagens](../winmsg/windowing.md):</span><span class="sxs-lookup"><span data-stu-id="a5d2b-166">[Windows and Messages](../winmsg/windowing.md):</span></span>

    -   [<span data-ttu-id="a5d2b-167">Mensagens e filas de mensagens</span><span class="sxs-lookup"><span data-stu-id="a5d2b-167">Messages and Message Queues</span></span>](../winmsg/message-and-message-queue-reference.md)
    -   [<span data-ttu-id="a5d2b-168">Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-168">Windows</span></span>](../winmsg/window-reference.md)
    -   [<span data-ttu-id="a5d2b-169">Classes de janela</span><span class="sxs-lookup"><span data-stu-id="a5d2b-169">Window Classes</span></span>](../winmsg/window-class-reference.md)
    -   [<span data-ttu-id="a5d2b-170">Procedimentos de janela</span><span class="sxs-lookup"><span data-stu-id="a5d2b-170">Window Procedures</span></span>](../winmsg/window-procedure-reference.md)
    -   [<span data-ttu-id="a5d2b-171">Temporizadores</span><span class="sxs-lookup"><span data-stu-id="a5d2b-171">Timers</span></span>](../winmsg/timer-reference.md)
    -   [<span data-ttu-id="a5d2b-172">Propriedades da janela</span><span class="sxs-lookup"><span data-stu-id="a5d2b-172">Window Properties</span></span>](../winmsg/window-property-reference.md)
    -   [<span data-ttu-id="a5d2b-173">Ganchos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-173">Hooks</span></span>](../winmsg/hook-reference.md)

## <a name="data-access-and-storage"></a><span data-ttu-id="a5d2b-174">Armazenamento e acesso a dados</span><span class="sxs-lookup"><span data-stu-id="a5d2b-174">Data access and storage</span></span>

-   [<span data-ttu-id="a5d2b-175">BITS (serviço de Transferência Inteligente em Segundo Plano)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-175">Background Intelligent Transfer Service (BITS)</span></span>](../bits/bits-reference.md)
-   [<span data-ttu-id="a5d2b-176">Backup de dados</span><span class="sxs-lookup"><span data-stu-id="a5d2b-176">Data Backup</span></span>](../backup/backup.md)
    -   [<span data-ttu-id="a5d2b-177">Backup</span><span class="sxs-lookup"><span data-stu-id="a5d2b-177">Backup</span></span>](../backup/backup-reference.md)
    -   [<span data-ttu-id="a5d2b-178">Eliminação de Duplicação de Dados</span><span class="sxs-lookup"><span data-stu-id="a5d2b-178">Data Deduplication</span></span>](/previous-versions/windows/desktop/dedup/data-deduplication-api-reference)
    -   [<span data-ttu-id="a5d2b-179">Cópias de Sombra de Volume</span><span class="sxs-lookup"><span data-stu-id="a5d2b-179">Volume Shadow Copy</span></span>](../vss/volume-shadow-copy-reference.md)
    -   [<span data-ttu-id="a5d2b-180">Backup do Windows Server</span><span class="sxs-lookup"><span data-stu-id="a5d2b-180">Windows Server Backup</span></span>](/previous-versions/windows/desktop/wsb/windows-server-backup-api-interfaces)
-   <span data-ttu-id="a5d2b-181">[Troca de dados](../dataxchg/data-exchange.md):</span><span class="sxs-lookup"><span data-stu-id="a5d2b-181">[Data Exchange](../dataxchg/data-exchange.md):</span></span>

    -   [<span data-ttu-id="a5d2b-182">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="a5d2b-182">Clipboard</span></span>](../dataxchg/clipboard-reference.md)
    -   [<span data-ttu-id="a5d2b-183">Troca dinâmica de dados (DDE)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-183">Dynamic Data Exchange (DDE)</span></span>](../dataxchg/dynamic-data-exchange-reference.md)
    -   [<span data-ttu-id="a5d2b-184">Gerenciamento de troca dinâmica de dados (DDEML)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-184">Dynamic Data Exchange Management (DDEML)</span></span>](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [<span data-ttu-id="a5d2b-185">Gerenciamento de diretórios</span><span class="sxs-lookup"><span data-stu-id="a5d2b-185">Directory Management</span></span>](../fileio/directory-management-reference.md)
-   [<span data-ttu-id="a5d2b-186">Gerenciamento de disco</span><span class="sxs-lookup"><span data-stu-id="a5d2b-186">Disk Management</span></span>](../fileio/disk-management-reference.md)
-   [<span data-ttu-id="a5d2b-187">DFS (Sistema de Arquivos Distribuído)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-187">Distributed File System (DFS)</span></span>](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [<span data-ttu-id="a5d2b-188">Replicação DFS</span><span class="sxs-lookup"><span data-stu-id="a5d2b-188">Distributed File System Replication</span></span>](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [<span data-ttu-id="a5d2b-189">Mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="a5d2b-189">Extensible Storage Engine</span></span>](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [<span data-ttu-id="a5d2b-190">Arquivos e e/s (sistema de arquivos local)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-190">Files and I/O (Local file system)</span></span>](../fileio/file-management-reference.md)
-   [<span data-ttu-id="a5d2b-191">API da biblioteca de descoberta do iSCSI</span><span class="sxs-lookup"><span data-stu-id="a5d2b-191">iSCSI Discovery Library API</span></span>](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
-   [<span data-ttu-id="a5d2b-192">Arquivos Offline</span><span class="sxs-lookup"><span data-stu-id="a5d2b-192">Offline Files</span></span>](/previous-versions/windows/desktop/offlinefiles/offline-files-reference)
-   [<span data-ttu-id="a5d2b-193">Empacotamento</span><span class="sxs-lookup"><span data-stu-id="a5d2b-193">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging-programming-reference)
-   [<span data-ttu-id="a5d2b-194">Compressão diferencial remota</span><span class="sxs-lookup"><span data-stu-id="a5d2b-194">Remote Differential Compression</span></span>](/previous-versions/windows/desktop/rdc/remote-differential-compression-reference)
-   [<span data-ttu-id="a5d2b-195">NTFS transacional</span><span class="sxs-lookup"><span data-stu-id="a5d2b-195">Transactional NTFS</span></span>](../fileio/transactional-ntfs-reference.md)
-   [<span data-ttu-id="a5d2b-196">Gerenciamento de volume</span><span class="sxs-lookup"><span data-stu-id="a5d2b-196">Volume Management</span></span>](../fileio/volume-management-reference.md)
-   <span data-ttu-id="a5d2b-197">[VHD (disco rígido virtual)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-197">[Virtual Hard Disk (VHD)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-198">Gerenciamento de Armazenamento do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-198">Windows Storage Management</span></span>](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   <span data-ttu-id="a5d2b-199">[Windows Data Access Components](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-199">[Windows Data Access Components](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))</span></span>
    -   [<span data-ttu-id="a5d2b-200">Microsoft ODBC (Open Database Connectivity)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-200">Microsoft Open Database Connectivity (ODBC)</span></span>](/sql/odbc/reference/syntax/odbc-reference)
    -   <span data-ttu-id="a5d2b-201">[Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-201">[Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))</span></span>
    -   [<span data-ttu-id="a5d2b-202">Microsoft ADO (ActiveX Data Objects)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-202">Microsoft ActiveX Data Objects (ADO)</span></span>](/sql/ado/reference/ado-programmer-s-reference)

## <a name="diagnostics"></a><span data-ttu-id="a5d2b-203">Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-203">Diagnostics</span></span>

<span data-ttu-id="a5d2b-204">A API de [diagnóstico](/previous-versions//bb648685(v=vs.85)) permite solucionar problemas de aplicativos ou do sistema e monitorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-204">The [Diagnostics](/previous-versions//bb648685(v=vs.85)) API enable you to troubleshoot application or system problems and monitor performance.</span></span>

-   [<span data-ttu-id="a5d2b-205">Reinicialização e recuperação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-205">Application Recovery and Restart</span></span>](../recovery/application-recovery-and-restart-reference.md)
-   [<span data-ttu-id="a5d2b-206">Depuração</span><span class="sxs-lookup"><span data-stu-id="a5d2b-206">Debugging</span></span>](../debug/debugging-reference.md)
-   [<span data-ttu-id="a5d2b-207">Tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="a5d2b-207">Error Handling</span></span>](../debug/error-handling-reference.md)
-   [<span data-ttu-id="a5d2b-208">Log de eventos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-208">Event Logging</span></span>](../eventlog/event-logging-reference.md)
-   [<span data-ttu-id="a5d2b-209">Rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-209">Event Tracing</span></span>](../etw/event-tracing-reference.md)
-   [<span data-ttu-id="a5d2b-210">Criação de perfil de contador de hardware (HCP)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-210">Hardware Counter Profiling (HCP)</span></span>](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [<span data-ttu-id="a5d2b-211">NDF (estrutura de diagnóstico de rede)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-211">Network Diagnostics Framework (NDF)</span></span>](../ndf/ndf-reference.md)
-   [<span data-ttu-id="a5d2b-212">Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="a5d2b-212">Network Monitor</span></span>](../netmon2/reference.md)
-   [<span data-ttu-id="a5d2b-213">Contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="a5d2b-213">Performance Counters</span></span>](../perfctrs/performance-counters-reference.md)
-   [<span data-ttu-id="a5d2b-214">Logs e Alertas de Desempenho (PLA)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-214">Performance Logs and Alerts (PLA)</span></span>](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [<span data-ttu-id="a5d2b-215">Processar instantâneos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-215">Process Snapshotting</span></span>](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [<span data-ttu-id="a5d2b-216">Status do processo (PSAPI)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-216">Process Status (PSAPI)</span></span>](../psapi/psapi-reference.md)
-   [<span data-ttu-id="a5d2b-217">Tratamento de exceções estruturado</span><span class="sxs-lookup"><span data-stu-id="a5d2b-217">Structured Exception Handling</span></span>](../debug/structured-exception-handling-reference.md)
-   [<span data-ttu-id="a5d2b-218">Monitor do Sistema</span><span class="sxs-lookup"><span data-stu-id="a5d2b-218">System Monitor</span></span>](../sysmon/system-monitor-reference.md)
-   [<span data-ttu-id="a5d2b-219">Passagem de cadeia de espera</span><span class="sxs-lookup"><span data-stu-id="a5d2b-219">Wait Chain Traversal</span></span>](../debug/wait-chain-traversal.md)
-   [<span data-ttu-id="a5d2b-220">Relatório de Erros do Windows (WER)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-220">Windows Error Reporting (WER)</span></span>](../wer/wer-reference.md)
-   [<span data-ttu-id="a5d2b-221">Log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-221">Windows Event Log</span></span>](../wes/windows-event-log-reference.md)
-   [<span data-ttu-id="a5d2b-222">Plataforma de solução de problemas do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-222">Windows Troubleshooting Platform</span></span>](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a><span data-ttu-id="a5d2b-223">Gráficos e multimídia</span><span class="sxs-lookup"><span data-stu-id="a5d2b-223">Graphics and multimedia</span></span>

<span data-ttu-id="a5d2b-224">As APIs de [gráficos, multimídia](/previous-versions//aa969176(v=vs.85)) , [áudio e vídeo](../audio-and-video.md) permitem que os aplicativos incorporem texto formatado, gráficos, áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-224">The [Graphics, multimedia,](/previous-versions//aa969176(v=vs.85)) [audio, and video](../audio-and-video.md) APIs enable applications to incorporate formatted text, graphics, audio, and video.</span></span>

-   [<span data-ttu-id="a5d2b-225">Áudio principal</span><span class="sxs-lookup"><span data-stu-id="a5d2b-225">Core Audio</span></span>](../coreaudio/programming-reference.md)
-   [<span data-ttu-id="a5d2b-226">Direct2D</span><span class="sxs-lookup"><span data-stu-id="a5d2b-226">Direct2D</span></span>](../direct2d/reference.md)
-   [<span data-ttu-id="a5d2b-227">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="a5d2b-227">DirectComposition</span></span>](../directcomp/reference.md)
-   [<span data-ttu-id="a5d2b-228">DirectShow</span><span class="sxs-lookup"><span data-stu-id="a5d2b-228">DirectShow</span></span>](../directshow/directshow-reference.md)
-   [<span data-ttu-id="a5d2b-229">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="a5d2b-229">DirectWrite</span></span>](../directwrite/reference.md)
-   [<span data-ttu-id="a5d2b-230">DirectX</span><span class="sxs-lookup"><span data-stu-id="a5d2b-230">DirectX</span></span>](../directx-sdk--august-2009-.md)
-   [<span data-ttu-id="a5d2b-231">Graphics Device Interface (GDI)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-231">Graphics Device Interface (GDI)</span></span>](../gdi/windows-gdi.md)
-   [<span data-ttu-id="a5d2b-232">GDI+</span><span class="sxs-lookup"><span data-stu-id="a5d2b-232">GDI+</span></span>](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [<span data-ttu-id="a5d2b-233">Streaming de mídia</span><span class="sxs-lookup"><span data-stu-id="a5d2b-233">Media Streaming</span></span>](../mediastreaming/media-streaming-api-portal.md)
-   [<span data-ttu-id="a5d2b-234">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5d2b-234">Microsoft Media Foundation</span></span>](../medfound/media-foundation-programming-reference.md)
-   [<span data-ttu-id="a5d2b-235">Tecnologias de TV da Microsoft</span><span class="sxs-lookup"><span data-stu-id="a5d2b-235">Microsoft TV Technologies</span></span>](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [<span data-ttu-id="a5d2b-236">OpenGL</span><span class="sxs-lookup"><span data-stu-id="a5d2b-236">OpenGL</span></span>](../opengl/opengl-reference.md)
-   [<span data-ttu-id="a5d2b-237">Configuração do monitor</span><span class="sxs-lookup"><span data-stu-id="a5d2b-237">Monitor Configuration</span></span>](../monitor/monitor-configuration-reference.md)
-   [<span data-ttu-id="a5d2b-238">Vários monitores de exibição</span><span class="sxs-lookup"><span data-stu-id="a5d2b-238">Multiple Display Monitors</span></span>](../gdi/multiple-display-monitors-reference.md)
-   [<span data-ttu-id="a5d2b-239">Aquisição de imagem</span><span class="sxs-lookup"><span data-stu-id="a5d2b-239">Picture Acquisition</span></span>](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [<span data-ttu-id="a5d2b-240">Sistema de cores do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-240">Windows Color System</span></span>](../wcs/reference.md)
-   [<span data-ttu-id="a5d2b-241">Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-241">Windows Imaging Component (WIC)</span></span>](../wic/-wic-codec-reference.md)
-   <span data-ttu-id="a5d2b-242">[Codec de áudio e vídeo do Windows Media e DSP](/previous-versions//dd443208(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-242">[Windows Media Audio and Video Codec and DSP](/previous-versions//dd443208(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-243">Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="a5d2b-243">Windows Media Center</span></span>](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [<span data-ttu-id="a5d2b-244">Formato de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-244">Windows Media Format</span></span>](../wmformat/programming-reference.md)
-   [<span data-ttu-id="a5d2b-245">Serviços de compartilhamento da biblioteca do Windows Media</span><span class="sxs-lookup"><span data-stu-id="a5d2b-245">Windows Media Library Sharing Services</span></span>](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [<span data-ttu-id="a5d2b-246">Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="a5d2b-246">Windows Media Player</span></span>](../wmp/windows-media-player-object-model-reference.md)
-   <span data-ttu-id="a5d2b-247">[Serviços de mídia do Windows](/previous-versions/windows/desktop/dd893580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-247">[Windows Media Services](/previous-versions/windows/desktop/dd893580(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-248">Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="a5d2b-248">Windows Movie Maker</span></span>](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [<span data-ttu-id="a5d2b-249">Multimídia do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-249">Windows Multimedia</span></span>](../multimedia/multimedia-reference.md)

## <a name="devices"></a><span data-ttu-id="a5d2b-250">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-250">Devices</span></span>

-   [<span data-ttu-id="a5d2b-251">AllJoyn</span><span class="sxs-lookup"><span data-stu-id="a5d2b-251">AllJoyn</span></span>](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [<span data-ttu-id="a5d2b-252">Recursos de comunicação</span><span class="sxs-lookup"><span data-stu-id="a5d2b-252">Communications Resources</span></span>](../devio/communications-reference.md)
-   [<span data-ttu-id="a5d2b-253">Acesso ao dispositivo</span><span class="sxs-lookup"><span data-stu-id="a5d2b-253">Device Access</span></span>](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [<span data-ttu-id="a5d2b-254">Gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a5d2b-254">Device Management</span></span>](../devio/device-management-reference.md)
-   [<span data-ttu-id="a5d2b-255">Armazenamento Avançado</span><span class="sxs-lookup"><span data-stu-id="a5d2b-255">Enhanced Storage</span></span>](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [<span data-ttu-id="a5d2b-256">Descoberta de função</span><span class="sxs-lookup"><span data-stu-id="a5d2b-256">Function Discovery</span></span>](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [<span data-ttu-id="a5d2b-257">Mestre de imagem</span><span class="sxs-lookup"><span data-stu-id="a5d2b-257">Image Mastering</span></span>](../imapi/imapi-reference.md)
-   [<span data-ttu-id="a5d2b-258">Localidade</span><span class="sxs-lookup"><span data-stu-id="a5d2b-258">Location</span></span>](../locationapi/windows-location-programming-reference.md)
-   [<span data-ttu-id="a5d2b-259">Banco de dados de associação PnP-X</span><span class="sxs-lookup"><span data-stu-id="a5d2b-259">PnP-X Association Database</span></span>](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [<span data-ttu-id="a5d2b-260">Impressão</span><span class="sxs-lookup"><span data-stu-id="a5d2b-260">Printing</span></span>](/windows-hardware/drivers/print/introduction-to-printing)
    -   [<span data-ttu-id="a5d2b-261">Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="a5d2b-261">Print Spooler</span></span>](../printdocs/printing-and-print-spooler-reference.md)
    -   [<span data-ttu-id="a5d2b-262">Imprimir pacote de documentos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-262">Print Document Package</span></span>](../printdocs/tailored-app-printing-api.md)
    -   [<span data-ttu-id="a5d2b-263">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a5d2b-263">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [<span data-ttu-id="a5d2b-264">Tíquete de impressão</span><span class="sxs-lookup"><span data-stu-id="a5d2b-264">Print Ticket</span></span>](../printdocs/print-ticket-api.md)
    -   [<span data-ttu-id="a5d2b-265">Impressão XPS</span><span class="sxs-lookup"><span data-stu-id="a5d2b-265">XPS Print</span></span>](../printdocs/xpsprint-api.md)
-   [<span data-ttu-id="a5d2b-266">Sensores</span><span class="sxs-lookup"><span data-stu-id="a5d2b-266">Sensors</span></span>](../sensorsapi/sensor-api-programming-reference.md)
-   [<span data-ttu-id="a5d2b-267">Serviço de notificação de eventos do sistema (SENS)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-267">System Event Notification Service (SENS)</span></span>](../sens/sens-reference.md)
-   [<span data-ttu-id="a5d2b-268">Ajuda da ferramenta</span><span class="sxs-lookup"><span data-stu-id="a5d2b-268">Tool Help</span></span>](../toolhelp/tool-help-reference.md)
-   [<span data-ttu-id="a5d2b-269">UPnP</span><span class="sxs-lookup"><span data-stu-id="a5d2b-269">UPnP</span></span>](../upnp/universal-plug-and-play-start-page.md)
-   [<span data-ttu-id="a5d2b-270">Serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-270">Web Services on Devices</span></span>](../wsdapi/web-services-for-devices-reference.md)
-   [<span data-ttu-id="a5d2b-271">WIA (Windows Image Acquisition)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-271">Windows Image Acquisition (WIA)</span></span>](../wia/-wia-reference.md)
-   [<span data-ttu-id="a5d2b-272">Gerenciador de Dispositivos de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-272">Windows Media Device Manager</span></span>](../wmdm/programming-reference.md)
-   [<span data-ttu-id="a5d2b-273">Dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-273">Windows Portable Devices</span></span>](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a><span data-ttu-id="a5d2b-274">Serviços do sistema</span><span class="sxs-lookup"><span data-stu-id="a5d2b-274">System services</span></span>

<span data-ttu-id="a5d2b-275">As APIs de [Serviços do sistema](/previous-versions//aa969179(v=vs.85)) fornecem aos aplicativos acesso aos recursos do computador e aos recursos do sistema operacional subjacente, como memória, sistemas de arquivos, dispositivos, processos e threads.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-275">The [System Services](/previous-versions//aa969179(v=vs.85)) APIs give applications access to the resources of the computer and the features of the underlying operating system, such as memory, file systems, devices, processes, and threads.</span></span>

-   [<span data-ttu-id="a5d2b-276">INTERFACES</span><span class="sxs-lookup"><span data-stu-id="a5d2b-276">COM</span></span>](../com/reference.md)
-   [<span data-ttu-id="a5d2b-277">COM+</span><span class="sxs-lookup"><span data-stu-id="a5d2b-277">COM+</span></span>](../cossdk/com--reference.md)
-   [<span data-ttu-id="a5d2b-278">API de compactação</span><span class="sxs-lookup"><span data-stu-id="a5d2b-278">Compression API</span></span>](../cmpapi/-compression-portal.md)
-   <span data-ttu-id="a5d2b-279">[DTC (Coordenador de Transações Distribuídas)](/previous-versions/windows/desktop/ms686108(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-279">[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-280">Bibliotecas de vínculo dinâmico (DLLs)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-280">Dynamic-Link Libraries (DLLs)</span></span>](../dlls/dynamic-link-library-functions.md)
-   [<span data-ttu-id="a5d2b-281">API de ajuda</span><span class="sxs-lookup"><span data-stu-id="a5d2b-281">Help API</span></span>](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   <span data-ttu-id="a5d2b-282">[Comunicações entre processos](../ipc/interprocess-communications.md):</span><span class="sxs-lookup"><span data-stu-id="a5d2b-282">[Interprocess Communications](../ipc/interprocess-communications.md):</span></span>
    -   [<span data-ttu-id="a5d2b-283">Processadores</span><span class="sxs-lookup"><span data-stu-id="a5d2b-283">Mailslots</span></span>](../ipc/mailslot-functions.md)
    -   [<span data-ttu-id="a5d2b-284">Pipes</span><span class="sxs-lookup"><span data-stu-id="a5d2b-284">Pipes</span></span>](../ipc/pipe-functions.md)
-   [<span data-ttu-id="a5d2b-285">KTM (kernel Transaction Manager)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-285">Kernel Transaction Manager (KTM)</span></span>](../ktm/ktm-reference.md)
-   [<span data-ttu-id="a5d2b-286">Gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="a5d2b-286">Memory Management</span></span>](../memory/memory-management-reference.md)
-   [<span data-ttu-id="a5d2b-287">Gravador de operação</span><span class="sxs-lookup"><span data-stu-id="a5d2b-287">Operation Recorder</span></span>](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [<span data-ttu-id="a5d2b-288">Gerenciamento de Energia</span><span class="sxs-lookup"><span data-stu-id="a5d2b-288">Power Management</span></span>](../power/power-management-reference.md)
-   [<span data-ttu-id="a5d2b-289">Serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="a5d2b-289">Remote Desktop Services</span></span>](../termserv/terminal-services-reference.md)
-   [<span data-ttu-id="a5d2b-290">Processos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-290">Processes</span></span>](../procthread/process-and-thread-reference.md)
-   [<span data-ttu-id="a5d2b-291">Serviços</span><span class="sxs-lookup"><span data-stu-id="a5d2b-291">Services</span></span>](../services/service-reference.md)
-   [<span data-ttu-id="a5d2b-292">Sincronização</span><span class="sxs-lookup"><span data-stu-id="a5d2b-292">Synchronization</span></span>](../sync/synchronization-reference.md)
-   [<span data-ttu-id="a5d2b-293">Threads</span><span class="sxs-lookup"><span data-stu-id="a5d2b-293">Threads</span></span>](../procthread/process-and-thread-reference.md)
-   [<span data-ttu-id="a5d2b-294">Compartilhamento de área de trabalho do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-294">Windows Desktop Sharing</span></span>](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [<span data-ttu-id="a5d2b-295">Informações do sistema Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-295">Windows System Information</span></span>](../sysinfo/windows-system-information.md)
    -   [<span data-ttu-id="a5d2b-296">Identificador e objetos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-296">Handle and Objects</span></span>](../sysinfo/handle-and-object-functions.md)
    -   [<span data-ttu-id="a5d2b-297">Registro</span><span class="sxs-lookup"><span data-stu-id="a5d2b-297">Registry</span></span>](../sysinfo/registry-reference.md)
    -   [<span data-ttu-id="a5d2b-298">Hora</span><span class="sxs-lookup"><span data-stu-id="a5d2b-298">Time</span></span>](../sysinfo/time-reference.md)
    -   [<span data-ttu-id="a5d2b-299">Provedor de tempo</span><span class="sxs-lookup"><span data-stu-id="a5d2b-299">Time Provider</span></span>](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a><span data-ttu-id="a5d2b-300">Segurança e identidade</span><span class="sxs-lookup"><span data-stu-id="a5d2b-300">Security and identity</span></span>

<span data-ttu-id="a5d2b-301">As APIs de [segurança e identidade](../devnotes/security.md) habilitam a autenticação de senha durante o logon, proteção condicional para todos os objetos do sistema compartilháveis, controle de acesso privilegiado, Rights Management e auditoria de segurança.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-301">The [Security and Identity](../devnotes/security.md) APIs enable password authentication at logon, discretionary protection for all sharable system objects, privileged access control, rights management, and security auditing.</span></span>

-   [<span data-ttu-id="a5d2b-302">Autenticação</span><span class="sxs-lookup"><span data-stu-id="a5d2b-302">Authentication</span></span>](../secauthn/authentication-reference.md)
-   [<span data-ttu-id="a5d2b-303">Autorização</span><span class="sxs-lookup"><span data-stu-id="a5d2b-303">Authorization</span></span>](../secauthz/authorization-reference.md)
-   [<span data-ttu-id="a5d2b-304">Registro de certificado</span><span class="sxs-lookup"><span data-stu-id="a5d2b-304">Certificate Enrollment</span></span>](../seccertenroll/certificate-enrollment-api-reference.md)
-   [<span data-ttu-id="a5d2b-305">Criptografia</span><span class="sxs-lookup"><span data-stu-id="a5d2b-305">Cryptography</span></span>](../seccrypto/cryptography-reference.md)
-   [<span data-ttu-id="a5d2b-306">CNG (criptografia próxima geração)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-306">Cryptographic Next Generation (CNG)</span></span>](../seccng/cng-reference.md)
-   <span data-ttu-id="a5d2b-307">[Serviços de diretório](/previous-versions//ms682458(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-307">[Directory Services](/previous-versions//ms682458(v=vs.85))</span></span>
    -   [<span data-ttu-id="a5d2b-308">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="a5d2b-308">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services-reference.md)
    -   [<span data-ttu-id="a5d2b-309">ADSI (interfaces de serviço Active Directory)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-309">Active Directory Service Interfaces (ADSI)</span></span>](../adsi/adsi-reference.md)
-   [<span data-ttu-id="a5d2b-310">Protocolo EAP (Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-310">Extensible Authentication Protocol (EAP)</span></span>](../eap/extensible-authentication-protocol-reference.md)
-   [<span data-ttu-id="a5d2b-311">Host de protocolo de autenticação extensível (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-311">Extensible Authentication Protocol Host (EAPHost)</span></span>](../eaphost/about-eap-host.md)
-   [<span data-ttu-id="a5d2b-312">Gerenciamento de senhas MS-CHAP</span><span class="sxs-lookup"><span data-stu-id="a5d2b-312">MS-CHAP Password Management</span></span>](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [<span data-ttu-id="a5d2b-313">NAP (proteção de acesso à rede)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-313">Network Access Protection (NAP)</span></span>](../nap/nap-reference.md)
-   [<span data-ttu-id="a5d2b-314">NPS (extensões do servidor de políticas de rede)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-314">Network Policy Server Extensions (NPS)</span></span>](../nps/ias-internet-authentication-service-reference.md)
-   [<span data-ttu-id="a5d2b-315">Controles dos pais</span><span class="sxs-lookup"><span data-stu-id="a5d2b-315">Parental Controls</span></span>](../parcon/parental-controls-reference.md)
-   [<span data-ttu-id="a5d2b-316">Provedores WMI de segurança</span><span class="sxs-lookup"><span data-stu-id="a5d2b-316">Security WMI Providers</span></span>](../secprov/security-wmi-providers-reference.md)
-   [<span data-ttu-id="a5d2b-317">Serviços de base do TPM (TBS)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-317">TPM Base Services (TBS)</span></span>](../tbs/tbs-reference.md)
-   [<span data-ttu-id="a5d2b-318">Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="a5d2b-318">Windows Biometric Framework</span></span>](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a><span data-ttu-id="a5d2b-319">Instalação e manutenção de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a5d2b-319">Application installation and servicing</span></span>

-   <span data-ttu-id="a5d2b-320">[Explorador de jogos](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-320">[Games Explorer](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-321">Assemblies lado a lado</span><span class="sxs-lookup"><span data-stu-id="a5d2b-321">Side-by-side Assemblies</span></span>](../sbscs/side-by-side-assemblies-reference.md)
-   [<span data-ttu-id="a5d2b-322">APIs de empacotamento, implantação e consulta</span><span class="sxs-lookup"><span data-stu-id="a5d2b-322">Packaging, deployment, and query APIs</span></span>](../appxpkg/api-reference.md
)
-   [<span data-ttu-id="a5d2b-323">Licença de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="a5d2b-323">Developer License</span></span>](../devlic/developer-license-apis.md)
-   [<span data-ttu-id="a5d2b-324">Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="a5d2b-324">Restart Manager</span></span>](../rstmgr/restart-manager-reference.md)
-   [<span data-ttu-id="a5d2b-325">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a5d2b-325">Windows Installer</span></span>](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a><span data-ttu-id="a5d2b-326">Administração e gerenciamento do sistema</span><span class="sxs-lookup"><span data-stu-id="a5d2b-326">System admin and management</span></span>

<span data-ttu-id="a5d2b-327">As interfaces de [Administração do sistema](../srvnodes/system-administration.md) permitem instalar, configurar e fazer a manutenção de aplicativos ou sistemas.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-327">The [System administration](../srvnodes/system-administration.md) interfaces enable you to install, configure, and service applications or systems.</span></span>

-   [<span data-ttu-id="a5d2b-328">Provedor WMI de Dados de Configuração da Inicialização</span><span class="sxs-lookup"><span data-stu-id="a5d2b-328">Boot Configuration Data WMI Provider</span></span>](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [<span data-ttu-id="a5d2b-329">Clusters de failover</span><span class="sxs-lookup"><span data-stu-id="a5d2b-329">Failover Clusters</span></span>](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [<span data-ttu-id="a5d2b-330">Gerenciador de Recursos de Servidor de Arquivos (FSRM)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-330">File Server Resource Manager (FSRM)</span></span>](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [<span data-ttu-id="a5d2b-331">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="a5d2b-331">Group Policy</span></span>](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [<span data-ttu-id="a5d2b-332">MMC (console de gerenciamento Microsoft) 2,0</span><span class="sxs-lookup"><span data-stu-id="a5d2b-332">Microsoft Management Console (MMC) 2.0</span></span>](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [<span data-ttu-id="a5d2b-333">NetShell</span><span class="sxs-lookup"><span data-stu-id="a5d2b-333">NetShell</span></span>](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [<span data-ttu-id="a5d2b-334">Infraestrutura de gerenciamento de configurações</span><span class="sxs-lookup"><span data-stu-id="a5d2b-334">Settings Management Infrastructure</span></span>](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [<span data-ttu-id="a5d2b-335">Log de Inventário de Software</span><span class="sxs-lookup"><span data-stu-id="a5d2b-335">Software Inventory Logging</span></span>](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [<span data-ttu-id="a5d2b-336">Licenciamento de software</span><span class="sxs-lookup"><span data-stu-id="a5d2b-336">Software Licensing</span></span>](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [<span data-ttu-id="a5d2b-337">Gerenciador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="a5d2b-337">Restart Manager</span></span>](../rstmgr/restart-manager-portal.md)
-   [<span data-ttu-id="a5d2b-338">Infraestrutura de gerenciamento de configurações</span><span class="sxs-lookup"><span data-stu-id="a5d2b-338">Settings Management Infrastructure</span></span>](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [<span data-ttu-id="a5d2b-339">Restauração do Sistema</span><span class="sxs-lookup"><span data-stu-id="a5d2b-339">System Restore</span></span>](../sr/system-restore-portal.md)
-   [<span data-ttu-id="a5d2b-340">Desligamento do sistema</span><span class="sxs-lookup"><span data-stu-id="a5d2b-340">System Shutdown</span></span>](../shutdown/system-shutdown.md)
-   [<span data-ttu-id="a5d2b-341">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a5d2b-341">Task Scheduler</span></span>](../taskschd/task-scheduler-start-page.md)
-   [<span data-ttu-id="a5d2b-342">Log de acesso do usuário</span><span class="sxs-lookup"><span data-stu-id="a5d2b-342">User Access Logging</span></span>](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [<span data-ttu-id="a5d2b-343">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a5d2b-343">Windows Virtual PC</span></span>](../vpc/virtual-pc-reference.md)
-   [<span data-ttu-id="a5d2b-344">Servidor virtual da Microsoft</span><span class="sxs-lookup"><span data-stu-id="a5d2b-344">Microsoft Virtual Server</span></span>](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [<span data-ttu-id="a5d2b-345">Provedor de balanceamento de carga de rede</span><span class="sxs-lookup"><span data-stu-id="a5d2b-345">Network Load Balancing Provider</span></span>](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [<span data-ttu-id="a5d2b-346">WMI do Windows Defender v2</span><span class="sxs-lookup"><span data-stu-id="a5d2b-346">Windows Defender WMI v2</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [<span data-ttu-id="a5d2b-347">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="a5d2b-347">Windows Deployment Services</span></span>](../wds/windows-deployment-services-portal.md)
-   [<span data-ttu-id="a5d2b-348">Vantagem do Windows Genuine</span><span class="sxs-lookup"><span data-stu-id="a5d2b-348">Windows Genuine Advantage</span></span>](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [<span data-ttu-id="a5d2b-349">Infraestrutura de gerenciamento do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-349">Windows Management Infrastructure</span></span>](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [<span data-ttu-id="a5d2b-350">WMI (Instrumentação de Gerenciamento do Windows)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-350">Windows Management Instrumentation (WMI)</span></span>](../wmisdk/wmi-reference.md)
-   [<span data-ttu-id="a5d2b-351">Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-351">Windows Remote Management</span></span>](../winrm/portal.md)
-   [<span data-ttu-id="a5d2b-352">Proteção de Recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-352">Windows Resource Protection</span></span>](../wfp/windows-resource-protection-portal.md)
-   <span data-ttu-id="a5d2b-353">[Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-353">[Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-354">Ferramenta de avaliação do sistema do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-354">Windows System Assessment Tool</span></span>](../winsat/winsat-reference.md)
-   [<span data-ttu-id="a5d2b-355">Windows Update Agent</span><span class="sxs-lookup"><span data-stu-id="a5d2b-355">Windows Update Agent</span></span>](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a><span data-ttu-id="a5d2b-356">Rede e Internet</span><span class="sxs-lookup"><span data-stu-id="a5d2b-356">Networking and internet</span></span>

<span data-ttu-id="a5d2b-357">As APIs de [rede](../devnotes/networking.md) permitem a comunicação entre aplicativos em uma rede.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-357">The [Networking](../devnotes/networking.md) APIs enable communication between applications over a network.</span></span> <span data-ttu-id="a5d2b-358">Você também pode criar e gerenciar o acesso a recursos compartilhados, como diretórios e impressoras de rede.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-358">You can also create and manage access to shared resources, such as directories and network printers.</span></span>

-   [<span data-ttu-id="a5d2b-359">Sistema de nome de domínio (DNS)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-359">Domain Name System (DNS)</span></span>](../dns/dns-reference.md)
-   [<span data-ttu-id="a5d2b-360">Protocolo DHCP</span><span class="sxs-lookup"><span data-stu-id="a5d2b-360">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
-   [<span data-ttu-id="a5d2b-361">Serviço de fax</span><span class="sxs-lookup"><span data-stu-id="a5d2b-361">Fax Service</span></span>](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [<span data-ttu-id="a5d2b-362">Assistente para Conexão</span><span class="sxs-lookup"><span data-stu-id="a5d2b-362">Get Connected Wizard</span></span>](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [<span data-ttu-id="a5d2b-363">Servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="a5d2b-363">HTTP Server</span></span>](../http/http-server-api-reference.md)
-   [<span data-ttu-id="a5d2b-364">Firewall e compartilhamento de conexão com a Internet</span><span class="sxs-lookup"><span data-stu-id="a5d2b-364">Internet Connection Sharing and Firewall</span></span>](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [<span data-ttu-id="a5d2b-365">Auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="a5d2b-365">IP Helper</span></span>](../iphlp/ip-helper-function-reference.md)
-   [<span data-ttu-id="a5d2b-366">Firewall de conexão com a Internet IPv6</span><span class="sxs-lookup"><span data-stu-id="a5d2b-366">IPv6 Internet Connection Firewall</span></span>](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [<span data-ttu-id="a5d2b-367">Base de informações de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a5d2b-367">Management Information Base</span></span>](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   <span data-ttu-id="a5d2b-368">[Serviço de enfileiramento de mensagens (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-368">[Message Queuing (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-369">Protocolo de alocação de cliente dinâmico (MADCAP) de endereço multicast</span><span class="sxs-lookup"><span data-stu-id="a5d2b-369">Multicast Address Dynamic Client Allocation Protocol (MADCAP)</span></span>](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [<span data-ttu-id="a5d2b-370">NAT (conversão de endereços de rede)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-370">Network Address Translation (NAT)</span></span>](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [<span data-ttu-id="a5d2b-371">NLM (Gerenciador de lista de rede)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-371">Network List Manager (NLM)</span></span>](../nla/network-list-manager-api-reference.md)
-   [<span data-ttu-id="a5d2b-372">Gerenciamento de rede</span><span class="sxs-lookup"><span data-stu-id="a5d2b-372">Network Management</span></span>](../netmgmt/network-management-reference.md)
-   [<span data-ttu-id="a5d2b-373">Gerenciamento de compartilhamento de rede</span><span class="sxs-lookup"><span data-stu-id="a5d2b-373">Network Share Management</span></span>](../netshare/network-share-management-reference.md)
-   [<span data-ttu-id="a5d2b-374">Ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="a5d2b-374">Peer-to-Peer</span></span>](../p2psdk/portal.md)
-   [<span data-ttu-id="a5d2b-375">QOS (qualidade de serviço)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-375">Quality of Service (QOS)</span></span>](/previous-versions/windows/desktop/qos/qos-reference)
-   [<span data-ttu-id="a5d2b-376">Chamada de Procedimento Remoto</span><span class="sxs-lookup"><span data-stu-id="a5d2b-376">Remote Procedure Call</span></span>](../rpc/reference.md)
-   [<span data-ttu-id="a5d2b-377">Serviço de roteamento e acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-377">Routing and Remote Access Service (RAS)</span></span>](../rras/portal.md)
-   [<span data-ttu-id="a5d2b-378">Protocolo SNMP</span><span class="sxs-lookup"><span data-stu-id="a5d2b-378">Simple Network Management Protocol (SNMP)</span></span>](../snmp/snmp-reference.md)
-   [<span data-ttu-id="a5d2b-379">Gerenciamento de SMB</span><span class="sxs-lookup"><span data-stu-id="a5d2b-379">SMB Management</span></span>](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [<span data-ttu-id="a5d2b-380">TAPI (interfaces de programação de aplicativo) de telefonia</span><span class="sxs-lookup"><span data-stu-id="a5d2b-380">Telephony Application Programming Interfaces (TAPI)</span></span>](../tapi/telephony-application-programming-interfaces.md)
-   [<span data-ttu-id="a5d2b-381">WebDAV</span><span class="sxs-lookup"><span data-stu-id="a5d2b-381">WebDAV</span></span>](../webdav/webdav-api-reference.md)
-   [<span data-ttu-id="a5d2b-382">Componente de protocolo WebSocket</span><span class="sxs-lookup"><span data-stu-id="a5d2b-382">WebSocket Protocol Component</span></span>](../websock/web-socket-protocol-component-api-portal.md)
-   <span data-ttu-id="a5d2b-383">Rede sem fio:</span><span class="sxs-lookup"><span data-stu-id="a5d2b-383">Wireless networking:</span></span>
    -   [<span data-ttu-id="a5d2b-384">Bluetooth</span><span class="sxs-lookup"><span data-stu-id="a5d2b-384">Bluetooth</span></span>](../bluetooth/bluetooth-reference.md)
    -   [<span data-ttu-id="a5d2b-385">IrDA</span><span class="sxs-lookup"><span data-stu-id="a5d2b-385">IrDA</span></span>](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [<span data-ttu-id="a5d2b-386">Banda larga móvel</span><span class="sxs-lookup"><span data-stu-id="a5d2b-386">Mobile Broadband</span></span>](../mbn/mobile-broadband-networks-api-reference.md)
    -   [<span data-ttu-id="a5d2b-387">WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="a5d2b-387">Native Wifi</span></span>](../nativewifi/native-wifi-reference.md)
    -   [<span data-ttu-id="a5d2b-388">Windows Connect agora</span><span class="sxs-lookup"><span data-stu-id="a5d2b-388">Windows Connect Now</span></span>](../wcn/windows-connect-now-reference.md)
    -   [<span data-ttu-id="a5d2b-389">Gerenciador de Conexão do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-389">Windows Connection Manager</span></span>](../wcm/windows-connection-manager-reference.md)
-   [<span data-ttu-id="a5d2b-390">Plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-390">Windows Filtering Platform</span></span>](../fwp/fwp-reference.md)
-   [<span data-ttu-id="a5d2b-391">Firewall do Windows com Advanced Security</span><span class="sxs-lookup"><span data-stu-id="a5d2b-391">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [<span data-ttu-id="a5d2b-392">WinHTTP (serviços HTTP do Windows)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-392">Windows HTTP Services (WinHTTP)</span></span>](../winhttp/winhttp-reference.md)
-   [<span data-ttu-id="a5d2b-393">Internet do Windows (WinINet)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-393">Windows Internet (WinINet)</span></span>](../wininet/wininet-reference.md)
-   [<span data-ttu-id="a5d2b-394">Sistema de rede do Windows (WNet)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-394">Windows Networking (WNet)</span></span>](../wnet/windows-networking-reference.md)
-   [<span data-ttu-id="a5d2b-395">Virtualização de rede do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-395">Windows Network Virtualization</span></span>](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   <span data-ttu-id="a5d2b-396">[Plataforma Windows RSS](/previous-versions/windows/desktop/ms684702(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-396">[Windows RSS Platform](/previous-versions/windows/desktop/ms684702(v=vs.85))</span></span>
-   [<span data-ttu-id="a5d2b-397">Windows Sockets (Winsock)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-397">Windows Sockets (Winsock)</span></span>](../winsock/winsock-reference.md)
-   [<span data-ttu-id="a5d2b-398">Serviços Web do Windows</span><span class="sxs-lookup"><span data-stu-id="a5d2b-398">Windows Web Services</span></span>](../wsw/windows-web-services-reference.md)
-   [<span data-ttu-id="a5d2b-399">Solicitação estendida HTTP XML</span><span class="sxs-lookup"><span data-stu-id="a5d2b-399">XML HTTP Extended Request</span></span>](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a><span data-ttu-id="a5d2b-400">APIs preteridas ou herdadas</span><span class="sxs-lookup"><span data-stu-id="a5d2b-400">Deprecated or legacy APIs</span></span>

<span data-ttu-id="a5d2b-401">Veja a seguir as tecnologias e as APIs que estão desatualizadas ou foram substituídas ou preteridas dos sistemas operacionais cliente e servidor do Windows.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-401">The following are technologies and APIs that are outdated or have been replaced or deprecated from the Windows client and server operating systems.</span></span>

-   <span data-ttu-id="a5d2b-402">[DirectMusic](/previous-versions/ms807133(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-402">[DirectMusic](/previous-versions/ms807133(v=msdn.10))</span></span>
-   <span data-ttu-id="a5d2b-403">[DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-403">[DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))</span></span>
-   <span data-ttu-id="a5d2b-404">O Microsoft [UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10)) agora está incluído com [o Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="a5d2b-404">[Microsoft UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10)) is now included with [Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).</span></span>
-   [<span data-ttu-id="a5d2b-405">Troca dinâmica de dados de rede (DDE)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-405">Network Dynamic Data Exchange (DDE)</span></span>](../ipc/network-dde-reference.md)
-   <span data-ttu-id="a5d2b-406">[Serviço de instalação remota](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)): em vez disso, use os [serviços de implantação do Windows](../wds/windows-deployment-services-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a5d2b-406">[Remote Installation Service](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)): Use [Windows Deployment Services](../wds/windows-deployment-services-portal.md) instead.</span></span>
-   <span data-ttu-id="a5d2b-407">[VDS (serviço de disco virtual)](../vds/vds-reference.md): Use o [Gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) .</span><span class="sxs-lookup"><span data-stu-id="a5d2b-407">[Virtual Disk Service (VDS)](../vds/vds-reference.md): Use [Windows Storage Management](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) instead.</span></span>
-   <span data-ttu-id="a5d2b-408">Serviços de terminal: use [serviços de área de trabalho remota](../termserv/terminal-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a5d2b-408">Terminal Services: Use [Remote Desktop Services](../termserv/terminal-services-reference.md).</span></span>
-   <span data-ttu-id="a5d2b-409">[Gerenciador de direitos do Windows Media](/previous-versions//bb614742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5d2b-409">[Windows Media Rights Manager](/previous-versions//bb614742(v=vs.85))</span></span>
-   <span data-ttu-id="a5d2b-410">[Sistema de mensagens do Windows (MAPI)](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi): use [MAPI do Office](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-410">[Windows Messaging (MAPI)](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi): Use [Office MAPI](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) instead.</span></span>
-   <span data-ttu-id="a5d2b-411">[Plataforma de gadget do Windows](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal): Crie aplicativos UWP em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-411">[Windows Gadget Platform](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal): Create UWP apps instead.</span></span>
-   <span data-ttu-id="a5d2b-412">[Barra lateral do Windows](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry): Crie aplicativos UWP em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-412">[Windows Sidebar](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry): Create UWP apps instead.</span></span>
-   <span data-ttu-id="a5d2b-413">[Windows SideShow](/previous-versions//ms744179(v=vs.85)): sem substituição.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-413">[Windows SideShow](/previous-versions//ms744179(v=vs.85)): No replacement.</span></span>
-   [<span data-ttu-id="a5d2b-414">Efeitos de bitmap do WPF</span><span class="sxs-lookup"><span data-stu-id="a5d2b-414">WPF Bitmap Effects</span></span>](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
