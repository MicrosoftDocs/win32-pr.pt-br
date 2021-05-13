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
# <a name="ishelldispatch-object"></a>Objeto IShellDispatch

Representa um objeto no Shell. Os métodos são fornecidos para controlar o Shell e executar comandos no Shell. Também há métodos para obter outros objetos relacionados ao shell.

> [!Note]  
> **IShellDispatch** é implementado e acessado por meio do objeto [**shell**](shell.md) .

 

## <a name="members"></a>Membros

O objeto **IShellDispatch** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **IShellDispatch** tem esses métodos.



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
<td style="text-align: left;"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de <a href="folder.md"><strong>pasta</strong></a> da pasta selecionada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Propaga todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>janelas em cascata</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Executa o aplicativo do painel de controle especificado. Se o aplicativo já estiver aberto, ele ativará a instância em execução. <br/>
<blockquote>
<p>[!Note]<br />
A partir do Windows Vista, a maioria dos aplicativos do painel de controle são itens do Shell e não pode ser aberta com essa função. Para abrir esses aplicativos do painel de controle, passe o nome canônico para control.exe. Por exemplo:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Ejeta o computador de sua estação de encaixe. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>ejetar PC</strong>se o computador dá suporte a esse comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-explore.md"><strong>Explorar</strong></a></td>
<td style="text-align: left;">Abre uma pasta especificada em uma Windows Explorer de dados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Exibe a <strong>caixa de diálogo</strong> Executar para o usuário.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>de diálogo Resultados da Pesquisa:</strong> Computadores. A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Exibe a caixa <strong>de diálogo Encontrar: Todos os</strong> Arquivos. Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e, em seguida, selecionar <strong>Pesquisar</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-help.md"><strong>Ajuda</strong></a></td>
<td style="text-align: left;">Exibe a janela Ajuda e Suporte do Windows. Esse método tem o mesmo efeito que clicar no menu <strong>Iniciar</strong> e selecionar <strong>Ajuda e Suporte.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Minimiza todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do <strong></strong> mouse na barra de tarefas e selecionar Minimizar Todas as <strong>Janelas</strong> em sistemas mais antigos ou clicar no ícone Mostrar Área de Trabalho na barra de tarefas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a></td>
<td style="text-align: left;">Cria e retorna um <a href="folder.md"><strong>objeto Folder</strong></a> para a pasta especificada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-open.md"><strong>Aberto</strong></a></td>
<td style="text-align: left;">Abre a pasta especificada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Atualiza o conteúdo do menu <strong>Iniciar</strong> . Usado apenas com sistemas anteriores ao Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>data e hora</strong> . Esse método tem o mesmo efeito que clicar com o botão direito do mouse no relógio na área de status da barra de tarefas e selecionar <strong>Ajustar data/hora</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Exibe a caixa de diálogo <strong>desligar o Windows</strong> . Isso é o mesmo que clicar no menu <strong>Iniciar</strong> e selecionar <strong>desligar</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Organiza todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Mostrar janelas empilhadas</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Organiza todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Mostrar janelas lado a lado</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-trayproperties.md"><strong>Bandejaproperties</strong></a></td>
<td style="text-align: left;">Exibe a <strong>barra de tarefas e a caixa de diálogo Propriedades do menu iniciar</strong> . Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar <strong>Propriedades</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Restaura todas as janelas da área de trabalho para o estado em que estavam antes do último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra <strong></strong> de tarefas e selecionar Desfazer Minimizar Todas as <strong>Janelas</strong> (em sistemas mais antigos) ou um segundo clique do ícone Mostrar Área de Trabalho na barra de tarefas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Cria e retorna um <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a> Esse objeto representa uma coleção de todas as janelas abertas que pertencem ao Shell.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propriedades

O **objeto IShellDispatch** tem essas propriedades.



| Propriedade                                                     | Tipo de acesso          | Descrição                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Aplicativo**](ishelldispatch-application.md)<br/> | Somente leitura<br/> | Contém um objeto que representa um aplicativo.<br/>                    |
| [**Pai**](ishelldispatch-parent.md)<br/>           | Somente leitura<br/> | Recupera um objeto que representa o pai do objeto atual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto Shell**](shell.md)
</dt> </dl>

 

 
