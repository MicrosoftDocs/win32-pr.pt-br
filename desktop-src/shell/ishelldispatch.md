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
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840887"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="bb29c-103">Objeto IShellDispatch</span><span class="sxs-lookup"><span data-stu-id="bb29c-103">IShellDispatch object</span></span>

<span data-ttu-id="bb29c-104">Representa um objeto no Shell.</span><span class="sxs-lookup"><span data-stu-id="bb29c-104">Represents an object in the Shell.</span></span> <span data-ttu-id="bb29c-105">Os métodos são fornecidos para controlar o Shell e executar comandos no Shell.</span><span class="sxs-lookup"><span data-stu-id="bb29c-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="bb29c-106">Também há métodos para obter outros objetos relacionados ao shell.</span><span class="sxs-lookup"><span data-stu-id="bb29c-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="bb29c-107">**IShellDispatch** é implementado e acessado por meio do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="bb29c-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="bb29c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bb29c-108">Members</span></span>

<span data-ttu-id="bb29c-109">O objeto **IShellDispatch** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bb29c-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="bb29c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb29c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bb29c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb29c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bb29c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb29c-112">Methods</span></span>

<span data-ttu-id="bb29c-113">O objeto **IShellDispatch** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="bb29c-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="bb29c-114">Método</span><span class="sxs-lookup"><span data-stu-id="bb29c-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="bb29c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb29c-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-117">Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de <a href="folder.md"><strong>pasta</strong></a> da pasta selecionada.</span><span class="sxs-lookup"><span data-stu-id="bb29c-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-119">Propaga todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb29c-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="bb29c-120">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas em cascata</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb29c-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-122">Executa o aplicativo do painel de controle especificado.</span><span class="sxs-lookup"><span data-stu-id="bb29c-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="bb29c-123">Se o aplicativo já estiver aberto, ele ativará a instância em execução.</span><span class="sxs-lookup"><span data-stu-id="bb29c-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="bb29c-124">A partir do Windows Vista, a maioria dos aplicativos do painel de controle são itens do Shell e não pode ser aberta com essa função.</span><span class="sxs-lookup"><span data-stu-id="bb29c-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="bb29c-125">Para abrir esses aplicativos do painel de controle, passe o nome canônico para control.exe.</span><span class="sxs-lookup"><span data-stu-id="bb29c-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="bb29c-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="bb29c-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-128">Ejeta o computador de sua estação de encaixe.</span><span class="sxs-lookup"><span data-stu-id="bb29c-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="bb29c-129">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>ejetar PC</strong>se o computador dá suporte a esse comando.</span><span class="sxs-lookup"><span data-stu-id="bb29c-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-130"><a href="ishelldispatch-explore.md"><strong>Explorar</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-131">Abre uma pasta especificada em uma Windows Explorer de dados.</span><span class="sxs-lookup"><span data-stu-id="bb29c-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-133">Exibe a <strong>caixa de diálogo</strong> Executar para o usuário.</span><span class="sxs-lookup"><span data-stu-id="bb29c-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-135">Exibe a caixa <strong>de diálogo Resultados da Pesquisa:</strong> Computadores.</span><span class="sxs-lookup"><span data-stu-id="bb29c-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="bb29c-136">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="bb29c-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-138">Exibe a caixa <strong>de diálogo Encontrar: Todos os</strong> Arquivos.</span><span class="sxs-lookup"><span data-stu-id="bb29c-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="bb29c-139">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e, em seguida, selecionar <strong>Pesquisar</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb29c-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-140"><a href="ishelldispatch-help.md"><strong>Ajuda</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-141">Exibe a janela Ajuda e Suporte do Windows.</span><span class="sxs-lookup"><span data-stu-id="bb29c-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="bb29c-142">Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Ajuda e Suporte.</strong></span><span class="sxs-lookup"><span data-stu-id="bb29c-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-144">Minimiza todas as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb29c-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="bb29c-145">Esse método tem o mesmo efeito que clicar com o botão direito do <strong></strong> mouse na barra de tarefas e selecionar Minimizar Todas as <strong>Janelas</strong> em sistemas mais antigos ou clicar no ícone Mostrar Área de Trabalho na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bb29c-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-146"><a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-147">Cria e retorna um <a href="folder.md"><strong>objeto Folder</strong></a> para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="bb29c-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-148"><a href="ishelldispatch-open.md"><strong>Aberto</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-149">Abre a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="bb29c-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-151">Atualiza o conteúdo do menu <strong>Iniciar</strong> .</span><span class="sxs-lookup"><span data-stu-id="bb29c-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="bb29c-152">Usado apenas com sistemas anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb29c-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-154">Exibe a caixa de diálogo <strong>data e hora</strong> .</span><span class="sxs-lookup"><span data-stu-id="bb29c-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="bb29c-155">Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar <strong>Ajustar data/hora</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb29c-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-157">Exibe a caixa de diálogo <strong>desligar o Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="bb29c-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="bb29c-158">Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>desligar</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb29c-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-161">Organiza todas as janelas na área de trabalho horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="bb29c-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="bb29c-162">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Mostrar janelas empilhadas</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb29c-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-164">Organiza todas as janelas na área de trabalho verticalmente.</span><span class="sxs-lookup"><span data-stu-id="bb29c-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="bb29c-165">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Mostrar janelas lado a lado</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb29c-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-166"><a href="ishelldispatch-trayproperties.md"><strong>Bandejaproperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-167">Exibe a <strong>barra de tarefas e a caixa de diálogo Propriedades do menu iniciar</strong> .</span><span class="sxs-lookup"><span data-stu-id="bb29c-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="bb29c-168">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Propriedades</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb29c-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="bb29c-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-170">Restaura todas as janelas da área de trabalho para o estado em que estavam antes do último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="bb29c-171">Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra <strong></strong> de tarefas e selecionar Desfazer Minimizar Todas as <strong>Janelas</strong> (em sistemas mais antigos) ou um segundo clique do ícone Mostrar Área de Trabalho na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bb29c-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bb29c-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bb29c-173">Cria e retorna um <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb29c-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="bb29c-174">Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao Shell.</span><span class="sxs-lookup"><span data-stu-id="bb29c-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="bb29c-175">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bb29c-175">Properties</span></span>

