---
description: Representa os objetos no Shell. Os métodos são fornecidos para controlar o Shell e executar comandos no Shell. Também há métodos para obter outros objetos relacionados ao shell.
title: 'Objeto shell (Shldisp.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 3e891278d98ca2eb51fca11054cba01947e03c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829702"
---
# <a name="shell-object"></a><span data-ttu-id="46c10-105">Objeto Shell</span><span class="sxs-lookup"><span data-stu-id="46c10-105">Shell object</span></span>

<span data-ttu-id="46c10-106">Representa os objetos no Shell.</span><span class="sxs-lookup"><span data-stu-id="46c10-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="46c10-107">Os métodos são fornecidos para controlar o Shell e executar comandos no Shell.</span><span class="sxs-lookup"><span data-stu-id="46c10-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="46c10-108">Também há métodos para obter outros objetos relacionados ao shell.</span><span class="sxs-lookup"><span data-stu-id="46c10-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="46c10-109">Membros</span><span class="sxs-lookup"><span data-stu-id="46c10-109">Members</span></span>

<span data-ttu-id="46c10-110">O objeto **shell** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="46c10-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="46c10-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="46c10-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="46c10-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46c10-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="46c10-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="46c10-113">Methods</span></span>

<span data-ttu-id="46c10-114">O objeto **shell** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="46c10-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="46c10-115">Método</span><span class="sxs-lookup"><span data-stu-id="46c10-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="46c10-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="46c10-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-118">Adiciona um arquivo à lista MRU (usada mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="46c10-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-120">Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de <a href="folder.md"><strong>pasta</strong></a> da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="46c10-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-122">Determina se o usuário atual pode iniciar e parar o serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="46c10-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-124">Propaga todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="46c10-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="46c10-125">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas em cascata</strong>.</span><span class="sxs-lookup"><span data-stu-id="46c10-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-127">Executa o aplicativo do painel de controle (\*. cpl) especificado.</span><span class="sxs-lookup"><span data-stu-id="46c10-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="46c10-128">Se o aplicativo já estiver aberto, ele ativará a instância em execução.</span><span class="sxs-lookup"><span data-stu-id="46c10-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="46c10-129">A partir do Windows Vista, a maioria dos aplicativos do painel de controle são itens do Shell e não pode ser aberta com essa função.</span><span class="sxs-lookup"><span data-stu-id="46c10-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="46c10-130">Para abrir esses aplicativos do painel de controle, passe o nome canônico para control.exe.</span><span class="sxs-lookup"><span data-stu-id="46c10-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="46c10-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="46c10-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-133">Ejeta o computador de sua estação de encaixe.</span><span class="sxs-lookup"><span data-stu-id="46c10-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="46c10-134">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Ejetar PC</strong>se o seu computador oferecer suporte a esse comando.</span><span class="sxs-lookup"><span data-stu-id="46c10-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-135"><a href="shell-explore.md"><strong>Explorar</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-136">Abre uma pasta especificada em uma janela do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="46c10-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-138">Obtém o valor de uma política especificada do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="46c10-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-140">Exibe a caixa de diálogo <strong>executar</strong> para o usuário.</span><span class="sxs-lookup"><span data-stu-id="46c10-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="46c10-141">Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>executar</strong>.</span><span class="sxs-lookup"><span data-stu-id="46c10-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-143">Exibe a caixa de diálogo <strong>resultados da pesquisa: computadores</strong> .</span><span class="sxs-lookup"><span data-stu-id="46c10-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="46c10-144">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="46c10-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-146">Exibe a caixa de diálogo <strong>localizar: todos os arquivos</strong> .</span><span class="sxs-lookup"><span data-stu-id="46c10-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="46c10-147">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Pesquisar</strong> (ou seu equivalente em sistemas anteriores ao Windows XP).</span><span class="sxs-lookup"><span data-stu-id="46c10-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-149">Exibe a caixa de diálogo <strong>Localizar impressora</strong> .</span><span class="sxs-lookup"><span data-stu-id="46c10-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetDefinition</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-151">Recupera uma configuração de shell global.</span><span class="sxs-lookup"><span data-stu-id="46c10-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-153">Recupera informações do sistema.</span><span class="sxs-lookup"><span data-stu-id="46c10-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-154"><a href="shell-help.md"><strong>Ajuda</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-155">Exibe o centro de ajuda e suporte do Windows.</span><span class="sxs-lookup"><span data-stu-id="46c10-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="46c10-156">Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>ajuda e suporte</strong>.</span><span class="sxs-lookup"><span data-stu-id="46c10-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-158">Recupera a configuração de restrição de um grupo do registro.</span><span class="sxs-lookup"><span data-stu-id="46c10-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-160">Retorna um valor que indica se um serviço específico está em execução.</span><span class="sxs-lookup"><span data-stu-id="46c10-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-162">Minimiza todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="46c10-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="46c10-163">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>minimizar todas as janelas</strong> em sistemas mais antigos ou clicar no ícone <strong>Mostrar área de trabalho</strong> na área início rápido da barra de tarefas no Windows 2000 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="46c10-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-165">Cria e retorna um objeto de <a href="folder.md"><strong>pasta</strong></a> para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="46c10-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-166"><a href="shell-open.md"><strong>Abrir</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-167">Abre a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="46c10-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-169">Atualiza o conteúdo do menu <strong>Iniciar</strong> .</span><span class="sxs-lookup"><span data-stu-id="46c10-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="46c10-170">Usado apenas com sistemas anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="46c10-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-172">Exibe o painel de pesquisa de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="46c10-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>Iniciar</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-174">Inicia um serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="46c10-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>Parar</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-176">Interrompe um serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="46c10-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-178">Exibe a caixa de diálogo <strong>Propriedades de data e hora</strong> .</span><span class="sxs-lookup"><span data-stu-id="46c10-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="46c10-179">Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar <strong>Ajustar data/hora</strong>.</span><span class="sxs-lookup"><span data-stu-id="46c10-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-181">Executa uma operação especificada em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="46c10-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-183">Exibe uma barra de navegador.</span><span class="sxs-lookup"><span data-stu-id="46c10-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-185">Exibe a caixa de diálogo <strong>desligar o Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="46c10-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="46c10-186">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>desligar</strong>.</span><span class="sxs-lookup"><span data-stu-id="46c10-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-189">Organiza todas as janelas na área de trabalho horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="46c10-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="46c10-190">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas de bloco horizontalmente</strong>.</span><span class="sxs-lookup"><span data-stu-id="46c10-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-192">Organiza todas as janelas na área de trabalho verticalmente.</span><span class="sxs-lookup"><span data-stu-id="46c10-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="46c10-193">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas de peças verticalmente</strong>.</span><span class="sxs-lookup"><span data-stu-id="46c10-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-195">Exibe ou oculta a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="46c10-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-196"><a href="shell-trayproperties.md"><strong>Bandejaproperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-197">Exibe a <strong>barra de tarefas e a caixa de diálogo Propriedades do menu iniciar</strong> .</span><span class="sxs-lookup"><span data-stu-id="46c10-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="46c10-198">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Propriedades</strong>.</span><span class="sxs-lookup"><span data-stu-id="46c10-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-200">Restaura todas as janelas da área de trabalho para o mesmo estado em que estavam antes do último comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="46c10-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="46c10-201">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>desfazer minimizar todas as janelas</strong> em sistemas mais antigos ou um segundo clique no ícone <strong>Mostrar área de trabalho</strong> na área início rápido da barra de tarefas no Windows 2000 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="46c10-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-203">Cria e retorna um objeto <a href="shellwindows.md"><strong>ShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="46c10-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="46c10-204">Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao shell.</span><span class="sxs-lookup"><span data-stu-id="46c10-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="46c10-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-206">Exibe a caixa de diálogo <strong>segurança do Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="46c10-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="46c10-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="46c10-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="46c10-208">Exibe as janelas abertas em uma pilha 3D que você pode percorrer.</span><span class="sxs-lookup"><span data-stu-id="46c10-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="46c10-209">Propriedades</span><span class="sxs-lookup"><span data-stu-id="46c10-209">Properties</span></span>

