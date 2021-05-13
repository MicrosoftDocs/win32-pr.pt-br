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
ms.openlocfilehash: 5862ae3c9b7bf1262edbc28b06f2963f2e577275
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842627"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="f1964-104">Objeto ShellLinkObject</span><span class="sxs-lookup"><span data-stu-id="f1964-104">ShellLinkObject object</span></span>

<span data-ttu-id="f1964-105">Gerencia links do Shell.</span><span class="sxs-lookup"><span data-stu-id="f1964-105">Manages Shell links.</span></span> <span data-ttu-id="f1964-106">Esse objeto torna grande parte da funcionalidade da interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) disponível para scripts de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f1964-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="f1964-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f1964-107">Members</span></span>

<span data-ttu-id="f1964-108">O objeto **ShellLinkObject** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f1964-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="f1964-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f1964-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1964-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1964-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1964-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f1964-111">Methods</span></span>

<span data-ttu-id="f1964-112">O objeto **ShellLinkObject** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f1964-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="f1964-113">Método</span><span class="sxs-lookup"><span data-stu-id="f1964-113">Method</span></span>                                                     | <span data-ttu-id="f1964-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1964-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1964-115">**GetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="f1964-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="f1964-116">Obtém o local do ícone atribuído ao link.</span><span class="sxs-lookup"><span data-stu-id="f1964-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="f1964-117">**Resolver**</span><span class="sxs-lookup"><span data-stu-id="f1964-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="f1964-118">Procura o destino de um link do Shell, mesmo que o destino tenha sido movido ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="f1964-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="f1964-119">**Salvar**</span><span class="sxs-lookup"><span data-stu-id="f1964-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="f1964-120">Salva todas as alterações no link.</span><span class="sxs-lookup"><span data-stu-id="f1964-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="f1964-121">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="f1964-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="f1964-122">Define o local do ícone atribuído ao link.</span><span class="sxs-lookup"><span data-stu-id="f1964-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="f1964-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1964-123">Properties</span></span>

<span data-ttu-id="f1964-124">O objeto **ShellLinkObject** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1964-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="f1964-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f1964-125">Property</span></span>                                                                | <span data-ttu-id="f1964-126">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="f1964-126">Access type</span></span>           | <span data-ttu-id="f1964-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1964-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1964-128">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="f1964-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="f1964-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f1964-129">Read/write</span></span><br/> | <span data-ttu-id="f1964-130">Contém os argumentos de um link.</span><span class="sxs-lookup"><span data-stu-id="f1964-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="f1964-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f1964-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="f1964-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f1964-132">Read/write</span></span><br/> | <span data-ttu-id="f1964-133">Obtém ou define a descrição do link.</span><span class="sxs-lookup"><span data-stu-id="f1964-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="f1964-134">**Tecla**</span><span class="sxs-lookup"><span data-stu-id="f1964-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="f1964-135">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f1964-135">Read/write</span></span><br/> | <span data-ttu-id="f1964-136">Obtém ou define o atalho de teclado para o link.</span><span class="sxs-lookup"><span data-stu-id="f1964-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="f1964-137">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="f1964-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="f1964-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f1964-138">Read/write</span></span><br/> | <span data-ttu-id="f1964-139">Obtém ou define o caminho para o objeto de link.</span><span class="sxs-lookup"><span data-stu-id="f1964-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="f1964-140">**ShowCommand**</span><span class="sxs-lookup"><span data-stu-id="f1964-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="f1964-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f1964-141">Read/write</span></span><br/> | <span data-ttu-id="f1964-142">Obtém ou define o estado de exibição inicial (dimensionado, minimizado ou maximizada) do comando do link.</span><span class="sxs-lookup"><span data-stu-id="f1964-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="f1964-143">**Workingdirectory**</span><span class="sxs-lookup"><span data-stu-id="f1964-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="f1964-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f1964-144">Read/write</span></span><br/> | <span data-ttu-id="f1964-145">Obtém ou define o diretório de trabalho especificado no link.</span><span class="sxs-lookup"><span data-stu-id="f1964-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="f1964-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1964-146">Requirements</span></span>



| <span data-ttu-id="f1964-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1964-147">Requirement</span></span> | <span data-ttu-id="f1964-148">Valor</span><span class="sxs-lookup"><span data-stu-id="f1964-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1964-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1964-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f1964-150">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f1964-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1964-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1964-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f1964-152">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1964-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f1964-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1964-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1964-154"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f1964-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f1964-155">Idl</span><span class="sxs-lookup"><span data-stu-id="f1964-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1964-156"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1964-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f1964-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f1964-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1964-158"><dt>Shell32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f1964-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1964-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1964-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1964-160">Shell Links</span><span class="sxs-lookup"><span data-stu-id="f1964-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
