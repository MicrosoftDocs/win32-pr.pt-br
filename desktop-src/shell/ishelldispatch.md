---
description: Representa um objeto no Shell.
title: Objeto IShellDispatch (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 20c6cc9f0b3a2e2fde8f56311564d63bc1cc9c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967531"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="6ab80-103">Objeto IShellDispatch</span><span class="sxs-lookup"><span data-stu-id="6ab80-103">IShellDispatch object</span></span>

<span data-ttu-id="6ab80-104">Representa um objeto no Shell.</span><span class="sxs-lookup"><span data-stu-id="6ab80-104">Represents an object in the Shell.</span></span> <span data-ttu-id="6ab80-105">Os métodos são fornecidos para controlar o Shell e executar comandos no Shell.</span><span class="sxs-lookup"><span data-stu-id="6ab80-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="6ab80-106">Também há métodos para obter outros objetos relacionados ao shell.</span><span class="sxs-lookup"><span data-stu-id="6ab80-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="6ab80-107">**IShellDispatch** é implementado e acessado por meio do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="6ab80-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="6ab80-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6ab80-108">Members</span></span>

<span data-ttu-id="6ab80-109">O objeto **IShellDispatch** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6ab80-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="6ab80-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ab80-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6ab80-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6ab80-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6ab80-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ab80-112">Methods</span></span>

<span data-ttu-id="6ab80-113">O objeto **IShellDispatch** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6ab80-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="6ab80-114">Método</span><span class="sxs-lookup"><span data-stu-id="6ab80-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="6ab80-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ab80-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-117">Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de <a href="folder.md"><strong>pasta</strong></a> da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="6ab80-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-119">Propaga todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6ab80-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="6ab80-120">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas em cascata</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab80-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-122">Executa o aplicativo do painel de controle especificado.</span><span class="sxs-lookup"><span data-stu-id="6ab80-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="6ab80-123">Se o aplicativo já estiver aberto, ele ativará a instância em execução.</span><span class="sxs-lookup"><span data-stu-id="6ab80-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="6ab80-124">A partir do Windows Vista, a maioria dos aplicativos do painel de controle são itens do Shell e não pode ser aberta com essa função.</span><span class="sxs-lookup"><span data-stu-id="6ab80-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="6ab80-125">Para abrir esses aplicativos do painel de controle, passe o nome canônico para control.exe.</span><span class="sxs-lookup"><span data-stu-id="6ab80-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="6ab80-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6ab80-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-128">Ejeta o computador de sua estação de encaixe.</span><span class="sxs-lookup"><span data-stu-id="6ab80-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="6ab80-129">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Ejetar PC</strong>se o seu computador oferecer suporte a esse comando.</span><span class="sxs-lookup"><span data-stu-id="6ab80-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-130"><a href="ishelldispatch-explore.md"><strong>Explorar</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-131">Abre uma pasta especificada em uma janela do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="6ab80-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-133">Exibe a caixa de diálogo <strong>executar</strong> para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6ab80-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-135">Exibe a caixa de diálogo <strong>resultados da pesquisa: computadores</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ab80-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="6ab80-136">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="6ab80-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-138">Exibe a caixa de diálogo <strong>localizar: todos os arquivos</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ab80-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="6ab80-139">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Pesquisar</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab80-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-140"><a href="ishelldispatch-help.md"><strong>Ajuda</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-141">Exibe a janela de ajuda e suporte do Windows.</span><span class="sxs-lookup"><span data-stu-id="6ab80-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="6ab80-142">Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>ajuda e suporte</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab80-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-144">Minimiza todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6ab80-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="6ab80-145">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>minimizar todas as janelas</strong> em sistemas mais antigos ou clicar no ícone <strong>Mostrar área de trabalho</strong> na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="6ab80-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-147">Cria e retorna um objeto de <a href="folder.md"><strong>pasta</strong></a> para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="6ab80-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-148"><a href="ishelldispatch-open.md"><strong>Abrir</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-149">Abre a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="6ab80-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-151">Atualiza o conteúdo do menu <strong>Iniciar</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ab80-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="6ab80-152">Usado apenas com sistemas anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ab80-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-154">Exibe a caixa de diálogo <strong>data e hora</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ab80-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="6ab80-155">Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar <strong>Ajustar data/hora</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab80-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-157">Exibe a caixa de diálogo <strong>desligar o Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ab80-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="6ab80-158">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>desligar</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab80-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-161">Organiza todas as janelas na área de trabalho horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="6ab80-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="6ab80-162">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Mostrar janelas empilhadas</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab80-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-164">Organiza todas as janelas na área de trabalho verticalmente.</span><span class="sxs-lookup"><span data-stu-id="6ab80-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="6ab80-165">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Mostrar janelas lado a lado</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab80-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-166"><a href="ishelldispatch-trayproperties.md"><strong>Bandejaproperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-167">Exibe a <strong>barra de tarefas e a caixa de diálogo Propriedades do menu iniciar</strong> .</span><span class="sxs-lookup"><span data-stu-id="6ab80-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="6ab80-168">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Propriedades</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ab80-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6ab80-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-170">Restaura todas as janelas da área de trabalho para o estado em que estavam antes do último comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ab80-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="6ab80-171">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>desfazer minimizar todas as janelas</strong> (em sistemas mais antigos) ou um segundo clique no ícone <strong>Mostrar área de trabalho</strong> na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="6ab80-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6ab80-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ab80-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6ab80-173">Cria e retorna um objeto <a href="shellwindows.md"><strong>ShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ab80-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="6ab80-174">Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao shell.</span><span class="sxs-lookup"><span data-stu-id="6ab80-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="6ab80-175">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6ab80-175">Properties</span></span>

<span data-ttu-id="6ab80-176">O objeto **IShellDispatch** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6ab80-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="6ab80-177">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6ab80-177">Property</span></span>                                                     | <span data-ttu-id="6ab80-178">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="6ab80-178">Access type</span></span>          | <span data-ttu-id="6ab80-179">Description</span><span class="sxs-lookup"><span data-stu-id="6ab80-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="6ab80-180">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="6ab80-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="6ab80-181">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ab80-181">Read-only</span></span><br/> | <span data-ttu-id="6ab80-182">Contém um objeto que representa um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ab80-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="6ab80-183">**Pai**</span><span class="sxs-lookup"><span data-stu-id="6ab80-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="6ab80-184">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ab80-184">Read-only</span></span><br/> | <span data-ttu-id="6ab80-185">Recupera um objeto que representa o pai do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="6ab80-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6ab80-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ab80-186">Requirements</span></span>



| <span data-ttu-id="6ab80-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab80-187">Requirement</span></span> | <span data-ttu-id="6ab80-188">Valor</span><span class="sxs-lookup"><span data-stu-id="6ab80-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab80-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ab80-189">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab80-190">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ab80-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6ab80-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ab80-191">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab80-192">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ab80-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6ab80-193">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6ab80-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab80-194"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ab80-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6ab80-195">INSERI</span><span class="sxs-lookup"><span data-stu-id="6ab80-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ab80-196"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ab80-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6ab80-197">DLL</span><span class="sxs-lookup"><span data-stu-id="6ab80-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ab80-198"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab80-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ab80-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ab80-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab80-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="6ab80-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="6ab80-201">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="6ab80-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
