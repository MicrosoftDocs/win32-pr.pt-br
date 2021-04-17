---
description: Wilogutl.exe ajuda na análise de arquivos de log de uma instalação do Windows Installer e exibe soluções sugeridas para erros encontrados em um arquivo de log.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760824"
---
# <a name="wilogutlexe"></a><span data-ttu-id="f9df3-103">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="f9df3-103">Wilogutl.exe</span></span>

<span data-ttu-id="f9df3-104">Wilogutl.exe ajuda na análise de arquivos de log de uma instalação do Windows Installer e exibe soluções sugeridas para erros encontrados em um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="f9df3-104">Wilogutl.exe assists the analysis of log files from a Windows Installer installation, and it displays suggested solutions to errors that are found in a log file.</span></span>

<span data-ttu-id="f9df3-105">Os erros não críticos não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="f9df3-105">Non-critical errors are not displayed.</span></span> <span data-ttu-id="f9df3-106">Wilogutl.exe pode ser executado no modo silencioso ou com uma interface do usuário (IU).</span><span class="sxs-lookup"><span data-stu-id="f9df3-106">Wilogutl.exe can be run in quiet mode or with a user interface (UI).</span></span> <span data-ttu-id="f9df3-107">A ferramenta gera relatórios como arquivos de texto na interface do usuário e nos modos silenciosos.</span><span class="sxs-lookup"><span data-stu-id="f9df3-107">The tool generates reports as text files in both the UI and quiet modes.</span></span> <span data-ttu-id="f9df3-108">Ele funciona melhor com arquivos de log Windows Installer detalhados, mas também funciona com logs não detalhados.</span><span class="sxs-lookup"><span data-stu-id="f9df3-108">It works best with verbose Windows Installer log files, but also works with non-verbose logs.</span></span> <span data-ttu-id="f9df3-109">Para obter mais informações, consulte [Logging](logging.md).</span><span class="sxs-lookup"><span data-stu-id="f9df3-109">For more information, see [Logging](logging.md).</span></span>

<span data-ttu-id="f9df3-110">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f9df3-110">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9df3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9df3-111">Syntax</span></span>

<span data-ttu-id="f9df3-112">\**wilogutl.exe\*\*\*\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span><span class="sxs-lookup"><span data-stu-id="f9df3-112">**wilogutl.exe** *\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span></span>

<span data-ttu-id="f9df3-113">Você pode usar as linhas de comando a seguir para executar no modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="f9df3-113">You can use the following command lines to run in quiet mode.</span></span>

<span data-ttu-id="f9df3-114">**Wilogutl/q/l** *c: \\ mymsilog. log* **/o** *c \\ OutputDir \\*</span><span class="sxs-lookup"><span data-stu-id="f9df3-114">**wilogutl /q /l** *c:\\mymsilog.log* **/o** *c\\outputdir\\*</span></span>

<span data-ttu-id="f9df3-115">**Wilogutl/q/l** *c: \\ mymsilog. log*</span><span class="sxs-lookup"><span data-stu-id="f9df3-115">**wilogutl /q /l** *c:\\mymsilog.log*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="f9df3-116">Opções de Linha de Comando</span><span class="sxs-lookup"><span data-stu-id="f9df3-116">Command-Line Options</span></span>

<span data-ttu-id="f9df3-117">Wilogutl.exe usa as seguintes opções de linha de comando sem diferenciação de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9df3-117">Wilogutl.exe uses the following case insensitive command-line options.</span></span> <span data-ttu-id="f9df3-118">Um delimitador de traço pode ser usado no lugar de uma barra.</span><span class="sxs-lookup"><span data-stu-id="f9df3-118">A dash delimiter can be used in place of a slash.</span></span>



