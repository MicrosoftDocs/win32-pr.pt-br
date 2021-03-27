---
description: Encaminha os eventos acionados por um objeto ShellFolderView especificado para manipuladores de eventos ShellFolderViewOC correspondentes.
title: Objeto ShellFolderViewOC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: b9a2b76f48731bf4c7b515779122503fa2cb02f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922490"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="23089-103">Objeto ShellFolderViewOC</span><span class="sxs-lookup"><span data-stu-id="23089-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="23089-104">Encaminha os eventos acionados por um objeto [**ShellFolderView**](shellfolderview.md) especificado para manipuladores de eventos **ShellFolderViewOC** correspondentes.</span><span class="sxs-lookup"><span data-stu-id="23089-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="23089-105">Membros</span><span class="sxs-lookup"><span data-stu-id="23089-105">Members</span></span>

<span data-ttu-id="23089-106">O objeto **ShellFolderViewOC** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="23089-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="23089-107">Eventos</span><span class="sxs-lookup"><span data-stu-id="23089-107">Events</span></span>](#events)
-   [<span data-ttu-id="23089-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="23089-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="23089-109">Eventos</span><span class="sxs-lookup"><span data-stu-id="23089-109">Events</span></span>

<span data-ttu-id="23089-110">O objeto **ShellFolderViewOC** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="23089-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="23089-111">Evento</span><span class="sxs-lookup"><span data-stu-id="23089-111">Event</span></span>                                                          | <span data-ttu-id="23089-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="23089-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23089-113">**EnumDone**</span><span class="sxs-lookup"><span data-stu-id="23089-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="23089-114">Indica que o objeto [**ShellFolderView**](shellfolderview.md) terminou de enumerar o conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="23089-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="23089-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="23089-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="23089-116">Indica que o estado de seleção de um ou mais itens na exibição foi alterado.</span><span class="sxs-lookup"><span data-stu-id="23089-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="23089-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="23089-117">Methods</span></span>

<span data-ttu-id="23089-118">O objeto **ShellFolderViewOC** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="23089-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="23089-119">Método</span><span class="sxs-lookup"><span data-stu-id="23089-119">Method</span></span>                                                   | <span data-ttu-id="23089-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="23089-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23089-121">**SetFolderView**</span><span class="sxs-lookup"><span data-stu-id="23089-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="23089-122">Encaminha os eventos do objeto [**ShellFolderView**](shellfolderview.md) especificado para o manipulador de eventos **ShellFolderViewOC** correspondente.</span><span class="sxs-lookup"><span data-stu-id="23089-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23089-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="23089-123">Remarks</span></span>

<span data-ttu-id="23089-124">O objeto [**ShellFolderView**](shellfolderview.md) aciona dois eventos, [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), que normalmente são manipulados por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="23089-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="23089-125">No entanto, alguns aplicativos devem manipular eventos de uma série de objetos **ShellFolderView** .</span><span class="sxs-lookup"><span data-stu-id="23089-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="23089-126">Por exemplo, um aplicativo pode hospedar um controle WebBrowser que permite aos usuários navegar por uma série de pastas.</span><span class="sxs-lookup"><span data-stu-id="23089-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="23089-127">Cada pasta tem seu próprio objeto **ShellFolderView** com seus eventos associados.</span><span class="sxs-lookup"><span data-stu-id="23089-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="23089-128">Lidar com esses eventos pode ser difícil.</span><span class="sxs-lookup"><span data-stu-id="23089-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="23089-129">O objeto **ShellFolderViewOC** simplifica a manipulação de eventos para esses cenários.</span><span class="sxs-lookup"><span data-stu-id="23089-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="23089-130">Ele permite que os aplicativos manipulem eventos para todos os objetos [**ShellFolderView**](shellfolderview.md) com um único par de manipuladores de eventos **ShellFolderViewOC** .</span><span class="sxs-lookup"><span data-stu-id="23089-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="23089-131">Cada vez que o usuário navega para uma nova pasta, o aplicativo passa o objeto **ShellFolderView** associado para o objeto **ShellFolderViewOC** chamando [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span><span class="sxs-lookup"><span data-stu-id="23089-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="23089-132">Em seguida, quando um evento [**EnumDone**](shellfolderviewoc-enumdone.md) ou [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) é acionado, o objeto **ShellFolderViewOC** encaminha o evento para seu próprio manipulador para processamento.</span><span class="sxs-lookup"><span data-stu-id="23089-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="23089-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23089-133">Requirements</span></span>



| <span data-ttu-id="23089-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="23089-134">Requirement</span></span> | <span data-ttu-id="23089-135">Valor</span><span class="sxs-lookup"><span data-stu-id="23089-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23089-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23089-136">Minimum supported client</span></span><br/> | <span data-ttu-id="23089-137">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="23089-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23089-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23089-138">Minimum supported server</span></span><br/> | <span data-ttu-id="23089-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23089-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="23089-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23089-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="23089-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23089-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="23089-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="23089-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="23089-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="23089-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="23089-144">DLL</span><span class="sxs-lookup"><span data-stu-id="23089-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23089-145"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="23089-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23089-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="23089-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23089-147">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="23089-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 




