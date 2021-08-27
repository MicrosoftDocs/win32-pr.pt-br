---
description: Representa um objeto no Shell.
title: Objeto IShellDispatch (Shldisp.h)
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
ms.openlocfilehash: 322b912ad7332b0862309b0ecc1510adb3aa1a10
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475292"
---
# <a name="ishelldispatch-object"></a>Objeto IShellDispatch

Representa um objeto no Shell. Métodos são fornecidos para controlar o Shell e para executar comandos dentro do Shell. Também há métodos para obter outros objetos relacionados ao Shell.

> [!Note]  
> **IShellDispatch** é implementado e acessado por meio do [**objeto Shell.**](shell.md)

 

## <a name="members"></a>Membros

O **objeto IShellDispatch** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto IShellDispatch** tem esses métodos.




| Método | Descrição | 
|--------|-------------|
| <a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Cria uma caixa de diálogo que permite que o usuário selecione uma pasta e, em seguida, retorne o objeto <a href="folder.md"><strong>Pasta da</strong></a> pasta selecionada.<br /> | 
| <a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a> | Em cascata todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Janelas em cascata</strong>.<br /> | 
| <a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Executa o aplicativo Painel de Controle especificado. Se o aplicativo já estiver aberto, ele ativará a instância em execução. <br /><blockquote><p>[!Note]<br />A partir Windows Vista, a maioria Painel de Controle aplicativos são itens do Shell e não podem ser abertos com essa função. Para abrir esses Painel de Controle aplicativos, passe o nome canônico para control.exe. Por exemplo:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="ishelldispatch-ejectpc.md"><strong>EjetoPC</strong></a> | Ejeta o computador de sua estação de encaixe. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>ejetar PC</strong>se o computador dá suporte a esse comando.<br /> | 
| <a href="ishelldispatch-explore.md"><strong>Explorar</strong></a> | Abre uma pasta especificada em uma janela Windows Explorer.<br /> | 
| <a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a> | Exibe a <strong>caixa de diálogo</strong> Executar para o usuário.<br /> | 
| <a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a> | Exibe a caixa <strong>de diálogo Resultados da Pesquisa:</strong> Computadores. A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.<br /> | 
| <a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a> | Exibe a caixa <strong>de diálogo Encontrar: Todos os</strong> Arquivos. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e, em seguida, selecionar <strong>Pesquisar</strong>.<br /> | 
| <a href="ishelldispatch-help.md"><strong>Ajuda</strong></a> | Exibe a janela Windows Ajuda e Suporte. Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Ajuda e Suporte.</strong><br /> | 
| <a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a> | Minimiza todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse <strong></strong> na barra de tarefas e selecionar Minimizar Todos <strong>os</strong> Windows sistemas mais antigos ou clicar no ícone Mostrar Área de Trabalho na barra de tarefas.<br /> | 
| <a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a> | Cria e retorna um <a href="folder.md"><strong>objeto Folder</strong></a> para a pasta especificada.<br /> | 
| <a href="ishelldispatch-open.md"><strong>Aberto</strong></a> | Abre a pasta especificada.<br /> | 
| <a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a> | Atualiza o conteúdo <strong>do</strong> menu Iniciar. Usado somente com sistemas anteriores Windows XP.<br /> | 
| <a href="ishelldispatch-settime.md"><strong>Settime</strong></a> | Exibe a caixa <strong>de diálogo Data</strong> e Hora. Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar <strong>Ajustar data/hora.</strong><br /> | 
| <a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | Exibe a caixa <strong>de Desligar Windows</strong> de diálogo. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Desligar</strong>.<br /> | 
| <a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a> | Td | 
| <a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Lado a lado todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Mostrar janelas empilhadas.</strong><br /> | 
| <a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a> | Lado a lado todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Mostrar janelas lado a lado.</strong><br /> | 
| <a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a> | Exibe a caixa <strong>de diálogo Propriedades da Barra de Tarefas e Iniciar Menu.</strong> Esse método tem o mesmo efeito de clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Propriedades</strong>.<br /> | 
| <a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Restaura todas as janelas da área de trabalho para o estado em que estavam antes do último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de <strong></strong> tarefas e selecionar <strong>Desfazer Windows</strong> Minimizar Tudo (em sistemas mais antigos) ou um segundo clique no ícone Mostrar Área de Trabalho na barra de tarefas.<br /> | 
| <a href="ishelldispatch-windows.md"><strong>Windows</strong></a> | Cria e retorna um <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a> Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao Shell.<br /> | 




 

### <a name="properties"></a>Propriedades

O **objeto IShellDispatch** tem essas propriedades.



| Propriedade                                                     | Tipo de acesso          | Descrição                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Aplicativo**](ishelldispatch-application.md)<br/> | Somente leitura<br/> | Contém um objeto que representa um aplicativo.<br/>                    |
| [**Pai**](ishelldispatch-parent.md)<br/>           | Somente leitura<br/> | Recupera um objeto que representa o pai do objeto atual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto Shell**](shell.md)
</dt> </dl>

 

 
