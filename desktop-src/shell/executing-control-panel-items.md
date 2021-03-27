---
description: Discute métodos de abrir um item do painel de controle para o Windows Vista e sistemas posteriores, além de abranger comandos herdados do painel de controle.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Executando itens do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989046"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="4cb0c-103">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="4cb0c-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="4cb0c-104">Se você estiver procurando a lista de nomes canônicos e de módulo para itens do painel de controle, consulte [nomes canônicos de itens do painel de controle](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="4cb0c-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="4cb0c-105">Há duas maneiras de abrir um item do painel de controle:</span><span class="sxs-lookup"><span data-stu-id="4cb0c-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="4cb0c-106">O usuário pode abrir o painel de controle e, em seguida, abrir um item clicando ou clicando duas vezes no ícone do item.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="4cb0c-107">O usuário ou um aplicativo pode iniciar um item do painel de controle executando-o diretamente do prompt de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="4cb0c-108">Um aplicativo pode abrir o painel de controle programaticamente usando a função [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="4cb0c-109">O exemplo a seguir mostra como um aplicativo pode iniciar o item do painel de controle chamado **MyCpl.cpl** usando a função [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="4cb0c-110">Quando um item do painel de controle é aberto por meio de uma linha de comando, você pode instruí-lo a abrir para uma determinada guia no item.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="4cb0c-111">Devido à adição e remoção de determinadas guias em alguns itens do painel de controle do Windows Vista, a numeração das guias pode ter mudado do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="4cb0c-112">Por exemplo, os exemplos a seguir iniciam a quarta guia no item do sistema no Windows XP e a terceira guia do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="4cb0c-113">Este tópico aborda o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4cb0c-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="4cb0c-114">Nomes canônicos do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cb0c-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="4cb0c-115">Novos comandos para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cb0c-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="4cb0c-116">Comandos do painel de controle herdado</span><span class="sxs-lookup"><span data-stu-id="4cb0c-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="4cb0c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4cb0c-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="4cb0c-118">Nomes canônicos do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cb0c-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="4cb0c-119">No Windows Vista e posterior, o método preferencial de iniciar um item do painel de controle a partir de uma linha de comando é usar o nome canônico do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="4cb0c-120">Um nome canônico é uma cadeia de caracteres não localizada que o item do painel de controle declara no registro.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="4cb0c-121">O valor de usar um nome canônico é que ele abstrai o nome do módulo do item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="4cb0c-122">Um item pode ser implementado em uma. dll e, posteriormente, ser reimplementado como um. exe ou alterar o nome do módulo.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="4cb0c-123">Desde que o nome canônico permaneça o mesmo, então qualquer programa que o abre usando esse nome canônico não precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="4cb0c-124">Por convenção, o nome canônico é formado como "Corporationname. ControlPanelItemName".</span><span class="sxs-lookup"><span data-stu-id="4cb0c-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="4cb0c-125">O exemplo a seguir mostra como um aplicativo pode iniciar o item do painel de controle **Windows Update** com [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span><span class="sxs-lookup"><span data-stu-id="4cb0c-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="4cb0c-126">Para iniciar um item do painel de controle com seu nome canônico, use: "% SystemRoot% \\ system32 \\control.exe/name *canônicaname*"</span><span class="sxs-lookup"><span data-stu-id="4cb0c-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="4cb0c-127">Para abrir uma subpágina específica em um item ou abri-la com parâmetros adicionais, use: "% SystemRoot% \\ system32 \\control.exe/name **Canônicaname** / **PageName**"</span><span class="sxs-lookup"><span data-stu-id="4cb0c-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="4cb0c-128">Um aplicativo também pode implementar o método [**IOpenControlPanel:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) para iniciar itens do painel de controle, incluindo a capacidade de abrir uma subpágina específica.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="4cb0c-129">Para obter uma lista completa de nomes canônicos de itens do painel de controle, consulte [nomes canônicos de itens do painel de controle](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="4cb0c-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="4cb0c-130">Novos comandos para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cb0c-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="4cb0c-131">No Windows Vista, algumas opções que foram acessadas por um módulo. cpl no Windows XP agora são implementadas como arquivos. exe.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="4cb0c-132">Isso fornece segurança adicional, permitindo que os usuários padrão sejam solicitados a fornecer credenciais de administrador ao tentar iniciar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="4cb0c-133">As opções que não exigem segurança extra são acessadas pelas mesmas linhas de comando que foram usadas no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="4cb0c-134">Veja a seguir uma lista de comandos usados no Windows Vista para acessar guias específicas de itens do painel de controle:</span><span class="sxs-lookup"><span data-stu-id="4cb0c-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="4cb0c-135">Personalização</span><span class="sxs-lookup"><span data-stu-id="4cb0c-135">Personalization</span></span>

-   <span data-ttu-id="4cb0c-136">Tamanho da fonte e DPI:% WINDIR% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="4cb0c-137">Resolução de tela:% WINDIR% \\ system32 \\control.exe desk.cpl, configurações,@Settings</span><span class="sxs-lookup"><span data-stu-id="4cb0c-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="4cb0c-138">Configurações de exibição:% WINDIR% \\ system32 \\control.exe desk.cpl, configurações,@Settings</span><span class="sxs-lookup"><span data-stu-id="4cb0c-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="4cb0c-139">Temas:% WINDIR% \\ system32 \\control.exe desk.cpl, temas,@Themes</span><span class="sxs-lookup"><span data-stu-id="4cb0c-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="4cb0c-140">Proteção de tela:% WINDIR% \\ system32 \\control.exe desk.cpl, proteção de tela,@screensaver</span><span class="sxs-lookup"><span data-stu-id="4cb0c-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="4cb0c-141">Vários monitores:% WINDIR% \\ system32 \\control.exe desk.cpl, monitor,@Monitor</span><span class="sxs-lookup"><span data-stu-id="4cb0c-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="4cb0c-142">Esquema de cores:% WINDIR% \\ system32 \\control.exe/name Microsoft. Personalization/pageColorization</span><span class="sxs-lookup"><span data-stu-id="4cb0c-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="4cb0c-143">Plano de fundo da área de trabalho:% WINDIR% \\ system32 \\control.exe/name Microsoft. Personalization/pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="4cb0c-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="4cb0c-144">As edições inicial e básica não dão suporte ao comando control.exe/name Microsoft. Personalization.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="4cb0c-145">Sistema</span><span class="sxs-lookup"><span data-stu-id="4cb0c-145">System</span></span>

-   <span data-ttu-id="4cb0c-146">Desempenho:% WINDIR% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="4cb0c-147">Acesso remoto:% WINDIR% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="4cb0c-148">Nome do computador:% WINDIR% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="4cb0c-149">Proteção do sistema:% WINDIR% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="4cb0c-150">Propriedades avançadas do sistema:% WINDIR% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="4cb0c-151">Programas e Recursos</span><span class="sxs-lookup"><span data-stu-id="4cb0c-151">Programs and Features</span></span>

-   <span data-ttu-id="4cb0c-152">Adicionar ou remover programas:% WINDIR% \\ system32 \\control.exe/name Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="4cb0c-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="4cb0c-153">Recursos do Windows:% WINDIR% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="4cb0c-154">Opções regionais e de idioma</span><span class="sxs-lookup"><span data-stu-id="4cb0c-154">Regional and Language Options</span></span>

-   <span data-ttu-id="4cb0c-155">Teclado:% SystemRoot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions//p: "teclado"</span><span class="sxs-lookup"><span data-stu-id="4cb0c-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="4cb0c-156">Local:% SystemRoot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions//p: "local"</span><span class="sxs-lookup"><span data-stu-id="4cb0c-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="4cb0c-157">Administrativo:% SystemRoot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions//p: "administrativo"</span><span class="sxs-lookup"><span data-stu-id="4cb0c-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="4cb0c-158">Opções de Pasta</span><span class="sxs-lookup"><span data-stu-id="4cb0c-158">Folder Options</span></span>

-   <span data-ttu-id="4cb0c-159">Pesquisa de pastas:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opções \_ rundll 2</span><span class="sxs-lookup"><span data-stu-id="4cb0c-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="4cb0c-160">Associações de arquivo:% WINDIR% \\ system32 \\control.exe/name Microsoft. defaultprograms/pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="4cb0c-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="4cb0c-161">Exibição:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opções \_ rundll 7</span><span class="sxs-lookup"><span data-stu-id="4cb0c-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="4cb0c-162">Geral:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opções \_ rundll 0</span><span class="sxs-lookup"><span data-stu-id="4cb0c-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="4cb0c-163">Opções de Energia</span><span class="sxs-lookup"><span data-stu-id="4cb0c-163">Power Options</span></span>

-   <span data-ttu-id="4cb0c-164">Editar configurações do plano atual:% WINDIR% \\ system32 \\control.exe/name Microsoft. poweroptions/pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="4cb0c-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="4cb0c-165">Configurações do sistema:% WINDIR% \\ system32 \\control.exe/name Microsoft. poweroptions/pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="4cb0c-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="4cb0c-166">Criar um plano de energia:% WINDIR% \\ system32 \\control.exe/name Microsoft. poweroptions/pageCreateNewPlan</span><span class="sxs-lookup"><span data-stu-id="4cb0c-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="4cb0c-167">Não há nenhum comando canônico para a página de configurações avançadas, ele é acessado da maneira mais antiga:% WINDIR% \\ system32 \\control.exe powercfg.cpl,, 3</span><span class="sxs-lookup"><span data-stu-id="4cb0c-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="4cb0c-168">Comandos do painel de controle herdado</span><span class="sxs-lookup"><span data-stu-id="4cb0c-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="4cb0c-169">Quando você usa a função [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) , o sistema pode reconhecer comandos especiais do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="4cb0c-170">Esses comandos são preessados no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4cb0c-171">Área de trabalho control.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="4cb0c-172">Inicia a janela <strong>Propriedades de exibição</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4cb0c-173">As edições inicial e básica não oferecem suporte a esse comando.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cb0c-174">Cor control.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-174">control.exe color</span></span></td>
<td><span data-ttu-id="4cb0c-175">Inicia a janela <strong>Propriedades de exibição</strong> com a guia <strong>aparência</strong> selecionada.</span><span class="sxs-lookup"><span data-stu-id="4cb0c-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cb0c-176">Data/hora control.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="4cb0c-177">Inicia a janela de <strong>Propriedades de data e hora</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cb0c-178">control.exe internacional</span><span class="sxs-lookup"><span data-stu-id="4cb0c-178">control.exe international</span></span></td>
<td><span data-ttu-id="4cb0c-179">Inicia a janela <strong>Opções regionais e de idioma</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cb0c-180">control.exe mouse</span><span class="sxs-lookup"><span data-stu-id="4cb0c-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="4cb0c-181">Inicia a janela <strong>Propriedades do mouse</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cb0c-182">control.exe teclado</span><span class="sxs-lookup"><span data-stu-id="4cb0c-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="4cb0c-183">Inicia a janela <strong>Propriedades do teclado</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cb0c-184">control.exe impressoras</span><span class="sxs-lookup"><span data-stu-id="4cb0c-184">control.exe printers</span></span></td>
<td><span data-ttu-id="4cb0c-185">Exibe a pasta <strong>impressoras e aparelhos de fax</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cb0c-186">control.exe fontes</span><span class="sxs-lookup"><span data-stu-id="4cb0c-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="4cb0c-187">Exibe a pasta <strong>fontes</strong> .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4cb0c-188">Para sistemas Windows 2000 e posteriores:</span><span class="sxs-lookup"><span data-stu-id="4cb0c-188">For Windows 2000 and later systems:</span></span>



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="4cb0c-189">control.exe pastas</span><span class="sxs-lookup"><span data-stu-id="4cb0c-189">control.exe folders</span></span>        | <span data-ttu-id="4cb0c-190">Inicia a janela de **Opções de pasta** .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-190">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="4cb0c-191">control.exe NetWare</span><span class="sxs-lookup"><span data-stu-id="4cb0c-191">control.exe netware</span></span>        | <span data-ttu-id="4cb0c-192">Inicia a janela do **Novell NetWare** (se instalado).</span><span class="sxs-lookup"><span data-stu-id="4cb0c-192">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="4cb0c-193">control.exe telefonia</span><span class="sxs-lookup"><span data-stu-id="4cb0c-193">control.exe telephony</span></span>      | <span data-ttu-id="4cb0c-194">Inicia a janela **Opções de telefone e modem** .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-194">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="4cb0c-195">control.exe AdminTools</span><span class="sxs-lookup"><span data-stu-id="4cb0c-195">control.exe admintools</span></span>     | <span data-ttu-id="4cb0c-196">Exibe a pasta **Ferramentas administrativas** .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-196">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="4cb0c-197">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="4cb0c-197">control.exe schedtasks</span></span>     | <span data-ttu-id="4cb0c-198">Exibe a pasta **tarefas agendadas** .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-198">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="4cb0c-199">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="4cb0c-199">control.exe netconnections</span></span> | <span data-ttu-id="4cb0c-200">Exibe a pasta **conexões de rede** .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-200">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="4cb0c-201">control.exe infravermelho</span><span class="sxs-lookup"><span data-stu-id="4cb0c-201">control.exe infrared</span></span>       | <span data-ttu-id="4cb0c-202">Inicia a janela do **Monitor de infravermelho** (se instalado).</span><span class="sxs-lookup"><span data-stu-id="4cb0c-202">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="4cb0c-203">Senhas de Usercontrol.exe</span><span class="sxs-lookup"><span data-stu-id="4cb0c-203">control.exe userpasswords</span></span>  | <span data-ttu-id="4cb0c-204">Inicia a janela **contas de usuário** .</span><span class="sxs-lookup"><span data-stu-id="4cb0c-204">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="4cb0c-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4cb0c-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cb0c-206">Itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="4cb0c-206">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="4cb0c-207">Diretrizes da Experiência do Usuário</span><span class="sxs-lookup"><span data-stu-id="4cb0c-207">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="4cb0c-208">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="4cb0c-208">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="4cb0c-209">Usando CPLApplet</span><span class="sxs-lookup"><span data-stu-id="4cb0c-209">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="4cb0c-210">Processamento de mensagens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="4cb0c-210">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="4cb0c-211">Estendendo itens do painel de controle do sistema</span><span class="sxs-lookup"><span data-stu-id="4cb0c-211">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="4cb0c-212">Atribuindo categorias do painel de controle</span><span class="sxs-lookup"><span data-stu-id="4cb0c-212">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="4cb0c-213">Criando links de tarefas pesquisáveis para um item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="4cb0c-213">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="4cb0c-214">Acessando o painel de controle no modo de segurança no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cb0c-214">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