<span data-ttu-id="bb29c-176">O **objeto IShellDispatch** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bb29c-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="bb29c-177">Propriedade</span><span class="sxs-lookup"><span data-stu-id="bb29c-177">Property</span></span>                                                     | <span data-ttu-id="bb29c-178">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="bb29c-178">Access type</span></span>          | <span data-ttu-id="bb29c-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb29c-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="bb29c-180">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="bb29c-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="bb29c-181">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb29c-181">Read-only</span></span><br/> | <span data-ttu-id="bb29c-182">Contém um objeto que representa um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bb29c-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="bb29c-183">**Pai**</span><span class="sxs-lookup"><span data-stu-id="bb29c-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="bb29c-184">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb29c-184">Read-only</span></span><br/> | <span data-ttu-id="bb29c-185">Recupera um objeto que representa o pai do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="bb29c-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb29c-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb29c-186">Requirements</span></span>



| <span data-ttu-id="bb29c-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb29c-187">Requirement</span></span> | <span data-ttu-id="bb29c-188">Valor</span><span class="sxs-lookup"><span data-stu-id="bb29c-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb29c-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb29c-189">Minimum supported client</span></span><br/> | <span data-ttu-id="bb29c-190">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bb29c-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bb29c-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb29c-191">Minimum supported server</span></span><br/> | <span data-ttu-id="bb29c-192">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bb29c-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb29c-193">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bb29c-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb29c-194"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="bb29c-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bb29c-195">Idl</span><span class="sxs-lookup"><span data-stu-id="bb29c-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb29c-196"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb29c-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bb29c-197">DLL</span><span class="sxs-lookup"><span data-stu-id="bb29c-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb29c-198"><dt>Shell32.dll (versão 4.71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bb29c-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb29c-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb29c-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb29c-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="bb29c-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="bb29c-201">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="bb29c-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