| <span data-ttu-id="f9df3-119">Opção</span><span class="sxs-lookup"><span data-stu-id="f9df3-119">Option</span></span> | <span data-ttu-id="f9df3-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9df3-120">Description</span></span>                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9df3-121">nenhum</span><span class="sxs-lookup"><span data-stu-id="f9df3-121">none</span></span>   | <span data-ttu-id="f9df3-122">É executado no modo de interface do usuário — sem opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f9df3-122">Runs in UI mode—without command-line options.</span></span>                                                                                                                                                   |
| <span data-ttu-id="f9df3-123">/q</span><span class="sxs-lookup"><span data-stu-id="f9df3-123">/q</span></span>     | <span data-ttu-id="f9df3-124">Especifica o modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="f9df3-124">Specifies the quiet mode.</span></span> <span data-ttu-id="f9df3-125">Wilogutl.exe gera arquivos de relatório e não exibe uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9df3-125">Wilogutl.exe generates report files and does not display a user interface.</span></span>                                                                                            |
| <span data-ttu-id="f9df3-126">/l</span><span class="sxs-lookup"><span data-stu-id="f9df3-126">/l</span></span>     | <span data-ttu-id="f9df3-127">Especifica o nome do arquivo de log a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="f9df3-127">Specifies the name of the log file to be analyzed.</span></span> <span data-ttu-id="f9df3-128">Essa opção é necessária ao usar o modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="f9df3-128">This option is required when using the quiet mode.</span></span>                                                                                           |
| <span data-ttu-id="f9df3-129">/o</span><span class="sxs-lookup"><span data-stu-id="f9df3-129">/o</span></span>     | <span data-ttu-id="f9df3-130">Especifica o diretório de saída para arquivos de relatório.</span><span class="sxs-lookup"><span data-stu-id="f9df3-130">Specifies the output directory for report files.</span></span> <span data-ttu-id="f9df3-131">Esse caminho de saída é usado somente quando executado no modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="f9df3-131">This output path is used only when running in quiet mode.</span></span> <span data-ttu-id="f9df3-132">Se a opção não estiver presente, os relatórios serão colocados no diretório C: \\ WiLogResults.</span><span class="sxs-lookup"><span data-stu-id="f9df3-132">If the option is not present, the reports are put in the C:\\WiLogResults directory.</span></span> |



 

