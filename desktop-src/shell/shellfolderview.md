---
description: Representa os objetos em uma exibição e fornece propriedades e métodos usados para obter informações sobre o conteúdo da exibição.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Objeto ShellFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989062"
---
# <a name="shellfolderview-object"></a><span data-ttu-id="f138e-103">Objeto ShellFolderView</span><span class="sxs-lookup"><span data-stu-id="f138e-103">ShellFolderView object</span></span>

<span data-ttu-id="f138e-104">Representa os objetos em uma exibição e fornece propriedades e métodos usados para obter informações sobre o conteúdo da exibição.</span><span class="sxs-lookup"><span data-stu-id="f138e-104">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span>

## <a name="members"></a><span data-ttu-id="f138e-105">Membros</span><span class="sxs-lookup"><span data-stu-id="f138e-105">Members</span></span>

<span data-ttu-id="f138e-106">O objeto **ShellFolderView** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f138e-106">The **ShellFolderView** object has these types of members:</span></span>

-   [<span data-ttu-id="f138e-107">Eventos</span><span class="sxs-lookup"><span data-stu-id="f138e-107">Events</span></span>](#events)
-   [<span data-ttu-id="f138e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f138e-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="f138e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f138e-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="f138e-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="f138e-110">Events</span></span>

<span data-ttu-id="f138e-111">O objeto **ShellFolderView** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="f138e-111">The **ShellFolderView** object has these events.</span></span>



| <span data-ttu-id="f138e-112">Evento</span><span class="sxs-lookup"><span data-stu-id="f138e-112">Event</span></span>                                                        | <span data-ttu-id="f138e-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f138e-113">Description</span></span>                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f138e-114">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="f138e-114">**SelectionChanged**</span></span>](shellfolderview-selectionchanged.md) | <span data-ttu-id="f138e-115">Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.</span><span class="sxs-lookup"><span data-stu-id="f138e-115">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="f138e-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="f138e-116">Methods</span></span>

<span data-ttu-id="f138e-117">O objeto **ShellFolderView** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f138e-117">The **ShellFolderView** object has these methods.</span></span>



| <span data-ttu-id="f138e-118">Método</span><span class="sxs-lookup"><span data-stu-id="f138e-118">Method</span></span>                                                 | <span data-ttu-id="f138e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="f138e-119">Description</span></span>                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f138e-120">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="f138e-120">**PopupItemMenu**</span></span>](shellfolderview-popupitemmenu.md) | <span data-ttu-id="f138e-121">Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.</span><span class="sxs-lookup"><span data-stu-id="f138e-121">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                 |
| [<span data-ttu-id="f138e-122">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="f138e-122">**SelectedItems**</span></span>](shellfolderview-selecteditems.md) | <span data-ttu-id="f138e-123">Obtém um objeto [**FolderItems**](folderitems.md) que representa todos os itens selecionados na exibição.</span><span class="sxs-lookup"><span data-stu-id="f138e-123">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="f138e-124">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="f138e-124">**SelectItem**</span></span>](shellfolderview-selectitem.md)       | <span data-ttu-id="f138e-125">Define o estado de seleção de um item na exibição.</span><span class="sxs-lookup"><span data-stu-id="f138e-125">Sets the selection state of an item in the view.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="f138e-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f138e-126">Properties</span></span>

<span data-ttu-id="f138e-127">O objeto **ShellFolderView** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f138e-127">The **ShellFolderView** object has these properties.</span></span>



| <span data-ttu-id="f138e-128">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f138e-128">Property</span></span>                                                      | <span data-ttu-id="f138e-129">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="f138e-129">Access type</span></span>          | <span data-ttu-id="f138e-130">Description</span><span class="sxs-lookup"><span data-stu-id="f138e-130">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f138e-131">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="f138e-131">**Application**</span></span>](shellfolderview-application.md)<br/> | <span data-ttu-id="f138e-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f138e-132">Read-only</span></span><br/> | <span data-ttu-id="f138e-133">Contém o objeto de aplicativo do objeto.</span><span class="sxs-lookup"><span data-stu-id="f138e-133">Contains the object's Application object.</span></span><br/>                                                         |
| [<span data-ttu-id="f138e-134">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="f138e-134">**FocusedItem**</span></span>](shellfolderview-focuseditem.md)<br/> | <span data-ttu-id="f138e-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f138e-135">Read-only</span></span><br/> | <span data-ttu-id="f138e-136">Obtém um objeto [**FolderItem**](folderitem.md) que representa o item que tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="f138e-136">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span><br/> |
| [<span data-ttu-id="f138e-137">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="f138e-137">**Folder**</span></span>](shellfolderview-folder.md)<br/>           | <span data-ttu-id="f138e-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f138e-138">Read-only</span></span><br/> | <span data-ttu-id="f138e-139">Obtém um objeto [**Folder**](folder.md) que representa a exibição.</span><span class="sxs-lookup"><span data-stu-id="f138e-139">Gets a [**Folder**](folder.md) object that represents the view.</span></span><br/>                                  |
| [<span data-ttu-id="f138e-140">**Pai**</span><span class="sxs-lookup"><span data-stu-id="f138e-140">**Parent**</span></span>](shellfolderview-parent.md)<br/>           | <span data-ttu-id="f138e-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f138e-141">Read-only</span></span><br/> | <span data-ttu-id="f138e-142">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="f138e-142">Not implemented.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f138e-143">**Prescritiva**</span><span class="sxs-lookup"><span data-stu-id="f138e-143">**Script**</span></span>](shellfolderview-script.md)<br/>           | <span data-ttu-id="f138e-144">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f138e-144">Read-only</span></span><br/> | <span data-ttu-id="f138e-145">Preterido.</span><span class="sxs-lookup"><span data-stu-id="f138e-145">Deprecated.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f138e-146">**Exibiroptions**</span><span class="sxs-lookup"><span data-stu-id="f138e-146">**ViewOptions**</span></span>](shellfolderview-viewoptions.md)<br/> | <span data-ttu-id="f138e-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f138e-147">Read-only</span></span><br/> | <span data-ttu-id="f138e-148">Obtém um conjunto de sinalizadores que indicam as opções atuais da exibição.</span><span class="sxs-lookup"><span data-stu-id="f138e-148">Gets a set of flags that indicate the current options of the view.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="f138e-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f138e-149">Requirements</span></span>



| <span data-ttu-id="f138e-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="f138e-150">Requirement</span></span> | <span data-ttu-id="f138e-151">Valor</span><span class="sxs-lookup"><span data-stu-id="f138e-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f138e-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f138e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f138e-153">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f138e-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f138e-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f138e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f138e-155">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f138e-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f138e-156">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f138e-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="f138e-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f138e-157"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f138e-158">INSERI</span><span class="sxs-lookup"><span data-stu-id="f138e-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f138e-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f138e-159"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f138e-160">DLL</span><span class="sxs-lookup"><span data-stu-id="f138e-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f138e-161"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f138e-161"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |
| <span data-ttu-id="f138e-162">IID</span><span class="sxs-lookup"><span data-stu-id="f138e-162">IID</span></span><br/>                      | <span data-ttu-id="f138e-163">\_SHELLFOLDERVIEW CLSID</span><span class="sxs-lookup"><span data-stu-id="f138e-163">CLSID\_ShellFolderView</span></span><br/>                                                                              |



## <a name="see-also"></a><span data-ttu-id="f138e-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="f138e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f138e-165">**Sinalizadores de ShellFolderViewOptions**</span><span class="sxs-lookup"><span data-stu-id="f138e-165">**ShellFolderViewOptions Flags**</span></span>](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




