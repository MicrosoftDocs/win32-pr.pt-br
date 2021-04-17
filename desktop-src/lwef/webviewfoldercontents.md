---
title: Objeto WebViewFolderContents (Shldisp.h)
description: Implementado pelo shell para uso dentro de uma WebView.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, descritos
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812017"
---
# <a name="webviewfoldercontents-object"></a><span data-ttu-id="e6cb0-105">Objeto WebViewFolderContents</span><span class="sxs-lookup"><span data-stu-id="e6cb0-105">WebViewFolderContents object</span></span>

<span data-ttu-id="e6cb0-106">Implementado pelo shell para uso dentro de uma *WebView*.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-106">Implemented by the Shell for use inside a *WebView*.</span></span> <span data-ttu-id="e6cb0-107">**WebViewFolderContents** se inicializa automaticamente para a pasta atual da WebView.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-107">**WebViewFolderContents** automatically initializes itself to WebView's current folder.</span></span> <span data-ttu-id="e6cb0-108">Ele cria um modo de exibição de pasta do shell que exibe o conteúdo da pasta em um dos cinco formatos: ícone pequeno, ícone grande, lista, detalhes ou miniatura.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-108">It creates a Shell folder view that displays the contents of the folder in one of five formats: Small Icon, Large Icon, List, Details, or Thumbnail.</span></span> <span data-ttu-id="e6cb0-109">Ele não é válido fora de uma WebView.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-109">It is not valid outside of a WebView.</span></span>

<span data-ttu-id="e6cb0-110">Os métodos e as propriedades expostas por **WebViewFolderContents** são idênticos aos do objeto [**ShellFolderView**](/windows/desktop/shell/shellfolderview) .</span><span class="sxs-lookup"><span data-stu-id="e6cb0-110">The methods and properties exposed by **WebViewFolderContents** are identical to those of the [**ShellFolderView**](/windows/desktop/shell/shellfolderview) object.</span></span>

## <a name="members"></a><span data-ttu-id="e6cb0-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e6cb0-111">Members</span></span>

<span data-ttu-id="e6cb0-112">O objeto **WebViewFolderContents** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e6cb0-112">The **WebViewFolderContents** object has these types of members:</span></span>

