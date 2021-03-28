---
description: Representa uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a pasta.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Objeto de pasta (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501160"
---
# <a name="folder-object"></a><span data-ttu-id="5d7cc-104">Objeto de pasta</span><span class="sxs-lookup"><span data-stu-id="5d7cc-104">Folder object</span></span>

<span data-ttu-id="5d7cc-105">Representa uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-105">Represents a Shell folder.</span></span> <span data-ttu-id="5d7cc-106">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a pasta.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-106">This object contains properties and methods that allow you to retrieve information about the folder.</span></span>

## <a name="members"></a><span data-ttu-id="5d7cc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5d7cc-107">Members</span></span>

<span data-ttu-id="5d7cc-108">O objeto **Folder** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d7cc-108">The **Folder** object has these types of members:</span></span>

-   [<span data-ttu-id="5d7cc-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d7cc-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5d7cc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d7cc-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5d7cc-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d7cc-111">Methods</span></span>

<span data-ttu-id="5d7cc-112">O objeto **Folder** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-112">The **Folder** object has these methods.</span></span>



| <span data-ttu-id="5d7cc-113">Método</span><span class="sxs-lookup"><span data-stu-id="5d7cc-113">Method</span></span>                                      | <span data-ttu-id="5d7cc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d7cc-114">Description</span></span>                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d7cc-115">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-115">**CopyHere**</span></span>](folder-copyhere.md)         | <span data-ttu-id="5d7cc-116">Copia um item ou itens para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-116">Copies an item or items to a folder.</span></span><br/>                                                                            |
| [<span data-ttu-id="5d7cc-117">**GetDetailsOf**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-117">**GetDetailsOf**</span></span>](folder-getdetailsof.md) | <span data-ttu-id="5d7cc-118">Recupera detalhes sobre um item em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-118">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="5d7cc-119">Por exemplo, seu tamanho, tipo ou a hora de sua última modificação.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-119">For example, its size, type, or the time of its last modification.</span></span><br/> |
| [<span data-ttu-id="5d7cc-120">**Itens**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-120">**Items**</span></span>](folder-items.md)               | <span data-ttu-id="5d7cc-121">Recupera um objeto [**FolderItems**](folderitems.md) que representa a coleção de itens na pasta.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-121">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span><br/>    |
| [<span data-ttu-id="5d7cc-122">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-122">**MoveHere**</span></span>](folder-movehere.md)         | <span data-ttu-id="5d7cc-123">Move um item ou itens para esta pasta.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-123">Moves an item or items to this folder.</span></span><br/>                                                                          |
| [<span data-ttu-id="5d7cc-124">**NewFolder**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-124">**NewFolder**</span></span>](folder-newfolder.md)       | <span data-ttu-id="5d7cc-125">Cria uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-125">Creates a new folder.</span></span><br/>                                                                                           |
| [<span data-ttu-id="5d7cc-126">**ParseName**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-126">**ParseName**</span></span>](folder-parsename.md)       | <span data-ttu-id="5d7cc-127">Cria e retorna um objeto [**FolderItem**](folderitem.md) que representa um item especificado.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-127">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="5d7cc-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d7cc-128">Properties</span></span>

<span data-ttu-id="5d7cc-129">O objeto **Folder** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-129">The **Folder** object has these properties.</span></span>



| <span data-ttu-id="5d7cc-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5d7cc-130">Property</span></span>                                               | <span data-ttu-id="5d7cc-131">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5d7cc-131">Access type</span></span>          | <span data-ttu-id="5d7cc-132">Description</span><span class="sxs-lookup"><span data-stu-id="5d7cc-132">Description</span></span>                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [<span data-ttu-id="5d7cc-133">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-133">**Application**</span></span>](folder-application.md)<br/>   | <span data-ttu-id="5d7cc-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d7cc-134">Read-only</span></span><br/> | <span data-ttu-id="5d7cc-135">Contém o objeto de aplicativo da pasta.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-135">Contains the folder's Application object.</span></span><br/> |
| [<span data-ttu-id="5d7cc-136">**Pai**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-136">**Parent**</span></span>](folder-parent.md)<br/>             | <span data-ttu-id="5d7cc-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d7cc-137">Read-only</span></span><br/> | <span data-ttu-id="5d7cc-138">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-138">Not implemented.</span></span><br/>                          |
| [<span data-ttu-id="5d7cc-139">**ParentFolder**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-139">**ParentFolder**</span></span>](folder-parentfolder.md)<br/> | <span data-ttu-id="5d7cc-140">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d7cc-140">Read-only</span></span><br/> | <span data-ttu-id="5d7cc-141">Contém o objeto da **pasta** pai.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-141">Contains the parent **Folder** object.</span></span><br/>    |
| [<span data-ttu-id="5d7cc-142">**Título**</span><span class="sxs-lookup"><span data-stu-id="5d7cc-142">**Title**</span></span>](folder-title.md)<br/>               | <span data-ttu-id="5d7cc-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d7cc-143">Read-only</span></span><br/> | <span data-ttu-id="5d7cc-144">Contém o título da pasta.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-144">Contains the title of the folder.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="5d7cc-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d7cc-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d7cc-146">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="5d7cc-147">Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="5d7cc-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="5d7cc-148">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="5d7cc-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d7cc-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d7cc-149">Requirements</span></span>



| <span data-ttu-id="5d7cc-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7cc-150">Requirement</span></span> | <span data-ttu-id="5d7cc-151">Valor</span><span class="sxs-lookup"><span data-stu-id="5d7cc-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7cc-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d7cc-152">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7cc-153">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5d7cc-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="5d7cc-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d7cc-154">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7cc-155">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d7cc-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5d7cc-156">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5d7cc-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7cc-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d7cc-157"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d7cc-158">INSERI</span><span class="sxs-lookup"><span data-stu-id="5d7cc-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d7cc-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d7cc-159"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




