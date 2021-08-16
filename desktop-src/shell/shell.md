---
description: Representa os objetos no Shell. Métodos são fornecidos para controlar o Shell e para executar comandos dentro do Shell. Também há métodos para obter outros objetos relacionados ao Shell.
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
ms.openlocfilehash: fe2fbaa1bad61ac9c22d36919e49cf493a26a778a8e97d69d1b200c0c62205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857715"
---
# <a name="shell-object"></a>Objeto shell

Representa os objetos no Shell. Métodos são fornecidos para controlar o Shell e para executar comandos dentro do Shell. Também há métodos para obter outros objetos relacionados ao Shell.

## <a name="members"></a>Membros

O **objeto Shell** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto** Shell tem esses métodos.



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
<td style="text-align: left;">Adiciona um arquivo à lista de MRU (usados mais recentemente).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Cria uma caixa de diálogo que permite que o usuário selecione uma pasta e, em seguida, retorne o objeto <a href="folder.md"><strong>Pasta da</strong></a> pasta selecionada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">Determina se o usuário atual pode iniciar e parar o serviço nomeado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Em cascata todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Cascata Windows</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Executa o aplicativo Painel de Controle (*.cpl) especificado. Se o aplicativo já estiver aberto, ele ativará a instância em execução. <br/>
<blockquote>
<p>[!Note]<br />
A partir Windows Vista, a maioria Painel de Controle aplicativos são itens do Shell e não podem ser abertos com essa função. Para abrir esses Painel de Controle aplicativos, passe o nome canônico para control.exe. Por exemplo:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>EjetoPC</strong></a></td>
<td style="text-align: left;">Ejeta o computador de sua estação de encaixe. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>ejetar PC</strong>se o computador dá suporte a esse comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Explorar</strong></a></td>
<td style="text-align: left;">Abre uma pasta especificada em uma janela Windows Explorer.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">Obtém o valor de uma política Internet Explorer especificada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Exibe a <strong>caixa de diálogo</strong> Executar para o usuário. Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Executar</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>de diálogo Resultados da Pesquisa:</strong> Computadores. A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>de diálogo Encontrar: Todos os</strong> Arquivos. Isso é o mesmo que clicar no <strong>menu</strong> Iniciar e, em seguida, selecionar <strong>Pesquisar</strong> (ou seu equivalente em sistemas anteriores Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>de diálogo</strong> Encontrar Impressora.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>Getsetting</strong></a></td>
<td style="text-align: left;">Recupera uma configuração de Shell global.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></td>
<td style="text-align: left;">Recupera informações do sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Ajuda</strong></a></td>
<td style="text-align: left;">Exibe o Windows Centro de Ajuda e Suporte. Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Ajuda e Suporte.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>Isrestricted</strong></a></td>
<td style="text-align: left;">Recupera a configuração de restrição de um grupo do Registro.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></td>
<td style="text-align: left;">Retorna um valor que indica se um serviço específico está em execução.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Minimiza todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse <strong></strong> na barra de tarefas e selecionar Minimizar Todos <strong>os Windows</strong> em sistemas mais antigos ou clicar no ícone Mostrar Área de Trabalho na área Início Rápido da barra de tarefas no Windows 2000 ou Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>Namespace</strong></a></td>
<td style="text-align: left;">Cria e retorna um <a href="folder.md"><strong>objeto Folder</strong></a> para a pasta especificada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Aberto</strong></a></td>
<td style="text-align: left;">Abre a pasta especificada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Atualiza o conteúdo <strong>do</strong> menu Iniciar. Usado somente com sistemas anteriores Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">Exibe o painel Pesquisa de Aplicativos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></td>
<td style="text-align: left;">Inicia um serviço nomeado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></td>
<td style="text-align: left;">Interrompe um serviço nomeado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>Settime</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>de diálogo Propriedades de Data</strong> e Hora. Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar <strong>Ajustar Data/Hora.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">Executa uma operação especificada em um arquivo especificado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></td>
<td style="text-align: left;">Exibe uma barra do navegador.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>Desligar Windows</strong> caixa de diálogo. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Desligar</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Suspend</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Lado a lado todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Windows Horizontalmente.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Lado a lado todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Windows Verticalmente.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Exibe ou oculta a área de trabalho.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>de diálogo Propriedades da Barra de Tarefas e Iniciar Menu.</strong> Esse método tem o mesmo efeito de clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Propriedades</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Restaura todas as janelas da área de trabalho para o mesmo estado em que estavam antes do último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra <strong></strong> de tarefas e selecionar Desfazer Minimizar Tudo <strong>Windows em</strong> sistemas mais antigos ou um segundo clique no ícone Mostrar Área de Trabalho na área Início Rápido da barra de tarefas no Windows 2000 ou Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Cria e retorna um <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a> Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao Shell.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>Segurança do Windows</strong> caixa de diálogo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>WindowScher</strong></a></td>
<td style="text-align: left;">Exibe as janelas abertas em uma pilha 3D que você pode inverter.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propriedades

O **objeto Shell** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Descrição                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Aplicativo**](shell-application.md)<br/> | Somente leitura<br/> | Contém o objeto Application do objeto .<br/>                        |
| [**Pai**](shell-parent.md)<br/>           | Somente leitura<br/> | Obtém um objeto que representa o pai do objeto atual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 
