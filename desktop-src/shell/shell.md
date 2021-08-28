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
ms.openlocfilehash: d31adcbf5a12d699750029c15a308ef73f4d8c03
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467223"
---
# <a name="shell-object"></a>Objeto shell

Representa os objetos no Shell. Métodos são fornecidos para controlar o Shell e para executar comandos dentro do Shell. Também há métodos para obter outros objetos relacionados ao Shell.

## <a name="members"></a>Membros

O **objeto Shell** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto** Shell tem esses métodos.




| Método | Descrição | 
|--------|-------------|
| <a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a> | Adiciona um arquivo à lista de MRU (usados mais recentemente).<br /> | 
| <a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Cria uma caixa de diálogo que permite que o usuário selecione uma pasta e, em seguida, retorne o objeto <a href="folder.md"><strong>Pasta da</strong></a> pasta selecionada.<br /> | 
| <a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a> | Determina se o usuário atual pode iniciar e parar o serviço nomeado.<br /> | 
| <a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a> | Em cascata todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Cascata Windows</strong>.<br /> | 
| <a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Executa o aplicativo Painel de Controle (*.cpl) especificado. Se o aplicativo já estiver aberto, ele ativará a instância em execução. <br /><blockquote><p>[!Note]<br />A partir Windows Vista, a maioria Painel de Controle aplicativos são itens do Shell e não podem ser abertos com essa função. Para abrir esses Painel de Controle aplicativos, passe o nome canônico para control.exe. Por exemplo:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="shell-ejectpc.md"><strong>EjetoPC</strong></a> | Ejeta o computador de sua estação de encaixe. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>ejetar PC</strong>se o computador dá suporte a esse comando.<br /> | 
| <a href="shell-explore.md"><strong>Explorar</strong></a> | Abre uma pasta especificada em uma janela Windows Explorer.<br /> | 
| <a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a> | Obtém o valor de uma política Internet Explorer especificada.<br /> | 
| <a href="shell-filerun.md"><strong>FileRun</strong></a> | Exibe a <strong>caixa de diálogo</strong> Executar para o usuário. Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Executar</strong>.<br /> | 
| <a href="shell-findcomputer.md"><strong>FindComputer</strong></a> | Exibe a caixa <strong>de diálogo Resultados da Pesquisa:</strong> Computadores. A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.<br /> | 
| <a href="shell-findfiles.md"><strong>FindFiles</strong></a> | Exibe a caixa <strong>de diálogo Encontrar: Todos os</strong> Arquivos. Isso é o mesmo que clicar no <strong>menu</strong> Iniciar e selecionar <strong>Pesquisar</strong> (ou seu equivalente em sistemas anteriores Windows XP.<br /> | 
| <a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a> | Exibe a caixa <strong>de diálogo</strong> Encontrar Impressora.<br /> | 
| <a href="/windows/desktop/shell/shell-getsetting"><strong>Getsetting</strong></a> | Recupera uma configuração de Shell global.<br /> | 
| <a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a> | Recupera informações do sistema.<br /> | 
| <a href="shell-help.md"><strong>Ajuda</strong></a> | Exibe o Windows Centro de Ajuda e Suporte. Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Ajuda e Suporte.</strong><br /> | 
| <a href="/windows/desktop/shell/shell-isrestricted"><strong>Isrestricted</strong></a> | Recupera a configuração de restrição de um grupo do Registro.<br /> | 
| <a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a> | Retorna um valor que indica se um serviço específico está em execução.<br /> | 
| <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> | Minimiza todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na <strong></strong> barra de tarefas e selecionar Minimizar Todos <strong>os Windows</strong> em sistemas mais antigos ou clicar no ícone Mostrar Área de Trabalho na área Início Rápido da barra de tarefas no Windows 2000 ou Windows XP.<br /> | 
| <a href="shell-namespace.md"><strong>Namespace</strong></a> | Cria e retorna um <a href="folder.md"><strong>objeto Folder</strong></a> para a pasta especificada.<br /> | 
| <a href="shell-open.md"><strong>Aberto</strong></a> | Abre a pasta especificada.<br /> | 
| <a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a> | Atualiza o conteúdo <strong>do</strong> menu Iniciar. Usado somente com sistemas anteriores Windows XP.<br /> | 
| <a href="shell-searchcommand.md"><strong>SearchCommand</strong></a> | Exibe o painel Pesquisa de Aplicativos.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a> | Inicia um serviço nomeado.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a> | Interrompe um serviço nomeado.<br /> | 
| <a href="shell-settime.md"><strong>Settime</strong></a> | Exibe a caixa <strong>de diálogo Propriedades de Data</strong> e Hora. Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar <strong>Ajustar Data/Hora.</strong><br /> | 
| <a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a> | Executa uma operação especificada em um arquivo especificado.<br /> | 
| <a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a> | Exibe uma barra do navegador.<br /> | 
| <a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | Exibe a caixa <strong>de Desligar Windows</strong> de diálogo. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Desligar</strong>.<br /> | 
| <a href="shell-suspend.md"><strong>Suspend</strong></a> | Td | 
| <a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Lado a lado todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Windows Horizontalmente.</strong><br /> | 
| <a href="shell-tilevertically.md"><strong>TileVertically</strong></a> | Lado a lado todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Lado Windows Verticalmente.</strong><br /> | 
| <a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a> | Exibe ou oculta a área de trabalho.<br /> | 
| <a href="shell-trayproperties.md"><strong>TrayProperties</strong></a> | Exibe a caixa <strong>de diálogo Propriedades da Barra de Tarefas e Iniciar Menu.</strong> Esse método tem o mesmo efeito de clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Propriedades</strong>.<br /> | 
| <a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Restaura todas as janelas da área de trabalho para o mesmo estado em que estavam antes do último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de <strong></strong> tarefas e selecionar Desfazer Minimizar Todos <strong>os Windows</strong> em sistemas mais antigos ou um segundo clique no ícone Mostrar Área de Trabalho na área Início Rápido da barra de tarefas no Windows 2000 ou Windows XP.<br /> | 
| <a href="shell-windows.md"><strong>Windows</strong></a> | Cria e retorna um <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a> Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao Shell.<br /> | 
| <a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a> | Exibe a caixa <strong>de Segurança do Windows</strong> de diálogo.<br /> | 
| <a href="shell-windowswitcher.md"><strong>WindowScher</strong></a> | Exibe as janelas abertas em uma pilha 3D que você pode inverter.<br /> | 




 

### <a name="properties"></a>Propriedades

O **objeto Shell** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Descrição                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Aplicativo**](shell-application.md)<br/> | Somente leitura<br/> | Contém o objeto Application do objeto .<br/>                        |
| [**Pai**](shell-parent.md)<br/>           | Somente leitura<br/> | Obtém um objeto que representa o pai do objeto atual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da área \[ de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 