-   [<span data-ttu-id="e6cb0-113">Eventos</span><span class="sxs-lookup"><span data-stu-id="e6cb0-113">Events</span></span>](#events)
-   [<span data-ttu-id="e6cb0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6cb0-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6cb0-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6cb0-115">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="e6cb0-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="e6cb0-116">Events</span></span>

<span data-ttu-id="e6cb0-117">O objeto **WebViewFolderContents** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-117">The **WebViewFolderContents** object has these events.</span></span>



| <span data-ttu-id="e6cb0-118">Evento</span><span class="sxs-lookup"><span data-stu-id="e6cb0-118">Event</span></span>                                                              | <span data-ttu-id="e6cb0-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6cb0-119">Description</span></span>                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6cb0-120">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-120">**SelectionChanged**</span></span>](webviewfoldercontents-selectionchanged.md) | <span data-ttu-id="e6cb0-121">Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-121">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="e6cb0-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6cb0-122">Methods</span></span>

<span data-ttu-id="e6cb0-123">O objeto **WebViewFolderContents** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-123">The **WebViewFolderContents** object has these methods.</span></span>



| <span data-ttu-id="e6cb0-124">Método</span><span class="sxs-lookup"><span data-stu-id="e6cb0-124">Method</span></span>                                                       | <span data-ttu-id="e6cb0-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6cb0-125">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6cb0-126">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-126">**PopupItemMenu**</span></span>](webviewfoldercontents-popupitemmenu.md) | <span data-ttu-id="e6cb0-127">Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-127">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                   |
| [<span data-ttu-id="e6cb0-128">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-128">**SelectedItems**</span></span>](webviewfoldercontents-selecteditems.md) | <span data-ttu-id="e6cb0-129">Obtém um objeto [**FolderItems**](../shell/folderitems.md) que representa todos os itens selecionados na exibição.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-129">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="e6cb0-130">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-130">**SelectItem**</span></span>](webviewfoldercontents-selectitem.md)       | <span data-ttu-id="e6cb0-131">Define o estado de seleção de um item na exibição.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-131">Sets the selection state of an item in the view.</span></span><br/>                                                          |



 

### <a name="properties"></a><span data-ttu-id="e6cb0-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6cb0-132">Properties</span></span>

<span data-ttu-id="e6cb0-133">O objeto **WebViewFolderContents** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-133">The **WebViewFolderContents** object has these properties.</span></span>



| <span data-ttu-id="e6cb0-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e6cb0-134">Property</span></span>                                                            | <span data-ttu-id="e6cb0-135">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="e6cb0-135">Access type</span></span>          | <span data-ttu-id="e6cb0-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6cb0-136">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6cb0-137">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-137">**Application**</span></span>](webviewfoldercontents-application.md)<br/> | <span data-ttu-id="e6cb0-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb0-138">Read-only</span></span><br/> | <span data-ttu-id="e6cb0-139">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-139">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e6cb0-140">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-140">**FocusedItem**</span></span>](webviewfoldercontents-focuseditem.md)<br/> | <span data-ttu-id="e6cb0-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb0-141">Read-only</span></span><br/> | <span data-ttu-id="e6cb0-142">Obtém um objeto [**FolderItem**](../shell/folderitem.md) que representa o item que tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-142">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span><br/>                           |
| [<span data-ttu-id="e6cb0-143">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-143">**Folder**</span></span>](webviewfoldercontents-folder.md)<br/>           | <span data-ttu-id="e6cb0-144">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb0-144">Read-only</span></span><br/> | <span data-ttu-id="e6cb0-145">Obtém um objeto [**Folder**](../shell/folder.md) que representa a exibição.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-145">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span><br/>                                                            |
| [<span data-ttu-id="e6cb0-146">**Pai**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-146">**Parent**</span></span>](webviewfoldercontents-parent.md)<br/>           | <span data-ttu-id="e6cb0-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb0-147">Read-only</span></span><br/> | <span data-ttu-id="e6cb0-148">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-148">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e6cb0-149">**Script**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-149">**Script**</span></span>](webviewfoldercontents-script.md)<br/>           | <span data-ttu-id="e6cb0-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb0-150">Read-only</span></span><br/> | <span data-ttu-id="e6cb0-151">Obtém o objeto de script para a exibição.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-151">Gets the scripting object for the view.</span></span><br/>                                                                                       |
| [<span data-ttu-id="e6cb0-152">**Exibiroptions**</span><span class="sxs-lookup"><span data-stu-id="e6cb0-152">**ViewOptions**</span></span>](webviewfoldercontents-viewoptions.md)<br/> | <span data-ttu-id="e6cb0-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6cb0-153">Read-only</span></span><br/> | <span data-ttu-id="e6cb0-154">Obtém um conjunto de sinalizadores [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indicam as opções atuais da exibição.</span><span class="sxs-lookup"><span data-stu-id="e6cb0-154">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e6cb0-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6cb0-155">Requirements</span></span>



| <span data-ttu-id="e6cb0-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6cb0-156">Requirement</span></span> | <span data-ttu-id="e6cb0-157">Valor</span><span class="sxs-lookup"><span data-stu-id="e6cb0-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cb0-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6cb0-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e6cb0-159">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e6cb0-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e6cb0-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6cb0-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e6cb0-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6cb0-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e6cb0-162">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e6cb0-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6cb0-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6cb0-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e6cb0-164">INSERI</span><span class="sxs-lookup"><span data-stu-id="e6cb0-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6cb0-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6cb0-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e6cb0-166">DLL</span><span class="sxs-lookup"><span data-stu-id="e6cb0-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6cb0-167"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e6cb0-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

