---
description: Gerencia links do Shell. Esse objeto torna grande parte da funcionalidade da interface IShellLink disponível para scripts de aplicativos.
title: Objeto ShellLinkObject (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968195"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="5b5bd-104">Objeto ShellLinkObject</span><span class="sxs-lookup"><span data-stu-id="5b5bd-104">ShellLinkObject object</span></span>

<span data-ttu-id="5b5bd-105">Gerencia links do Shell.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-105">Manages Shell links.</span></span> <span data-ttu-id="5b5bd-106">Esse objeto torna grande parte da funcionalidade da interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) disponível para scripts de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="5b5bd-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5b5bd-107">Members</span></span>

<span data-ttu-id="5b5bd-108">O objeto **ShellLinkObject** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b5bd-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="5b5bd-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b5bd-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5b5bd-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b5bd-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5b5bd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b5bd-111">Methods</span></span>

<span data-ttu-id="5b5bd-112">O objeto **ShellLinkObject** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="5b5bd-113">Método</span><span class="sxs-lookup"><span data-stu-id="5b5bd-113">Method</span></span>                                                     | <span data-ttu-id="5b5bd-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b5bd-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b5bd-115">**GetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="5b5bd-116">Obtém o local do ícone atribuído ao link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="5b5bd-117">**Resolver**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="5b5bd-118">Procura o destino de um link do Shell, mesmo que o destino tenha sido movido ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="5b5bd-119">**Salvar**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="5b5bd-120">Salva todas as alterações no link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="5b5bd-121">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="5b5bd-122">Define o local do ícone atribuído ao link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="5b5bd-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b5bd-123">Properties</span></span>

<span data-ttu-id="5b5bd-124">O objeto **ShellLinkObject** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="5b5bd-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5b5bd-125">Property</span></span>                                                                | <span data-ttu-id="5b5bd-126">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5b5bd-126">Access type</span></span>           | <span data-ttu-id="5b5bd-127">Description</span><span class="sxs-lookup"><span data-stu-id="5b5bd-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b5bd-128">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="5b5bd-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5bd-129">Read/write</span></span><br/> | <span data-ttu-id="5b5bd-130">Contém os argumentos de um link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="5b5bd-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="5b5bd-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5bd-132">Read/write</span></span><br/> | <span data-ttu-id="5b5bd-133">Obtém ou define a descrição do link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="5b5bd-134">**Tecla**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="5b5bd-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5bd-135">Read/write</span></span><br/> | <span data-ttu-id="5b5bd-136">Obtém ou define o atalho de teclado para o link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="5b5bd-137">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="5b5bd-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5bd-138">Read/write</span></span><br/> | <span data-ttu-id="5b5bd-139">Obtém ou define o caminho para o objeto de link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="5b5bd-140">**ShowCommand**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="5b5bd-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5bd-141">Read/write</span></span><br/> | <span data-ttu-id="5b5bd-142">Obtém ou define o estado de exibição inicial (dimensionado, minimizado ou maximizado) do comando do link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="5b5bd-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="5b5bd-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="5b5bd-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5b5bd-144">Read/write</span></span><br/> | <span data-ttu-id="5b5bd-145">Obtém ou define o diretório de trabalho especificado no link.</span><span class="sxs-lookup"><span data-stu-id="5b5bd-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="5b5bd-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5bd-146">Requirements</span></span>



| <span data-ttu-id="5b5bd-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5bd-147">Requirement</span></span> | <span data-ttu-id="5b5bd-148">Valor</span><span class="sxs-lookup"><span data-stu-id="5b5bd-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5bd-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5bd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5bd-150">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5b5bd-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b5bd-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5bd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5bd-152">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b5bd-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5b5bd-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b5bd-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5bd-154"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5bd-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5b5bd-155">INSERI</span><span class="sxs-lookup"><span data-stu-id="5b5bd-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b5bd-156"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b5bd-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5b5bd-157">DLL</span><span class="sxs-lookup"><span data-stu-id="5b5bd-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b5bd-158"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5b5bd-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5bd-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b5bd-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5bd-160">Links do Shell</span><span class="sxs-lookup"><span data-stu-id="5b5bd-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
