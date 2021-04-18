---
<span data-ttu-id="f3e92-101">Descrição: o programa executável que interpreta pacotes e instala produtos é Msiexec.exe. Observação: msiexec também define um nível de erro no retorno que corresponde aos códigos de erro do sistema.</span><span class="sxs-lookup"><span data-stu-id="f3e92-101">description: The executable program that interprets packages and installs products is Msiexec.exe.Note  Msiexec also sets an error level on return that corresponds to System Error Codes.</span></span> <span data-ttu-id="f3e92-102">A tabela a seguir identifica as opções de linha de comando padrão para este programa.</span><span class="sxs-lookup"><span data-stu-id="f3e92-102">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="f3e92-103">As opções de linha de comando não diferenciam maiúsculas de minúsculas. Windows Installer 2,0: as opções de linha de comando que são identificadas neste tópico estão disponíveis a partir do Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="f3e92-103">Command-line options are case insensitive.Windows Installer 2.0:  The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="f3e92-104">As opções de Command-Line Windows Installer estão disponíveis com Windows Installer&\# 160; 3.0 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f3e92-104">The Windows Installer Command-Line Options are available with Windows Installer&\#160;3.0 and earlier versions.</span></span>
<span data-ttu-id="f3e92-105">MS. AssetID: b1707c88-1cca-45ab-bb23-6002bfd5204e título: opções do instalador padrão Command-Line MS. tópico: artigo MS. Date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="f3e92-105">ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="standard-installer-command-line-options"></a><span data-ttu-id="f3e92-106">Opções de Command-Line do instalador padrão</span><span class="sxs-lookup"><span data-stu-id="f3e92-106">Standard Installer Command-Line Options</span></span>

<span data-ttu-id="f3e92-107">O programa executável que interpreta pacotes e instala produtos é Msiexec.exe.</span><span class="sxs-lookup"><span data-stu-id="f3e92-107">The executable program that interprets packages and installs products is Msiexec.exe.</span></span>