<span data-ttu-id="f9df3-133">Quando executado no modo de interface do usuário, Wilogutl.exe exibe as caixas de diálogo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9df3-133">When run in UI mode, Wilogutl.exe displays the following dialog boxes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9df3-134">Nome</span><span class="sxs-lookup"><span data-stu-id="f9df3-134">Name</span></span></th>
<th><span data-ttu-id="f9df3-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9df3-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9df3-136">Windows Installer detalhado do log Analyzer</span><span class="sxs-lookup"><span data-stu-id="f9df3-136">Windows Installer Verbose Log Analyzer</span></span></td>
<td><span data-ttu-id="f9df3-137">A Windows Installer caixa de diálogo analisador de log detalhado permite que os usuários selecionem um arquivo de log para análise:</span><span class="sxs-lookup"><span data-stu-id="f9df3-137">The Windows Installer Verbose Log Analyzer dialog box enables users to select a log file for analysis:</span></span>
<ul>
<li><span data-ttu-id="f9df3-138">O botão <strong>abrir</strong> abre o arquivo no bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="f9df3-138">The <strong>Open</strong> button opens the file in Notepad.</span></span> <span data-ttu-id="f9df3-139">A área de visualização pode ser usada para verificar se o arquivo de log correto foi selecionado.</span><span class="sxs-lookup"><span data-stu-id="f9df3-139">The preview area can be used to verify that the correct log file has been selected.</span></span></li>
<li><span data-ttu-id="f9df3-140">O botão <strong>analisar</strong> começa a análise do arquivo de log e exibe a caixa de diálogo exibição detalhada do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="f9df3-140">The <strong>Analyze</strong> button begins log file analysis and displays the Detailed Log File View dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9df3-141">Exibição detalhada do arquivo de log</span><span class="sxs-lookup"><span data-stu-id="f9df3-141">Detailed Log File View</span></span></td>
<td><span data-ttu-id="f9df3-142">A caixa de diálogo exibição do arquivo de log detalhado exibe informações de erro registradas.</span><span class="sxs-lookup"><span data-stu-id="f9df3-142">The Detailed Log File View dialog box displays logged error information.</span></span> <span data-ttu-id="f9df3-143">Use os botões <strong>voltar</strong> e <strong>Avançar</strong> para navegar por vários erros.</span><span class="sxs-lookup"><span data-stu-id="f9df3-143">Use the <strong>Back</strong> and <strong>Next</strong> buttons to navigate through multiple errors.</span></span> <span data-ttu-id="f9df3-144">Para exibir erros não críticos, marque a caixa de seleção <strong>mostrar erros de depuração ignorados</strong> .</span><span class="sxs-lookup"><span data-stu-id="f9df3-144">To display non-critical errors select the <strong>Show Ignored Debug Errors</strong> check box.</span></span> <span data-ttu-id="f9df3-145">A versão do instalador no computador usado para executar a instalação registrada é exibida.</span><span class="sxs-lookup"><span data-stu-id="f9df3-145">The installer version on the computer used to run the logged installation is displayed.</span></span> <span data-ttu-id="f9df3-146">Se a instalação registrada tiver sido executada com permissões elevadas, a caixa de seleção <strong>instalação elevada</strong> será marcada e as informações serão fornecidas nas caixas de texto <strong>detalhes do privilégio do lado do cliente</strong> e detalhes de <strong>privilégio do lado do servidor</strong> .</span><span class="sxs-lookup"><span data-stu-id="f9df3-146">If the logged installation was run with elevated permissions, the <strong>Elevated install</strong> check box is selected and information is provided in the <strong>Client Side Privilege Details</strong> and <strong>Server Side Privilege Details</strong> text boxes.</span></span> <span data-ttu-id="f9df3-147">A caixa de diálogo exibição detalhada do arquivo de log contém os seguintes botões:</span><span class="sxs-lookup"><span data-stu-id="f9df3-147">The Detailed Log File View dialog box contains the following buttons:</span></span><br/>
<ul>
<li><span data-ttu-id="f9df3-148"><strong>Estados</strong> - do Mostrar a caixa de diálogo de recursos e Estados de componentes.</span><span class="sxs-lookup"><span data-stu-id="f9df3-148"><strong>States</strong> - Show the Feature and Component States dialog box.</span></span></li>
<li><span data-ttu-id="f9df3-149"><strong>Propriedades</strong> - do Mostrar a caixa de diálogo Propriedades.</span><span class="sxs-lookup"><span data-stu-id="f9df3-149"><strong>Properties</strong> - Show the Properties dialog box.</span></span></li>
<li><span data-ttu-id="f9df3-150"><strong>Políticas</strong> - do Mostrar a caixa de diálogo políticas.</span><span class="sxs-lookup"><span data-stu-id="f9df3-150"><strong>Policies</strong> - Show the Policies dialog box.</span></span></li>
<li><span data-ttu-id="f9df3-151">Log anotado em <strong>HTML</strong> - Mostrar log como arquivo HTML anotado.</span><span class="sxs-lookup"><span data-stu-id="f9df3-151"><strong>HTML Annotated Log</strong> - Show log as annotated HTML file.</span></span></li>
<li><span data-ttu-id="f9df3-152"><strong>Salvar resultados</strong> - Salvar arquivos de relatório no diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="f9df3-152"><strong>Save Results</strong> - Save report files to specified directory.</span></span></li>
<li><span data-ttu-id="f9df3-153">Ajuda da mensagem de <strong>erro</strong> - Mostrar ajuda da mensagem de erro do instalador.</span><span class="sxs-lookup"><span data-stu-id="f9df3-153"><strong>Error Message Help</strong> - Show installer error message help.</span></span></li>
<li><span data-ttu-id="f9df3-154"><strong>Ajuda</strong> - do Mostrar ajuda para o Windows Installer setup log Analyzer.</span><span class="sxs-lookup"><span data-stu-id="f9df3-154"><strong>Help</strong> - Show help for Windows Installer Setup Log Analyzer.</span></span></li>
<li><span data-ttu-id="f9df3-155"><strong>Como ler um arquivo</strong> - de log Mostrar o documento de ajuda do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="f9df3-155"><strong>How to Read a Log File</strong> - Show the log file help document.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9df3-156">Estados de recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="f9df3-156">Feature and Component States</span></span></td>
<td><span data-ttu-id="f9df3-157">A caixa de diálogo Estados de recursos <strong>e componentes</strong> exibe os Estados dos recursos e componentes:</span><span class="sxs-lookup"><span data-stu-id="f9df3-157">The <strong>Feature and Component States</strong> dialog box displays the states of features and components:</span></span>
<ul>
<li><span data-ttu-id="f9df3-158">A coluna <strong>recurso</strong> mostra o nome do recurso no pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="f9df3-158">The <strong>Feature</strong> column shows the name for the feature in the installation package.</span></span></li>
<li><span data-ttu-id="f9df3-159">A coluna <strong>componente</strong> mostra o nome do componente no pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="f9df3-159">The <strong>Component</strong> column shows the name of the component in the installation package.</span></span></li>
<li><span data-ttu-id="f9df3-160">A coluna <strong>instalado</strong> mostra o estado do recurso ou componente no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="f9df3-160">The <strong>Installed</strong> column shows the feature or component's state at the end of the installation.</span></span></li>
<li><span data-ttu-id="f9df3-161">A coluna <strong>solicitação</strong> mostra a seleção do usuário durante a instalação para o estado do recurso ou componente.</span><span class="sxs-lookup"><span data-stu-id="f9df3-161">The <strong>Request</strong> column shows the user's selection during the installation for the feature or component's state.</span></span></li>
<li><span data-ttu-id="f9df3-162">A coluna <strong>ação</strong> mostra a ação realizada pelo instalador para o recurso ou componente.</span><span class="sxs-lookup"><span data-stu-id="f9df3-162">The <strong>Action</strong> column shows the action taken by the installer for the feature or component.</span></span></li>
</ul>
<span data-ttu-id="f9df3-163">Para obter mais informações, consulte <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> e <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f9df3-163">For more information, see <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> and <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9df3-164">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f9df3-164">Properties</span></span></td>
<td><span data-ttu-id="f9df3-165">A caixa de diálogo Propriedades mostra Windows Installer <a href="properties.md">Propriedades</a> e seus valores no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="f9df3-165">The Properties dialog box shows Windows Installer <a href="properties.md">Properties</a> and their values at the end of the installation.</span></span> <span data-ttu-id="f9df3-166">Você pode classificar as propriedades por nome ou por valor:</span><span class="sxs-lookup"><span data-stu-id="f9df3-166">You can sort the properties by name or by value:</span></span>
<ul>
<li><span data-ttu-id="f9df3-167">A guia <strong>cliente</strong> mostra Propriedades e valores durante a parte do lado do cliente da instalação.</span><span class="sxs-lookup"><span data-stu-id="f9df3-167">The <strong>Client</strong> tab shows properties and values during the client side portion of the installation.</span></span></li>
<li><span data-ttu-id="f9df3-168">A guia <strong>servidor</strong> mostra Propriedades e valores durante a parte do servidor da instalação.</span><span class="sxs-lookup"><span data-stu-id="f9df3-168">The <strong>Server</strong> tab shows properties and values during the server portion of the installation.</span></span></li>
<li><span data-ttu-id="f9df3-169">A guia <strong>aninhada</strong> mostra as propriedades e os valores de qualquer <a href="concurrent-installations.md">instalação simultânea</a>.</span><span class="sxs-lookup"><span data-stu-id="f9df3-169">The <strong>Nested</strong> tab shows the properties and values of any <a href="concurrent-installations.md">Concurrent Installations</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9df3-170">Políticas</span><span class="sxs-lookup"><span data-stu-id="f9df3-170">Policies</span></span></td>
<td><span data-ttu-id="f9df3-171">A caixa de diálogo políticas exibe o conjunto de <a href="system-policy.md">políticas do sistema</a> após a instalação:</span><span class="sxs-lookup"><span data-stu-id="f9df3-171">The Policies dialog box displays the <a href="system-policy.md">System Policy</a> set after the installation:</span></span>
<ul>
<li><span data-ttu-id="f9df3-172">Um valor de 0 (zero) definido para a política significa que a política não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f9df3-172">A value of 0 (zero) set for the policy means the policy is not enabled.</span></span></li>
<li><span data-ttu-id="f9df3-173">Um valor de 1 (um) significa que a política está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f9df3-173">A value of 1 (one) means the policy is enabled.</span></span></li>
<li><span data-ttu-id="f9df3-174">Um valor de?</span><span class="sxs-lookup"><span data-stu-id="f9df3-174">A value of ?</span></span> <span data-ttu-id="f9df3-175">(ponto de interrogação) significa que o valor da política não é registrado no log.</span><span class="sxs-lookup"><span data-stu-id="f9df3-175">(question mark) means the policy value is not recorded in the log.</span></span></li>
</ul>
<span data-ttu-id="f9df3-176">Se você precisar de um valor de política que não esteja no log, tente usar Regedit.exe para verificar as chaves do registro no computador que está falhando na instalação.</span><span class="sxs-lookup"><span data-stu-id="f9df3-176">If you need a policy value that is not in the log, try using Regedit.exe to check the registry keys on the computer failing the installation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a><span data-ttu-id="f9df3-177">Arquivos de relatório</span><span class="sxs-lookup"><span data-stu-id="f9df3-177">Report Files</span></span>

