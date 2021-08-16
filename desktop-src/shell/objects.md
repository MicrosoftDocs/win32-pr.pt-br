---
description: esta seção descreve os objetos de Windows implementados pelo Shell.
title: Objetos do Shell para scripts e Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bd2c924d9b66194c8f016fc8b1c16bed8a7e3c62f82e3673837e0e31c8563fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858795"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Objetos do Shell para scripts e Microsoft Visual Basic

esta seção descreve os objetos de Windows implementados pelo Shell.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br/></td>
<td>Permite que um cliente gerencie as configurações de cota de disco global de um volume NTFS. esse objeto torna a funcionalidade essencial da interface <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> disponível para scripts e aplicativos baseados no Microsoft Visual Basic.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br/></td>
<td>Permite que um administrador gerencie as propriedades de cota de disco de um volume. O sistema de arquivos NTFS permite que um administrador gerencie o uso do disco em um volume compartilhado alocando uma quantidade especificada de espaço em disco ou <em>limite de cota</em>para cada usuário. Você pode usar esse objeto para definir o limite de cota padrão que será atribuído automaticamente a todos os novos usuários.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br/></td>
<td>Recebe eventos de registro da janela <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Pasta</strong></a><br/></td>
<td>Representa uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a pasta.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Pasta2</strong></a><br/></td>
<td>Estende o objeto <a href="folder.md"><strong>Folder</strong></a> para dar suporte a pastas offline.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>FolderItem</strong></a><br/></td>
<td>Representa um item em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o item.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>FolderItems</strong></a><br/></td>
<td>Representa a coleção de itens em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Estende o objeto <a href="folderitems.md"><strong>FolderItems</strong></a> . Ele dá suporte a um método adicional.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Estende o objeto <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> . Este objeto dá suporte a um método e uma propriedade adicionais.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br/></td>
<td>Representa um único verbo disponível para um item. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o verbo.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br/></td>
<td>Representa a coleção de verbos de um item em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br/></td>
<td>Representa um objeto no Shell. Os métodos são fornecidos para controlar o Shell e executar comandos no Shell. Também há métodos para obter outros objetos relacionados ao shell. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Estende o objeto <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> com uma variedade de novas funcionalidades. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Estende o objeto <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> . O <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> dá suporte a um novo método além das propriedades e métodos com suporte do <strong>IShellDispatch2</strong>. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Estende o objeto <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> . Além das propriedades e métodos com suporte do <strong>IShellDispatch3</strong>, o <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> dá suporte a quatro métodos adicionais. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Estende o objeto <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> . Além das propriedades e métodos com suporte do <strong>IShellDispatch4</strong>, o <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adiciona um método que exibe janelas abertas em uma pilha 3D. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Estende o objeto <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> . Além das propriedades e métodos com suporte do <strong>IShellDispatch5</strong>, o <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adiciona um método que exibe o painel de pesquisa de aplicativos. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Estende o objeto <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> e dá suporte a uma propriedade adicional.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>NewWDEvents</strong></a><br/></td>
<td>Estende o objeto <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> habilitando páginas do lado do servidor hospedadas em um assistente para verificar se o usuário foi autenticado por meio de um conta Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Representa os objetos no Shell. Os métodos são fornecidos para controlar o Shell e executar comandos no Shell. Também há métodos para obter outros objetos relacionados ao shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br/></td>
<td>Estende o objeto <a href="folderitem.md"><strong>FolderItem</strong></a> . Além das propriedades e métodos com suporte do <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> tem dois métodos adicionais.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br/></td>
<td>Representa os objetos em uma exibição e fornece propriedades e métodos usados para obter informações sobre o conteúdo da exibição.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br/></td>
<td>Encaminha os eventos acionados por um objeto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> especificado para manipuladores de eventos <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> correspondentes.<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br/></td>
<td>Gerencia links do Shell. Esse objeto torna grande parte da funcionalidade da interface <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> disponível para scripts de aplicativos. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br/></td>
<td>implementado pelo Shell para ajudar o script e os desenvolvedores de Visual Basic a usar alguns dos recursos disponíveis no Shell. O objeto <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> não tem nenhuma propriedade ou evento. Os métodos são fornecidos para adicionar itens ao shell.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>ShellWindows</strong></a><br/></td>
<td>Representa uma coleção das janelas abertas que pertencem ao shell. Os métodos associados a esses objetos podem controlar e executar comandos no Shell e obter outros objetos relacionados ao shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br/></td>
<td>Expõe métodos que habilitam páginas HTML que são hospedadas em uma extensão de assistente para se comunicar com o assistente.<br/></td>
</tr>
</tbody>
</table>



 

 

 




