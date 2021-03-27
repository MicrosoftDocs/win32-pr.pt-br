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
# <a name="shell-object"></a>Objeto Shell

Representa os objetos no Shell. Os métodos são fornecidos para controlar o Shell e executar comandos no Shell. Também há métodos para obter outros objetos relacionados ao shell.

## <a name="members"></a>Membros

O objeto **shell** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **shell** tem esses métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></td>
<td style="text-align: left;">Adiciona um arquivo à lista MRU (usada mais recentemente).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de <a href="folder.md"><strong>pasta</strong></a> da pasta selecionada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">Determina se o usuário atual pode iniciar e parar o serviço nomeado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Propaga todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas em cascata</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Executa o aplicativo do painel de controle (*. cpl) especificado. Se o aplicativo já estiver aberto, ele ativará a instância em execução. <br/>
<blockquote>
<p>[!Note]<br />
A partir do Windows Vista, a maioria dos aplicativos do painel de controle são itens do Shell e não pode ser aberta com essa função. Para abrir esses aplicativos do painel de controle, passe o nome canônico para control.exe. Por exemplo:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Ejeta o computador de sua estação de encaixe. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Ejetar PC</strong>se o seu computador oferecer suporte a esse comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Explorar</strong></a></td>
<td style="text-align: left;">Abre uma pasta especificada em uma janela do Windows Explorer.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">Obtém o valor de uma política especificada do Internet Explorer.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>executar</strong> para o usuário. Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>executar</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>resultados da pesquisa: computadores</strong> . A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>localizar: todos os arquivos</strong> . Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Pesquisar</strong> (ou seu equivalente em sistemas anteriores ao Windows XP).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>Localizar impressora</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetDefinition</strong></a></td>
<td style="text-align: left;">Recupera uma configuração de shell global.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></td>
<td style="text-align: left;">Recupera informações do sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Ajuda</strong></a></td>
<td style="text-align: left;">Exibe o centro de ajuda e suporte do Windows. Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>ajuda e suporte</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></td>
<td style="text-align: left;">Recupera a configuração de restrição de um grupo do registro.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></td>
<td style="text-align: left;">Retorna um valor que indica se um serviço específico está em execução.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Minimiza todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>minimizar todas as janelas</strong> em sistemas mais antigos ou clicar no ícone <strong>Mostrar área de trabalho</strong> na área início rápido da barra de tarefas no Windows 2000 ou no Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>NameSpace</strong></a></td>
<td style="text-align: left;">Cria e retorna um objeto de <a href="folder.md"><strong>pasta</strong></a> para a pasta especificada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Abrir</strong></a></td>
<td style="text-align: left;">Abre a pasta especificada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Atualiza o conteúdo do menu <strong>Iniciar</strong> . Usado apenas com sistemas anteriores ao Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">Exibe o painel de pesquisa de aplicativos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>Iniciar</strong></a></td>
<td style="text-align: left;">Inicia um serviço nomeado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>Parar</strong></a></td>
<td style="text-align: left;">Interrompe um serviço nomeado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>Propriedades de data e hora</strong> . Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar <strong>Ajustar data/hora</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">Executa uma operação especificada em um arquivo especificado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></td>
<td style="text-align: left;">Exibe uma barra de navegador.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>desligar o Windows</strong> . Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>desligar</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Suspend</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Organiza todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas de bloco horizontalmente</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Organiza todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas de peças verticalmente</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Exibe ou oculta a área de trabalho.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>Bandejaproperties</strong></a></td>
<td style="text-align: left;">Exibe a <strong>barra de tarefas e a caixa de diálogo Propriedades do menu iniciar</strong> . Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Propriedades</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Restaura todas as janelas da área de trabalho para o mesmo estado em que estavam antes do último comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> . Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>desfazer minimizar todas as janelas</strong> em sistemas mais antigos ou um segundo clique no ícone <strong>Mostrar área de trabalho</strong> na área início rápido da barra de tarefas no Windows 2000 ou no Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Cria e retorna um objeto <a href="shellwindows.md"><strong>ShellWindows</strong></a> . Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao shell.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>segurança do Windows</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></td>
<td style="text-align: left;">Exibe as janelas abertas em uma pilha 3D que você pode percorrer.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propriedades

O objeto **shell** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Description                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Aplicativo**](shell-application.md)<br/> | Somente leitura<br/> | Contém o objeto de aplicativo do objeto.<br/>                        |
| [**Pai**](shell-parent.md)<br/>           | Somente leitura<br/> | Obtém um objeto que representa o pai do objeto atual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 
