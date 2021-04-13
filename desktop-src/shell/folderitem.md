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
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457201"
---
# <a name="folderitem-object"></a><span data-ttu-id="efcdf-104">Objeto FolderItem</span><span class="sxs-lookup"><span data-stu-id="efcdf-104">FolderItem object</span></span>

<span data-ttu-id="efcdf-105">Representa um item em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="efcdf-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="efcdf-106">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="efcdf-107">Membros</span><span class="sxs-lookup"><span data-stu-id="efcdf-107">Members</span></span>

<span data-ttu-id="efcdf-108">O objeto **FolderItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="efcdf-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="efcdf-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="efcdf-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="efcdf-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efcdf-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="efcdf-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="efcdf-111">Methods</span></span>

<span data-ttu-id="efcdf-112">O objeto **FolderItem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="efcdf-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="efcdf-113">Método</span><span class="sxs-lookup"><span data-stu-id="efcdf-113">Method</span></span>                                      | <span data-ttu-id="efcdf-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="efcdf-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efcdf-115">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="efcdf-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="efcdf-116">Executa um verbo no item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="efcdf-117">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="efcdf-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="efcdf-118">Recupera o objeto [**FolderItemVerbs**](folderitemverbs.md) do item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="efcdf-119">Esse objeto é a coleção de verbos que podem ser executados no item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="efcdf-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efcdf-120">Properties</span></span>

<span data-ttu-id="efcdf-121">O objeto **FolderItem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="efcdf-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="efcdf-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="efcdf-122">Property</span></span>                                                   | <span data-ttu-id="efcdf-123">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="efcdf-123">Access type</span></span>           | <span data-ttu-id="efcdf-124">Description</span><span class="sxs-lookup"><span data-stu-id="efcdf-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efcdf-125">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="efcdf-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="efcdf-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-126">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-127">Contém o objeto de [**aplicativo**](folderitem-application.md) do item de pasta.</span><span class="sxs-lookup"><span data-stu-id="efcdf-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="efcdf-128">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="efcdf-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="efcdf-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-129">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-130">Contém o objeto de [**pasta**](folder.md) do item, se o item for uma pasta.</span><span class="sxs-lookup"><span data-stu-id="efcdf-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="efcdf-131">**GetLink**</span><span class="sxs-lookup"><span data-stu-id="efcdf-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="efcdf-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-132">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-133">Contém o objeto [**ShellLinkObject**](shelllinkobject-object.md) do item, se o item for um atalho.</span><span class="sxs-lookup"><span data-stu-id="efcdf-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="efcdf-134">**Isnavegável**</span><span class="sxs-lookup"><span data-stu-id="efcdf-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="efcdf-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-135">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-136">Indica se o item pode ser hospedado dentro de um navegador ou quadro do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="efcdf-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="efcdf-137">**Isfilesystem**</span><span class="sxs-lookup"><span data-stu-id="efcdf-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="efcdf-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-138">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-139">Indica se o item faz parte do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="efcdf-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="efcdf-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="efcdf-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="efcdf-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-141">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-142">Indica se o item é uma pasta.</span><span class="sxs-lookup"><span data-stu-id="efcdf-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="efcdf-143">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="efcdf-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="efcdf-144">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-144">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-145">Indica se o item é um atalho.</span><span class="sxs-lookup"><span data-stu-id="efcdf-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="efcdf-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="efcdf-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="efcdf-147">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="efcdf-147">Read/write</span></span><br/> | <span data-ttu-id="efcdf-148">Define ou obtém a data e a hora da última modificação de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="efcdf-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="efcdf-149">[**ModifyDate**](folderitem-modifydate.md) pode ser usado para recuperar a data e a hora em que uma pasta foi modificada pela última vez, mas não pode defini-la.</span><span class="sxs-lookup"><span data-stu-id="efcdf-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="efcdf-150">**Name**</span><span class="sxs-lookup"><span data-stu-id="efcdf-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="efcdf-151">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="efcdf-151">Read/write</span></span><br/> | <span data-ttu-id="efcdf-152">Define ou Obtém o nome do item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="efcdf-153">**Pai**</span><span class="sxs-lookup"><span data-stu-id="efcdf-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="efcdf-154">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-154">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-155">Obtém um objeto que representa o pai do item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="efcdf-156">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="efcdf-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="efcdf-157">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-157">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-158">Contém o caminho e o nome completos do item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="efcdf-159">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="efcdf-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="efcdf-160">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-160">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-161">Contém o tamanho do item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="efcdf-162">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="efcdf-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="efcdf-163">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efcdf-163">Read-only</span></span><br/>  | <span data-ttu-id="efcdf-164">Contém uma representação de cadeia de caracteres do tipo do item.</span><span class="sxs-lookup"><span data-stu-id="efcdf-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="efcdf-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efcdf-165">Requirements</span></span>



| <span data-ttu-id="efcdf-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="efcdf-166">Requirement</span></span> | <span data-ttu-id="efcdf-167">Valor</span><span class="sxs-lookup"><span data-stu-id="efcdf-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efcdf-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efcdf-168">Minimum supported client</span></span><br/> | <span data-ttu-id="efcdf-169">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="efcdf-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="efcdf-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efcdf-170">Minimum supported server</span></span><br/> | <span data-ttu-id="efcdf-171">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="efcdf-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="efcdf-172">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="efcdf-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="efcdf-173"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="efcdf-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="efcdf-174">INSERI</span><span class="sxs-lookup"><span data-stu-id="efcdf-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="efcdf-175"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="efcdf-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="efcdf-176">DLL</span><span class="sxs-lookup"><span data-stu-id="efcdf-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efcdf-177"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="efcdf-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




