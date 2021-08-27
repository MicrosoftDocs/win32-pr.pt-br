---
description: Esta seção descreve os objetos Windows implementados pelo Shell.
title: Objetos shell para scripts e microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e4d367b836516259a4c0f73cea9da20e7e13326
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465023"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Objetos shell para scripts e microsoft Visual Basic

Esta seção descreve os objetos Windows implementados pelo Shell.

## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br /> | Permite que um cliente gerencie as configurações de cota de disco global de um volume NTFS. Esse objeto disponibiliza a funcionalidade essencial da interface <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> para scripts e aplicativos baseados Visual Basic Microsoft.<br /> | 
| <a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br /> | Permite que um administrador gerencie as propriedades de cota de disco de um volume. O sistema de arquivos NTFS permite que um administrador gerencie o uso de disco em um volume compartilhado alocando uma quantidade especificada de espaço em disco ou limite de cota <em>para</em>cada usuário. Você pode usar esse objeto para definir o limite de cota padrão que será atribuído automaticamente a todos os novos usuários.<br /> | 
| <a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br /> | Recebe eventos <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>de registro de janela do IShellWindows.</strong></a> <br /> | 
| <a href="folder.md"><strong>Pasta</strong></a><br /> | Representa uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a pasta.<br /> | 
| <a href="folder2-object.md"><strong>Pasta2</strong></a><br /> | Estende o objeto <a href="folder.md"><strong>Pasta</strong></a> para dar suporte a pastas offline.<br /> | 
| <a href="folderitem.md"><strong>FolderItem</strong></a><br /> | Representa um item em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre o item.<br /> | 
| <a href="folderitems.md"><strong>FolderItems</strong></a><br /> | Representa a coleção de itens em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a coleção.<br /> | 
| <a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br /> | Estende o <a href="folderitems.md"><strong>objeto FolderItems.</strong></a> Ele dá suporte a um método adicional.<br /> | 
| <a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br /> | Estende o <a href="folderitems2-object.md"><strong>objeto FolderItems2.</strong></a> Esse objeto dá suporte a um método e propriedade adicionais.<br /> | 
| <a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br /> | Representa um único verbo disponível para um item. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre o verbo.<br /> | 
| <a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br /> | Representa a coleção de verbos para um item em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a coleção.<br /> | 
| <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br /> | Representa um objeto no Shell. Métodos são fornecidos para controlar o Shell e para executar comandos dentro do Shell. Também há métodos para obter outros objetos relacionados ao Shell. <br /><blockquote>[!Note]<br /><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> é implementado e acessado por meio do <a href="shell.md"><strong>objeto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br /> | Estende o <a href="ishelldispatch.md"><strong>objeto IShellDispatch</strong></a> com uma variedade de novas funcionalidades. <br /><blockquote>[!Note]<br /><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> é implementado e acessado por meio do <a href="shell.md"><strong>objeto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br /> | Estende o <a href="ishelldispatch2-object.md"><strong>objeto IShellDispatch2.</strong></a> <a href="ishelldispatch3.md"><strong>IShellDispatch3 dá</strong></a> suporte a um novo método, além das propriedades e métodos compatíveis com <strong>IShellDispatch2</strong>. <br /><blockquote>[!Note]<br /><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> é implementado e acessado por meio do <a href="shell.md"><strong>objeto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br /> | Estende o <a href="ishelldispatch3.md"><strong>objeto IShellDispatch3.</strong></a> Além das propriedades e métodos compatíveis com <strong>IShellDispatch3,</strong> <a href="ishelldispatch4.md"><strong>O IShellDispatch4</strong></a> dá suporte a quatro métodos adicionais. <br /><blockquote>[!Note]<br /><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> é implementado e acessado por meio do <a href="shell.md"><strong>objeto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br /> | Estende o <a href="ishelldispatch4.md"><strong>objeto IShellDispatch4.</strong></a> Além das propriedades e métodos com suporte de <strong>IShellDispatch4,</strong> <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adiciona um método que exibe janelas abertas em uma pilha 3D. <br /><blockquote>[!Note]<br /><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> é implementado e acessado por meio do <a href="shell.md"><strong>objeto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br /> | Estende o <a href="ishelldispatch5.md"><strong>objeto IShellDispatch5.</strong></a> Além das propriedades e métodos com suporte de <strong>IShellDispatch5,</strong> <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adiciona um método que exibe o painel Pesquisa de Aplicativos. <br /><blockquote>[!Note]<br /><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> é implementado e acessado por meio do <a href="shell.md"><strong>objeto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br /> | Estende o objeto <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> e dá suporte a uma propriedade adicional.<br /> | 
| <a href="newwdevents.md"><strong>NewWDEvents</strong></a><br /> | Estende o <a href="webwizardhost.md"><strong>objeto WebWizardHost</strong></a> habilitando páginas do lado do servidor hospedadas em um assistente para verificar se o usuário foi autenticado por meio de um conta Microsoft.<br /> | 
| <a href="shell.md"><strong>Shell</strong></a><br /> | Representa os objetos no Shell. Métodos são fornecidos para controlar o Shell e para executar comandos dentro do Shell. Também há métodos para obter outros objetos relacionados ao Shell.<br /> | 
| <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br /> | Estende o <a href="folderitem.md"><strong>objeto FolderItem.</strong></a> Além das propriedades e métodos com suporte de <strong>FolderItem,</strong> <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> tem dois métodos adicionais.<br /> | 
| <a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br /> | Representa os objetos em uma exibição e fornece propriedades e métodos usados para obter informações sobre o conteúdo da exibição.<br /> | 
| <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br /> | Encaminha os eventos disparados por um objeto <a href="shellfolderview.md"><strong>ShellFolderView especificado</strong></a> para manipuladores <a href="shellfolderviewoc-object.md"><strong>de eventos ShellFolderViewOC</strong></a> correspondentes.<br /> | 
| <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br /> | Gerencia links do Shell. Esse objeto disponibiliza grande parte da funcionalidade da interface <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> para aplicativos de script. <br /> | 
| <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br /> | Implementado pelo Shell para ajudar os desenvolvedores Visual Basic script e usar alguns dos recursos disponíveis no Shell. O <a href="shelluihelper.md"><strong>objeto ShellUIHelper</strong></a> não tem nenhuma propriedade ou eventos. Métodos são fornecidos para adicionar itens ao Shell.<br /> | 
| <a href="shellwindows.md"><strong>ShellWindows</strong></a><br /> | Representa uma coleção das janelas abertas que pertencem ao Shell. Os métodos associados a esses objetos podem controlar e executar comandos dentro do Shell e obter outros objetos relacionados ao Shell.<br /> | 
| <a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br /> | Expõe métodos que habilitam páginas HTML hospedadas em uma extensão de assistente para se comunicar com o assistente.<br /> | 




 

 

 