<span data-ttu-id="46c10-210">O objeto **shell** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="46c10-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="46c10-211">Propriedade</span><span class="sxs-lookup"><span data-stu-id="46c10-211">Property</span></span>                                            | <span data-ttu-id="46c10-212">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="46c10-212">Access type</span></span>          | <span data-ttu-id="46c10-213">Description</span><span class="sxs-lookup"><span data-stu-id="46c10-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="46c10-214">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="46c10-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="46c10-215">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c10-215">Read-only</span></span><br/> | <span data-ttu-id="46c10-216">Contém o objeto de aplicativo do objeto.</span><span class="sxs-lookup"><span data-stu-id="46c10-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="46c10-217">**Pai**</span><span class="sxs-lookup"><span data-stu-id="46c10-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="46c10-218">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="46c10-218">Read-only</span></span><br/> | <span data-ttu-id="46c10-219">Obtém um objeto que representa o pai do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="46c10-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="46c10-220">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46c10-220">Requirements</span></span>



| <span data-ttu-id="46c10-221">Requisito</span><span class="sxs-lookup"><span data-stu-id="46c10-221">Requirement</span></span> | <span data-ttu-id="46c10-222">Valor</span><span class="sxs-lookup"><span data-stu-id="46c10-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c10-223">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46c10-223">Minimum supported client</span></span><br/> | <span data-ttu-id="46c10-224">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="46c10-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="46c10-225">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46c10-225">Minimum supported server</span></span><br/> | <span data-ttu-id="46c10-226">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46c10-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46c10-227">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46c10-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="46c10-228"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="46c10-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="46c10-229">INSERI</span><span class="sxs-lookup"><span data-stu-id="46c10-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46c10-230"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46c10-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="46c10-231">DLL</span><span class="sxs-lookup"><span data-stu-id="46c10-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46c10-232"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="46c10-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
