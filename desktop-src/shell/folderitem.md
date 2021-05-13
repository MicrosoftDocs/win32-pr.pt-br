---
description: Representa um item em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o item.
title: Objeto FolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a8b9309e7bd1c8cbcc05360c076db085d0f8b991
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840977"
---
# <a name="folderitem-object"></a><span data-ttu-id="dd6f2-104">Objeto FolderItem</span><span class="sxs-lookup"><span data-stu-id="dd6f2-104">FolderItem object</span></span>

<span data-ttu-id="dd6f2-105">Representa um item em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="dd6f2-106">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="dd6f2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="dd6f2-107">Members</span></span>

<span data-ttu-id="dd6f2-108">O objeto **FolderItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dd6f2-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="dd6f2-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd6f2-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd6f2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd6f2-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd6f2-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd6f2-111">Methods</span></span>

<span data-ttu-id="dd6f2-112">O objeto **FolderItem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="dd6f2-113">Método</span><span class="sxs-lookup"><span data-stu-id="dd6f2-113">Method</span></span>                                      | <span data-ttu-id="dd6f2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd6f2-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd6f2-115">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="dd6f2-116">Executa um verbo no item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="dd6f2-117">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="dd6f2-118">Recupera o objeto [**FolderItemVerbs**](folderitemverbs.md) do item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="dd6f2-119">Esse objeto é a coleção de verbos que podem ser executados no item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd6f2-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd6f2-120">Properties</span></span>

<span data-ttu-id="dd6f2-121">O objeto **FolderItem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="dd6f2-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dd6f2-122">Property</span></span>                                                   | <span data-ttu-id="dd6f2-123">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="dd6f2-123">Access type</span></span>           | <span data-ttu-id="dd6f2-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd6f2-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd6f2-125">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="dd6f2-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-126">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-127">Contém o objeto de [**aplicativo**](folderitem-application.md) do item de pasta.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="dd6f2-128">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="dd6f2-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-129">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-130">Contém o objeto de [**pasta**](folder.md) do item, se o item for uma pasta.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="dd6f2-131">**GetLink**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="dd6f2-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-132">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-133">Contém o objeto [**ShellLinkObject**](shelllinkobject-object.md) do item, se o item for um atalho.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="dd6f2-134">**Isnavegável**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="dd6f2-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-135">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-136">Indica se o item pode ser hospedado dentro de um navegador ou quadro do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="dd6f2-137">**IsFileSystem**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="dd6f2-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-138">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-139">Indica se o item faz parte do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="dd6f2-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="dd6f2-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-141">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-142">Indica se o item é uma pasta.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="dd6f2-143">**Islink**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="dd6f2-144">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-144">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-145">Indica se o item é um atalho.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="dd6f2-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="dd6f2-147">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dd6f2-147">Read/write</span></span><br/> | <span data-ttu-id="dd6f2-148">Define ou obtém a data e a hora em que um arquivo foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="dd6f2-149">[**ModifyDate**](folderitem-modifydate.md) pode ser usado para recuperar a data e a hora em que uma pasta foi modificada pela última vez, mas não pode defini-la.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="dd6f2-150">**Nome**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="dd6f2-151">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dd6f2-151">Read/write</span></span><br/> | <span data-ttu-id="dd6f2-152">Define ou obtém o nome do item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="dd6f2-153">**Pai**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="dd6f2-154">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-154">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-155">Obtém um objeto que representa o pai do item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="dd6f2-156">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="dd6f2-157">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-157">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-158">Contém o caminho e o nome completos do item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="dd6f2-159">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="dd6f2-160">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-160">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-161">Contém o tamanho do item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="dd6f2-162">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dd6f2-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="dd6f2-163">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd6f2-163">Read-only</span></span><br/>  | <span data-ttu-id="dd6f2-164">Contém uma representação de cadeia de caracteres do tipo do item.</span><span class="sxs-lookup"><span data-stu-id="dd6f2-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="dd6f2-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd6f2-165">Requirements</span></span>



| <span data-ttu-id="dd6f2-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd6f2-166">Requirement</span></span> | <span data-ttu-id="dd6f2-167">Valor</span><span class="sxs-lookup"><span data-stu-id="dd6f2-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6f2-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd6f2-168">Minimum supported client</span></span><br/> | <span data-ttu-id="dd6f2-169">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dd6f2-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dd6f2-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd6f2-170">Minimum supported server</span></span><br/> | <span data-ttu-id="dd6f2-171">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dd6f2-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dd6f2-172">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dd6f2-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd6f2-173"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="dd6f2-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dd6f2-174">Idl</span><span class="sxs-lookup"><span data-stu-id="dd6f2-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd6f2-175"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd6f2-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dd6f2-176">DLL</span><span class="sxs-lookup"><span data-stu-id="dd6f2-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd6f2-177"><dt>Shell32.dll (versão 4.71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dd6f2-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




