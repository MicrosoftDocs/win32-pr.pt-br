---
description: Esta seção descreve os objetos do Windows implementados pelo shell.
title: Objetos do Shell para scripts e Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505984"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a><span data-ttu-id="83909-103">Objetos do Shell para scripts e Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="83909-103">Shell Objects for Scripting and Microsoft Visual Basic</span></span>

<span data-ttu-id="83909-104">Esta seção descreve os objetos do Windows implementados pelo shell.</span><span class="sxs-lookup"><span data-stu-id="83909-104">This section describes the Windows objects implemented by the Shell.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="83909-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="83909-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="83909-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="83909-106">Topic</span></span></th>
<th><span data-ttu-id="83909-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="83909-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="83909-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-109">Permite que um cliente gerencie as configurações de cota de disco global de um volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="83909-109">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="83909-110">Esse objeto torna a funcionalidade essencial da interface <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> disponível para scripts e aplicativos baseados no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="83909-110">This object makes the essential functionality of the <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> interface available to scripting and Microsoft Visual Basic-based applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-112">Permite que um administrador gerencie as propriedades de cota de disco de um volume.</span><span class="sxs-lookup"><span data-stu-id="83909-112">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="83909-113">O sistema de arquivos NTFS permite que um administrador gerencie o uso do disco em um volume compartilhado alocando uma quantidade especificada de espaço em disco ou <em>limite de cota</em>para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="83909-113">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or <em>quota limit</em>, to each user.</span></span> <span data-ttu-id="83909-114">Você pode usar esse objeto para definir o limite de cota padrão que será atribuído automaticamente a todos os novos usuários.</span><span class="sxs-lookup"><span data-stu-id="83909-114">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-116">Recebe eventos de registro da janela <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-116">Receives <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> window registration events.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-117"><a href="folder.md"><strong>Pasta</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-117"><a href="folder.md"><strong>Folder</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-118">Representa uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-118">Represents a Shell folder.</span></span> <span data-ttu-id="83909-119">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="83909-119">This object contains properties and methods that allow you to retrieve information about the folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-120"><a href="folder2-object.md"><strong>Pasta2</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-121">Estende o objeto <a href="folder.md"><strong>Folder</strong></a> para dar suporte a pastas offline.</span><span class="sxs-lookup"><span data-stu-id="83909-121">Extends the <a href="folder.md"><strong>Folder</strong></a> object to support offline folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-123">Representa um item em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-123">Represents an item in a Shell folder.</span></span> <span data-ttu-id="83909-124">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="83909-124">This object contains properties and methods that allow you to retrieve information about the item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-126">Representa a coleção de itens em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-126">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="83909-127">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.</span><span class="sxs-lookup"><span data-stu-id="83909-127">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-129">Estende o objeto <a href="folderitems.md"><strong>FolderItems</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-129">Extends the <a href="folderitems.md"><strong>FolderItems</strong></a> object.</span></span> <span data-ttu-id="83909-130">Ele dá suporte a um método adicional.</span><span class="sxs-lookup"><span data-stu-id="83909-130">It supports one additional method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-132">Estende o objeto <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-132">Extends the <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> object.</span></span> <span data-ttu-id="83909-133">Este objeto dá suporte a um método e uma propriedade adicionais.</span><span class="sxs-lookup"><span data-stu-id="83909-133">This object supports an additional method and property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-135">Representa um único verbo disponível para um item.</span><span class="sxs-lookup"><span data-stu-id="83909-135">Represents a single verb available to an item.</span></span> <span data-ttu-id="83909-136">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o verbo.</span><span class="sxs-lookup"><span data-stu-id="83909-136">This object contains properties and methods that allow you to retrieve information about the verb.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-138">Representa a coleção de verbos de um item em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-138">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="83909-139">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.</span><span class="sxs-lookup"><span data-stu-id="83909-139">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-141">Representa um objeto no Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-141">Represents an object in the Shell.</span></span> <span data-ttu-id="83909-142">Os métodos são fornecidos para controlar o Shell e executar comandos no Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-142">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="83909-143">Também há métodos para obter outros objetos relacionados ao shell.</span><span class="sxs-lookup"><span data-stu-id="83909-143">There are also methods to obtain other Shell-related objects.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="83909-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-146">Estende o objeto <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> com uma variedade de novas funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="83909-146">Extends the <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> object with a variety of new functionality.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="83909-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-149">Estende o objeto <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-149">Extends the <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> object.</span></span> <span data-ttu-id="83909-150">O <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> dá suporte a um novo método além das propriedades e métodos com suporte do <strong>IShellDispatch2</strong>.</span><span class="sxs-lookup"><span data-stu-id="83909-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supports one new method in addition to the properties and methods supported by <strong>IShellDispatch2</strong>.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="83909-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-153">Estende o objeto <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-153">Extends the <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> object.</span></span> <span data-ttu-id="83909-154">Além das propriedades e métodos com suporte do <strong>IShellDispatch3</strong>, o <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> dá suporte a quatro métodos adicionais.</span><span class="sxs-lookup"><span data-stu-id="83909-154">In addition to the properties and methods supported by <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supports four additional methods.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="83909-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-157">Estende o objeto <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-157">Extends the <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> object.</span></span> <span data-ttu-id="83909-158">Além das propriedades e métodos com suporte do <strong>IShellDispatch4</strong>, o <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adiciona um método que exibe janelas abertas em uma pilha 3D.</span><span class="sxs-lookup"><span data-stu-id="83909-158">In addition to the properties and methods supported by <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adds a method that displays open windows in a 3D stack.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="83909-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-161">Estende o objeto <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-161">Extends the <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> object.</span></span> <span data-ttu-id="83909-162">Além das propriedades e métodos com suporte do <strong>IShellDispatch5</strong>, o <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adiciona um método que exibe o painel de pesquisa de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="83909-162">In addition to the properties and methods supported by <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adds a method that displays the Apps Search pane.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="83909-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> é implementado e acessado por meio do objeto <a href="shell.md"><strong>shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-165">Estende o objeto <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> e dá suporte a uma propriedade adicional.</span><span class="sxs-lookup"><span data-stu-id="83909-165">Extends the <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> object and supports one additional property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-167">Estende o objeto <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> habilitando páginas do lado do servidor hospedadas em um assistente para verificar se o usuário foi autenticado por meio de um conta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83909-167">Extends the <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-168"><a href="shell.md"><strong>Shell</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-168"><a href="shell.md"><strong>Shell</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-169">Representa os objetos no Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-169">Represents the objects in the Shell.</span></span> <span data-ttu-id="83909-170">Os métodos são fornecidos para controlar o Shell e executar comandos no Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-170">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="83909-171">Também há métodos para obter outros objetos relacionados ao shell.</span><span class="sxs-lookup"><span data-stu-id="83909-171">There are also methods to obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-173">Estende o objeto <a href="folderitem.md"><strong>FolderItem</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="83909-173">Extends the <a href="folderitem.md"><strong>FolderItem</strong></a> object.</span></span> <span data-ttu-id="83909-174">Além das propriedades e métodos com suporte do <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> tem dois métodos adicionais.</span><span class="sxs-lookup"><span data-stu-id="83909-174">In addition to the properties and methods supported by <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> has two additional methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-176">Representa os objetos em uma exibição e fornece propriedades e métodos usados para obter informações sobre o conteúdo da exibição.</span><span class="sxs-lookup"><span data-stu-id="83909-176">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-178">Encaminha os eventos acionados por um objeto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> especificado para manipuladores de eventos <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> correspondentes.</span><span class="sxs-lookup"><span data-stu-id="83909-178">Forwards the events fired by a specified <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> object to corresponding <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> event handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-180">Gerencia links do Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-180">Manages Shell links.</span></span> <span data-ttu-id="83909-181">Esse objeto torna grande parte da funcionalidade da interface <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> disponível para scripts de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="83909-181">This object makes much of the functionality of the <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> interface available to scripting applications.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-183">Implementado pelo shell para ajudar o script e os desenvolvedores de Visual Basic a usar alguns dos recursos disponíveis no Shell.</span><span class="sxs-lookup"><span data-stu-id="83909-183">Implemented by the Shell to help script and Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="83909-184">O objeto <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> não tem nenhuma propriedade ou evento.</span><span class="sxs-lookup"><span data-stu-id="83909-184">The <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> object does not have any properties or events.</span></span> <span data-ttu-id="83909-185">Os métodos são fornecidos para adicionar itens ao shell.</span><span class="sxs-lookup"><span data-stu-id="83909-185">Methods are provided to add items to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83909-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-187">Representa uma coleção das janelas abertas que pertencem ao shell.</span><span class="sxs-lookup"><span data-stu-id="83909-187">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="83909-188">Os métodos associados a esses objetos podem controlar e executar comandos no Shell e obter outros objetos relacionados ao shell.</span><span class="sxs-lookup"><span data-stu-id="83909-188">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83909-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span><span class="sxs-lookup"><span data-stu-id="83909-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="83909-190">Expõe métodos que habilitam páginas HTML que são hospedadas em uma extensão de assistente para se comunicar com o assistente.</span><span class="sxs-lookup"><span data-stu-id="83909-190">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




