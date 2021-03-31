---
title: Editar contextos
description: Editar contextos
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- TSF (estrutura de serviços de texto), editar contextos
- TSF (estrutura de serviços de texto), editar contextos
- serviços de texto, editar contextos
- Aplicativos habilitados para TSF, editar contextos
- editar contextos
- TSF (estrutura de serviços de texto), editar cookies
- TSF (estrutura de serviços de texto), editar cookies
- serviços de texto, editar cookies
- Aplicativos habilitados para TSF, editar cookies
- editar cookies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822531"
---
# <a name="edit-contexts"></a><span data-ttu-id="e1be7-113">Editar contextos</span><span class="sxs-lookup"><span data-stu-id="e1be7-113">Edit Contexts</span></span>

## <a name="applications"></a><span data-ttu-id="e1be7-114">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e1be7-114">Applications</span></span>

<span data-ttu-id="e1be7-115">Para criar um contexto de edição, um aplicativo chama [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="e1be7-115">To create an edit context, an application calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>

## <a name="text-services"></a><span data-ttu-id="e1be7-116">Serviços de texto</span><span class="sxs-lookup"><span data-stu-id="e1be7-116">Text Services</span></span>

<span data-ttu-id="e1be7-117">Um serviço de texto geralmente usa o contexto de edição atualmente ativo.</span><span class="sxs-lookup"><span data-stu-id="e1be7-117">A text service often uses the currently active edit context.</span></span> <span data-ttu-id="e1be7-118">O contexto de edição atualmente ativo é o contexto de edição na parte superior da pilha do Gerenciador de documentos ativo.</span><span class="sxs-lookup"><span data-stu-id="e1be7-118">The currently active edit context is the edit context at the top of the stack of the active document manager.</span></span> <span data-ttu-id="e1be7-119">Para obter o contexto ativo no momento, um serviço de texto chama [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) para obter o Gerenciador de documentos ativo e, em seguida, chama [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) para obter o contexto de edição na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="e1be7-119">To obtain the currently active context, a text service calls [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) to obtain the active document manager and then calls [ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) to obtain the edit context at the top of the stack.</span></span>

<span data-ttu-id="e1be7-120">Em alguns casos, um serviço de texto requer seu próprio contexto de edição.</span><span class="sxs-lookup"><span data-stu-id="e1be7-120">In some cases, a text service requires its own edit context.</span></span> <span data-ttu-id="e1be7-121">Para criar um contexto de edição, um serviço de texto chama **ITfDocumentMgr:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="e1be7-121">To create an edit context, a text service calls **ITfDocumentMgr::CreateContext**.</span></span>

## <a name="edit-cookies"></a><span data-ttu-id="e1be7-122">Editar cookies</span><span class="sxs-lookup"><span data-stu-id="e1be7-122">Edit Cookies</span></span>

<span data-ttu-id="e1be7-123">Muitos métodos, como [ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), exigem uma maneira de identificar um contexto de edição que tem um [bloqueio de documento](document-locks.md)somente leitura ou leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e1be7-123">Many methods, such as [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), require a way to identify an edit context that has a read-only or read/write [document lock](document-locks.md).</span></span> <span data-ttu-id="e1be7-124">Um bloqueio de documento é obtido por meio de uma negociação entre o Gerenciador de TSF e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1be7-124">A document lock is obtained through a negotiation between the TSF manager and the application.</span></span> <span data-ttu-id="e1be7-125">Um serviço de texto não pode executar essa negociação diretamente.</span><span class="sxs-lookup"><span data-stu-id="e1be7-125">A text service cannot perform this negotiation directly.</span></span> <span data-ttu-id="e1be7-126">Um serviço de texto só pode obter um bloqueio solicitando uma [sessão de edição](edit-sessions.md) com um contexto específico e acesso somente leitura ou de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e1be7-126">A text service can only obtain a lock by requesting an [edit session](edit-sessions.md) with a specific context and read-only or read/write access.</span></span> <span data-ttu-id="e1be7-127">Quando a sessão de edição é concedida, o serviço de texto é fornecido com um *cookie de edição* que identifica o contexto de edição com o acesso solicitado.</span><span class="sxs-lookup"><span data-stu-id="e1be7-127">When the edit session is granted, the text service is supplied with an *edit cookie* that identifies the edit context with the requested access.</span></span> <span data-ttu-id="e1be7-128">Esse cookie é passado para o método para identificar o contexto de edição com o acesso apropriado.</span><span class="sxs-lookup"><span data-stu-id="e1be7-128">This cookie is then passed to the method to identify the edit context with the proper access.</span></span>

<span data-ttu-id="e1be7-129">**ITfDocumentMgr:: CreateContext** também fornece um cookie de edição para o criador de contexto.</span><span class="sxs-lookup"><span data-stu-id="e1be7-129">**ITfDocumentMgr::CreateContext** also supplies an edit cookie to the context creator.</span></span> <span data-ttu-id="e1be7-130">Esse cookie tem acesso somente leitura e não há como modificar o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="e1be7-130">This cookie has read-only access and there is no way to modify the access level.</span></span> <span data-ttu-id="e1be7-131">Na verdade, o Gerenciador do TSF não negocia um bloqueio de documento para este cookie de edição.</span><span class="sxs-lookup"><span data-stu-id="e1be7-131">In truth, the TSF manager does not negotiate a document lock for this edit cookie.</span></span> <span data-ttu-id="e1be7-132">O cookie é marcado internamente como somente leitura, mas o documento não está realmente bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e1be7-132">The cookie is internally marked read-only, but the document is not actually locked.</span></span> <span data-ttu-id="e1be7-133">Por exemplo, se o criador de contexto chamar [ITfContext:: Getselecting](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) com o cookie de edição retornado por **ITfDocumentMgr:: CreateContext** , isso resultará na chamada de [ITextStoreACP:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) ou [ITextStoreAnchor:: getselecionation](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1be7-133">For example, if the context creator calls [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) with the edit cookie returned by **ITfDocumentMgr::CreateContext** , this results in the application's [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) or [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) being called.</span></span> <span data-ttu-id="e1be7-134">Antes de obter a seleção, o aplicativo determinará se existe um bloqueio de documento.</span><span class="sxs-lookup"><span data-stu-id="e1be7-134">Before obtaining the selection, the application will determine if a document lock exists.</span></span> <span data-ttu-id="e1be7-135">Como não existe bloqueio, o aplicativo falhará com TS \_ E \_ NOLOCK.</span><span class="sxs-lookup"><span data-stu-id="e1be7-135">Because no lock exists, the application will fail with TS\_E\_NOLOCK.</span></span> <span data-ttu-id="e1be7-136">Ou seja, se um aplicativo chama um método com esse cookie que resulta em um dos métodos de armazenamento de texto do aplicativo que está sendo chamado, ele deve tratar esse caso internamente, pois o aplicativo não terá realmente um bloqueio de documento.</span><span class="sxs-lookup"><span data-stu-id="e1be7-136">That is, if an application calls a method with this cookie that results in one of the application's text store methods being called, it must handle this case internally because the application will not actually have a document lock.</span></span>

<span data-ttu-id="e1be7-137">Se o criador de contexto exigir um cookie de edição com acesso de leitura/gravação, ele deverá estabelecer sua própria sessão de edição.</span><span class="sxs-lookup"><span data-stu-id="e1be7-137">If the context creator requires an edit cookie with read/write access, it must establish its own edit session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1be7-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1be7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1be7-139">ITfContext</span><span class="sxs-lookup"><span data-stu-id="e1be7-139">ITfContext</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[<span data-ttu-id="e1be7-140">ITfDocumentMgr:: CreateContext</span><span class="sxs-lookup"><span data-stu-id="e1be7-140">ITfDocumentMgr::CreateContext</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="e1be7-141">ITfThreadMgr:: GetFocus</span><span class="sxs-lookup"><span data-stu-id="e1be7-141">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[<span data-ttu-id="e1be7-142">ITfDocumentMgr:: GetTop</span><span class="sxs-lookup"><span data-stu-id="e1be7-142">ITfDocumentMgr::GetTop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[<span data-ttu-id="e1be7-143">ITfRange:: SetText</span><span class="sxs-lookup"><span data-stu-id="e1be7-143">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="e1be7-144">Bloqueios de documentos</span><span class="sxs-lookup"><span data-stu-id="e1be7-144">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="e1be7-145">Editar sessões</span><span class="sxs-lookup"><span data-stu-id="e1be7-145">Edit Sessions</span></span>](edit-sessions.md)
</dt> <dt>

[<span data-ttu-id="e1be7-146">ITfContext:: getseleções</span><span class="sxs-lookup"><span data-stu-id="e1be7-146">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="e1be7-147">ITextStoreACP:: getseleções</span><span class="sxs-lookup"><span data-stu-id="e1be7-147">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="e1be7-148">ITextStoreAnchor:: getseleções</span><span class="sxs-lookup"><span data-stu-id="e1be7-148">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