<span data-ttu-id="f9df3-178">Ao executar uma análise de modo silencioso ou clicar no botão **salvar resultados** na caixa de diálogo **Exibir arquivo de log detalhado** , a ferramenta Windows Installer setup Analyzer gera três arquivos de texto e um arquivo de log anotado em HTML.</span><span class="sxs-lookup"><span data-stu-id="f9df3-178">When performing a quiet mode analysis or clicking the **Save Results** button on the **Detailed Log File View** dialog, the Windows Installer Setup Analyzer tool generates three text files and an HTML annotated log file.</span></span>

<span data-ttu-id="f9df3-179">A tabela a seguir identifica os nomes e o conteúdo nos arquivos de relatório.</span><span class="sxs-lookup"><span data-stu-id="f9df3-179">The following table identifies the names and contents in the report files.</span></span>



| <span data-ttu-id="f9df3-180">Nome</span><span class="sxs-lookup"><span data-stu-id="f9df3-180">Name</span></span>                      | <span data-ttu-id="f9df3-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9df3-181">Description</span></span>                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9df3-182">LogFileName \_summary.txt</span><span class="sxs-lookup"><span data-stu-id="f9df3-182">logfilename\_summary.txt</span></span>  | <span data-ttu-id="f9df3-183">Resume o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="f9df3-183">Summarizes the log file.</span></span> <span data-ttu-id="f9df3-184">Lista as informações exibidas pela caixa de diálogo exibição detalhada do arquivo de log e o primeiro erro.</span><span class="sxs-lookup"><span data-stu-id="f9df3-184">Lists the information displayed by the Detailed Log File View dialog box and the first error.</span></span>         |
| <span data-ttu-id="f9df3-185">LogFileName \_errors.txt</span><span class="sxs-lookup"><span data-stu-id="f9df3-185">logfilename\_errors.txt</span></span>   | <span data-ttu-id="f9df3-186">Identifica o número de erros, os erros e as soluções recomendadas.</span><span class="sxs-lookup"><span data-stu-id="f9df3-186">Identifies the number of errors, the errors, and recommended solutions.</span></span> <span data-ttu-id="f9df3-187">Esse arquivo lista os erros críticos e não críticos.</span><span class="sxs-lookup"><span data-stu-id="f9df3-187">This file lists both critical and non-critical errors.</span></span> |
| <span data-ttu-id="f9df3-188">LogFileName \_policies.txt</span><span class="sxs-lookup"><span data-stu-id="f9df3-188">logfilename\_policies.txt</span></span> | <span data-ttu-id="f9df3-189">Identifica os nomes de política e os valores definidos no final da instalação como na caixa de diálogo políticas.</span><span class="sxs-lookup"><span data-stu-id="f9df3-189">Identifies the policy names and values set at the end of the installation as in the Policies dialog box.</span></span>                       |
| <span data-ttu-id="f9df3-190">detalhes \_logfilename.htm</span><span class="sxs-lookup"><span data-stu-id="f9df3-190">details\_logfilename.htm</span></span>  | <span data-ttu-id="f9df3-191">Um log anotado em HTML com uma legenda para a codificação de cores.</span><span class="sxs-lookup"><span data-stu-id="f9df3-191">An HTML annotated log with a legend for the color coding.</span></span>                                                                      |



 