> [!Note]  
> <span data-ttu-id="f3e92-108">Msiexec também define um nível de erro no retorno que corresponde aos [códigos de erro do sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f3e92-108">Msiexec also sets an error level on return that corresponds to [System Error Codes](../debug/system-error-codes.md).</span></span>

 

<span data-ttu-id="f3e92-109">A tabela a seguir identifica as opções de linha de comando padrão para este programa.</span><span class="sxs-lookup"><span data-stu-id="f3e92-109">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="f3e92-110">As opções de linha de comando não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f3e92-110">Command-line options are case insensitive.</span></span>

<span data-ttu-id="f3e92-111">**Windows Installer 2,0:** As opções de linha de comando que são identificadas neste tópico estão disponíveis a partir do Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="f3e92-111">**Windows Installer 2.0:** The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="f3e92-112">As [Opções de linha de comando](command-line-options.md) Windows Installer estão disponíveis com o Windows Installer 3,0 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f3e92-112">The Windows Installer [Command-Line Options](command-line-options.md) are available with Windows Installer 3.0 and earlier versions.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3e92-113">Opção</span><span class="sxs-lookup"><span data-stu-id="f3e92-113">Option</span></span></th>
<th><span data-ttu-id="f3e92-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3e92-114">Parameters</span></span></th>
<th><span data-ttu-id="f3e92-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f3e92-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3e92-116"><strong>/Help</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-116"><strong>/help</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="f3e92-117">Opção de ajuda e referência rápida.</span><span class="sxs-lookup"><span data-stu-id="f3e92-117">Help and quick reference option.</span></span> <span data-ttu-id="f3e92-118">Exibe o uso correto do comando de instalação, incluindo uma lista de todos os comutadores e comportamentos.</span><span class="sxs-lookup"><span data-stu-id="f3e92-118">Displays the correct usage of the setup command including a list of all switches and behavior.</span></span> <span data-ttu-id="f3e92-119">A descrição do uso pode ser exibida na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3e92-119">The description of usage can be displayed in the user interface.</span></span> <span data-ttu-id="f3e92-120">O uso incorreto de qualquer opção invoca essa opção de ajuda.</span><span class="sxs-lookup"><span data-stu-id="f3e92-120">Incorrect use of any option invokes this help option.</span></span><br/> <span data-ttu-id="f3e92-121">Exemplo: <strong>msiexec/Help</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-121">Example: <strong>msiexec /help</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-122">A opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/?</strong>.</span><span class="sxs-lookup"><span data-stu-id="f3e92-122">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/?</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3e92-123"><strong>/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-123"><strong>/quiet</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="f3e92-124">Opção de exibição silenciosa.</span><span class="sxs-lookup"><span data-stu-id="f3e92-124">Quiet display option.</span></span> <span data-ttu-id="f3e92-125">O instalador executa uma instalação sem exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3e92-125">The installer runs an installation without displaying a user interface.</span></span> <span data-ttu-id="f3e92-126">Nenhum prompt, mensagem ou caixa de diálogo é exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f3e92-126">No prompts, messages, or dialog boxes are displayed to the user.</span></span> <span data-ttu-id="f3e92-127">O usuário não pode cancelar a instalação.</span><span class="sxs-lookup"><span data-stu-id="f3e92-127">The user cannot cancel the installation.</span></span> <span data-ttu-id="f3e92-128">Use as opções de linha de comando <strong>/norestart</strong> ou <strong>/forcerestart</strong> padrão para controlar as reinicializações.</span><span class="sxs-lookup"><span data-stu-id="f3e92-128">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="f3e92-129">Se nenhuma opção de reinicialização for especificada, o instalador reiniciará o computador sempre que necessário, sem exibir nenhum prompt ou aviso para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f3e92-129">If no reboot options are specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span><br/> <span data-ttu-id="f3e92-130">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="f3e92-130">Examples:</span></span> <br/> <span data-ttu-id="f3e92-131"><strong>msiexec/pacote Application.msi/Quiet</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-131"><strong>msiexec /package Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="f3e92-132"><strong>Msiexec/Uninstall Application.msi/Quiet</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-132"><strong>Msiexec /uninstall Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="f3e92-133"><strong>Msiexec/Update msipatch. msp/Quiet</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-133"><strong>Msiexec /update msipatch.msp /quiet</strong></span></span><br/> <span data-ttu-id="f3e92-134"><strong>Msiexec/Uninstall msipatch. msp/pacote Application.msi/Quiet</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-134"><strong>Msiexec /uninstall msipatch.msp /package Application.msi / quiet</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-135">A opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/qn</strong>.</span><span class="sxs-lookup"><span data-stu-id="f3e92-135">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qn</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3e92-136"><strong>/Passive</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-136"><strong>/passive</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="f3e92-137">Opção de exibição passiva.</span><span class="sxs-lookup"><span data-stu-id="f3e92-137">Passive display option.</span></span> <span data-ttu-id="f3e92-138">O instalador exibe uma barra de progresso para o usuário que indica que uma instalação está em andamento, mas nenhum prompt ou mensagem de erro é exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f3e92-138">The installer displays a progress bar to the user that indicates that an installation is in progress but no prompts or error messages are displayed to the user.</span></span> <span data-ttu-id="f3e92-139">O usuário não pode cancelar a instalação.</span><span class="sxs-lookup"><span data-stu-id="f3e92-139">The user cannot cancel the installation.</span></span> <span data-ttu-id="f3e92-140">Use as opções de linha de comando <strong>/norestart</strong> ou <strong>/forcerestart</strong> padrão para controlar as reinicializações.</span><span class="sxs-lookup"><span data-stu-id="f3e92-140">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="f3e92-141">Se nenhuma opção de reinicialização for especificada, o instalador reiniciará o computador sempre que necessário, sem exibir nenhum prompt ou aviso para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f3e92-141">If no reboot option is specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span> <br/> <span data-ttu-id="f3e92-142">Exemplo: <strong>msiexec/pacote Application.msi/Passive</strong> </span><span class="sxs-lookup"><span data-stu-id="f3e92-142">Example: <strong>msiexec /package Application.msi /passive</strong> </span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-143">A opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/QB!-</strong> com <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S definida na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f3e92-143">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3e92-144"><strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-144"><strong>/norestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="f3e92-145">Nunca reinicie a opção.</span><span class="sxs-lookup"><span data-stu-id="f3e92-145">Never restart option.</span></span> <span data-ttu-id="f3e92-146">O instalador nunca reinicia o computador após a instalação.</span><span class="sxs-lookup"><span data-stu-id="f3e92-146">The installer never restarts the computer after the installation.</span></span><br/> <span data-ttu-id="f3e92-147">Exemplo: msiexec/pacote Application.msi <strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-147">Example: msiexec /package Application.msi <strong>/norestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-148">O equivalente Windows Installer linha de comando foi <a href="reboot.md"><strong>reboot</strong></a>= ReallySuppress definido na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f3e92-148">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3e92-149"><strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-149"><strong>/forcerestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="f3e92-150">Sempre reinicie a opção.</span><span class="sxs-lookup"><span data-stu-id="f3e92-150">Always restart option.</span></span> <span data-ttu-id="f3e92-151">O instalador sempre reinicia o computador após cada instalação.</span><span class="sxs-lookup"><span data-stu-id="f3e92-151">The installer always restarts the computer after every installation.</span></span><br/> <span data-ttu-id="f3e92-152">Exemplo: msiexec/pacote Application.msi <strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-152">Example: msiexec /package Application.msi <strong>/forcerestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-153">O equivalente Windows Installer linha de comando foi <a href="reboot.md"><strong>reboot</strong></a>= Force Set na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f3e92-153">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=Force set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3e92-154"><strong>/promptrestart</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-154"><strong>/promptrestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="f3e92-155">Avisar antes da opção de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="f3e92-155">Prompt before restarting option.</span></span> <span data-ttu-id="f3e92-156">Exibe uma mensagem informando que uma reinicialização é necessária para concluir a instalação e solicita ao usuário se o sistema deve ser reiniciado agora.</span><span class="sxs-lookup"><span data-stu-id="f3e92-156">Displays a message that a restart is required to complete the installation and asks the user whether to restart the system now.</span></span> <span data-ttu-id="f3e92-157">Essa opção não pode ser usada junto com a opção <strong>/Quiet</strong> .</span><span class="sxs-lookup"><span data-stu-id="f3e92-157">This option cannot be used together with the <strong>/quiet</strong> option.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-158">O equivalente Windows Installer linha de comando tem <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; definido na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f3e92-158">The equivalent Windows Installer command line has <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a> = &quot;&quot; set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3e92-159"><strong>/Uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-159"><strong>/uninstall</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="f3e92-160">Opção desinstalar produto.</span><span class="sxs-lookup"><span data-stu-id="f3e92-160">Uninstall product option.</span></span> <span data-ttu-id="f3e92-161">Desinstala um produto.</span><span class="sxs-lookup"><span data-stu-id="f3e92-161">Uninstalls a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-162">A opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/x</strong>.</span><span class="sxs-lookup"><span data-stu-id="f3e92-162">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/x</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3e92-163"><strong>/Uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-163"><strong>/uninstall</strong></span></span></td>
<td><span data-ttu-id="f3e92-164"><em>/pacote <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. msp | PatchGUID2]</em></span><span class="sxs-lookup"><span data-stu-id="f3e92-164"><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1>[;Update2.msp | PatchGUID2]</em></span></span></td>
<td><span data-ttu-id="f3e92-165">Desinstale a opção de atualização.</span><span class="sxs-lookup"><span data-stu-id="f3e92-165">Uninstall update option.</span></span> <span data-ttu-id="f3e92-166">Desinstala um patch de atualização.</span><span class="sxs-lookup"><span data-stu-id="f3e92-166">Uninstalls an update patch.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-167">A opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/i</strong> com <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= atualização1. msp | PatchGUID1[; Update2. msp | PatchGUID2] definido na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f3e92-167">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2] set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3e92-168"><strong>/log</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-168"><strong>/log</strong></span></span></td>
<td><em><logfile></em></td>
<td><span data-ttu-id="f3e92-169">Opção de log.</span><span class="sxs-lookup"><span data-stu-id="f3e92-169">Log option.</span></span> <span data-ttu-id="f3e92-170">Grava informações de log em um arquivo de log no caminho existente especificado.</span><span class="sxs-lookup"><span data-stu-id="f3e92-170">Writes logging information into a log file at the specified existing path.</span></span> <span data-ttu-id="f3e92-171">O caminho para o local do arquivo de log já deve existir.</span><span class="sxs-lookup"><span data-stu-id="f3e92-171">The path to the log file location must already exist.</span></span> <span data-ttu-id="f3e92-172">O instalador não cria a estrutura de diretório para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="f3e92-172">The installer does not create the directory structure for the logfile.</span></span><br/> <span data-ttu-id="f3e92-173">As informações a seguir são inseridas no log:</span><span class="sxs-lookup"><span data-stu-id="f3e92-173">The following information is entered into the log:</span></span><br/>
<ul>
<li><span data-ttu-id="f3e92-174">Mensagens de status</span><span class="sxs-lookup"><span data-stu-id="f3e92-174">Status messages</span></span></li>
<li><span data-ttu-id="f3e92-175">Avisos não fatais</span><span class="sxs-lookup"><span data-stu-id="f3e92-175">Nonfatal warnings</span></span></li>
<li><span data-ttu-id="f3e92-176">Todas as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="f3e92-176">All error messages</span></span></li>
<li><span data-ttu-id="f3e92-177">Inicialização de ações</span><span class="sxs-lookup"><span data-stu-id="f3e92-177">Start up of actions</span></span></li>
<li><span data-ttu-id="f3e92-178">Registros específicos da ação</span><span class="sxs-lookup"><span data-stu-id="f3e92-178">Action-specific records</span></span></li>
<li><span data-ttu-id="f3e92-179">Solicitações do usuário</span><span class="sxs-lookup"><span data-stu-id="f3e92-179">User requests</span></span></li>
<li><span data-ttu-id="f3e92-180">Parâmetros iniciais da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="f3e92-180">Initial UI parameters</span></span></li>
<li><span data-ttu-id="f3e92-181">Informações de saída fatal ou de memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="f3e92-181">Out-of-memory or fatal exit information</span></span></li>
<li><span data-ttu-id="f3e92-182">Mensagens de espaço em disco insuficiente</span><span class="sxs-lookup"><span data-stu-id="f3e92-182">Out-of-disk-space messages</span></span></li>
<li><span data-ttu-id="f3e92-183">Propriedades do terminal</span><span class="sxs-lookup"><span data-stu-id="f3e92-183">Terminal properties</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-184">A opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/l \*</strong>.</span><span class="sxs-lookup"><span data-stu-id="f3e92-184">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/L\*</strong>.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-185">Para obter mais informações sobre todos os métodos que estão disponíveis para definir o modo de log, consulte <a href="normal-logging.md">log normal</a> na seção <a href="windows-installer-logging.md">log de Windows Installer</a> .</span><span class="sxs-lookup"><span data-stu-id="f3e92-185">For more information about all the methods that are available for setting the logging mode, see <a href="normal-logging.md">Normal Logging</a> in the <a href="windows-installer-logging.md">Windows Installer Logging</a> section.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3e92-186"><strong>/pacote</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-186"><strong>/package</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="f3e92-187">Instalar opção de produto.</span><span class="sxs-lookup"><span data-stu-id="f3e92-187">Install product option.</span></span> <span data-ttu-id="f3e92-188">Instala ou configura um produto.</span><span class="sxs-lookup"><span data-stu-id="f3e92-188">Installs or configures a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-189">A opção de <a href="command-line-options.md">linha de comando</a> equivalente Windows Installer é <strong>/i</strong>.</span><span class="sxs-lookup"><span data-stu-id="f3e92-189">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3e92-190"><strong>/Update</strong></span><span class="sxs-lookup"><span data-stu-id="f3e92-190"><strong>/update</strong></span></span></td>
<td><span data-ttu-id="f3e92-191"><em><Update1.msp>[; Update2. msp]</em></span><span class="sxs-lookup"><span data-stu-id="f3e92-191"><em><Update1.msp>[;Update2.msp]</em></span></span></td>
<td><span data-ttu-id="f3e92-192">Opção instalar patches.</span><span class="sxs-lookup"><span data-stu-id="f3e92-192">Install patches option.</span></span> <span data-ttu-id="f3e92-193">Instala um ou vários patches.</span><span class="sxs-lookup"><span data-stu-id="f3e92-193">Installs one or multiple patches.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3e92-194">O equivalente Windows Installer linha de comando tem <a href="patch.md"><strong>patch</strong></a> = [msipatch. msp] <; PatchGuid2> definido na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f3e92-194">The equivalent Windows Installer command line has <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<;PatchGuid2> set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