## <a name="return-values"></a><span data-ttu-id="f9df3-192">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="f9df3-192">Return Values</span></span>

<span data-ttu-id="f9df3-193">Se argumentos de linha de comando inválidos forem passados para operações de modo silencioso, o Wilogutl.exe não fará nada e o processo retornará um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9df3-193">If invalid command-line arguments are passed for quiet mode operations, Wilogutl.exe does nothing, and the process returns one of the values in the following table.</span></span>



| <span data-ttu-id="f9df3-194">Valor</span><span class="sxs-lookup"><span data-stu-id="f9df3-194">Value</span></span> | <span data-ttu-id="f9df3-195">Significado</span><span class="sxs-lookup"><span data-stu-id="f9df3-195">Meaning</span></span>                                                                 |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="f9df3-196">1</span><span class="sxs-lookup"><span data-stu-id="f9df3-196">1</span></span>     | <span data-ttu-id="f9df3-197">Diretório de saída inválidos especificado.</span><span class="sxs-lookup"><span data-stu-id="f9df3-197">Bad output directory is specified.</span></span>                                      |
| <span data-ttu-id="f9df3-198">2</span><span class="sxs-lookup"><span data-stu-id="f9df3-198">2</span></span>     | <span data-ttu-id="f9df3-199">Nome de arquivo de log inadequado especificado.</span><span class="sxs-lookup"><span data-stu-id="f9df3-199">Bad log file name is specified.</span></span>                                         |
| <span data-ttu-id="f9df3-200">3</span><span class="sxs-lookup"><span data-stu-id="f9df3-200">3</span></span>     | <span data-ttu-id="f9df3-201">Passou/q, mas está faltando a opção/l necessária para o nome do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="f9df3-201">Passed /q, but is missing the required switch /l for the log file name.</span></span> |
| <span data-ttu-id="f9df3-202">4</span><span class="sxs-lookup"><span data-stu-id="f9df3-202">4</span></span>     | <span data-ttu-id="f9df3-203">Passou em/l, mas não tem a opção necessária/q para o modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="f9df3-203">Passed /l, but is missing the required switch /q for quiet mode.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f9df3-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9df3-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9df3-205">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="f9df3-205">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> <dt>

[<span data-ttu-id="f9df3-206">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f9df3-206">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> </dl>

 

 




