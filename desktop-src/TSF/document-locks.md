---
title: Bloqueios de documentos
description: Bloqueios de documentos
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- TSF (estrutura de serviços de texto), bloqueios de documentos
- TSF (estrutura de serviços de texto), bloqueios de documentos
- Aplicativos habilitados para TSF, bloqueios de documentos
- bloqueios de documentos
- TSF (estrutura de serviços de texto), função de caractere do aplicativo (ACP)
- TSF (estrutura de serviços de texto), função de caractere do aplicativo (ACP)
- Aplicativos habilitados para TSF, posição de caracteres do aplicativo (ACP)
- Posição de caracteres do aplicativo (ACP)
- ACP (posição do caractere do aplicativo)
- TSF (estrutura de serviços de texto), âncoras
- TSF (estrutura de serviços de texto), âncoras
- Aplicativos habilitados para TSF, âncoras
- âncoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159567"
---
# <a name="document-locks"></a><span data-ttu-id="40bdc-116">Bloqueios de documentos</span><span class="sxs-lookup"><span data-stu-id="40bdc-116">Document Locks</span></span>

## <a name="the-document-lock-protocol"></a><span data-ttu-id="40bdc-117">O protocolo de bloqueio de documento</span><span class="sxs-lookup"><span data-stu-id="40bdc-117">The Document Lock Protocol</span></span>

<span data-ttu-id="40bdc-118">Para solicitar um bloqueio de documento para aplicativos baseados em ACP, o Gerenciador de TSF chama [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span><span class="sxs-lookup"><span data-stu-id="40bdc-118">To request a document lock for ACP-based applications, the TSF manager calls [ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span></span> <span data-ttu-id="40bdc-119">Para aplicativos baseados em ancoragem, o Gerenciador TSF chama [ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span><span class="sxs-lookup"><span data-stu-id="40bdc-119">For anchor-based applications, the TSF manager calls [ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span></span> <span data-ttu-id="40bdc-120">O aplicativo concede o bloqueio de documento chamando [ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (aplicativos baseados em ACP) ou [ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (aplicativos baseados em âncora) dentro de **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="40bdc-120">The application grants the document lock by calling [ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-based applications) or [ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (anchor-based applications) inside of **RequestLock**.</span></span> <span data-ttu-id="40bdc-121">O bloqueio só é válido durante a chamada **OnLockGranted** .</span><span class="sxs-lookup"><span data-stu-id="40bdc-121">The lock is only valid during the **OnLockGranted** call.</span></span> <span data-ttu-id="40bdc-122">Quando **OnLockGranted** retorna, o documento é considerado desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="40bdc-122">When **OnLockGranted** returns, the document is considered unlocked.</span></span>

## <a name="types-of-document-locks"></a><span data-ttu-id="40bdc-123">Tipos de bloqueios de documento</span><span class="sxs-lookup"><span data-stu-id="40bdc-123">Types of Document Locks</span></span>

<span data-ttu-id="40bdc-124">Há dois tipos de bloqueios de documentos, somente leitura e leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="40bdc-124">There are two types of document locks, read-only and read/write.</span></span> <span data-ttu-id="40bdc-125">Um bloqueio somente leitura permite que o gerente Leia o texto, mas não pode modificar ou inserir texto.</span><span class="sxs-lookup"><span data-stu-id="40bdc-125">A read-only lock enables the manager to read the text, but it cannot modify or insert text.</span></span> <span data-ttu-id="40bdc-126">Um bloqueio de leitura/gravação permite que o gerente Leia, modifique e insira texto.</span><span class="sxs-lookup"><span data-stu-id="40bdc-126">A read/write lock enables the manager to read, modify, and insert text.</span></span> <span data-ttu-id="40bdc-127">Um bloqueio somente leitura é solicitado por meio da especificação \_ de TS LF \_ lido no *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="40bdc-127">A read-only lock is requested by specifying TS\_LF\_READ in *dwFlags*.</span></span> <span data-ttu-id="40bdc-128">Um bloqueio de leitura/gravação é solicitado pela especificação \_ de TS LF \_ ReadWrite no *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="40bdc-128">A read/write lock is requested by specifying TS\_LF\_READWRITE in *dwFlags*.</span></span>

## <a name="asynchronous-and-synchronous-requests"></a><span data-ttu-id="40bdc-129">Solicitações assíncronas e síncronas</span><span class="sxs-lookup"><span data-stu-id="40bdc-129">Asynchronous and Synchronous Requests</span></span>

<span data-ttu-id="40bdc-130">Uma solicitação de bloqueio pode ser síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="40bdc-130">A lock request can be either synchronous or asynchronous.</span></span> <span data-ttu-id="40bdc-131">O gerente solicita um bloqueio síncrono usando o sinalizador de \_ sincronização TS LF \_ no *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="40bdc-131">The manager requests a synchronous lock by using the TS\_LF\_SYNC flag in *dwFlags*.</span></span> <span data-ttu-id="40bdc-132">Se esse sinalizador não estiver presente, a solicitação será assíncrona.</span><span class="sxs-lookup"><span data-stu-id="40bdc-132">If this flag is not present, the request is asynchronous.</span></span>

## <a name="granting-the-lock"></a><span data-ttu-id="40bdc-133">Concedendo o bloqueio</span><span class="sxs-lookup"><span data-stu-id="40bdc-133">Granting the Lock</span></span>

<span data-ttu-id="40bdc-134">Quando **RequestLock** é chamado, o aplicativo deve determinar se o documento está bloqueado no momento.</span><span class="sxs-lookup"><span data-stu-id="40bdc-134">When **RequestLock** is called, the application must determine if the document is currently locked.</span></span> <span data-ttu-id="40bdc-135">Se o documento não estiver bloqueado e nenhum outro motivo para negar o bloqueio existir, o aplicativo deverá definir *phrSession* como s \_ OK e retornar s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40bdc-135">If the document is not locked, and no other reason to deny the lock exists, the application should set *phrSession* to S\_OK and return S\_OK.</span></span>

<span data-ttu-id="40bdc-136">Se o documento estiver bloqueado e a solicitação de bloqueio for síncrona, o aplicativo deverá definir *phrSession* como TS \_ e \_ síncrono e retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40bdc-136">If the document is locked and the lock request is synchronous, the application should set *phrSession* to TS\_E\_SYNCHRONOUS and return S\_OK.</span></span> <span data-ttu-id="40bdc-137">Isso indica que uma solicitação síncrona não pode ser concedida.</span><span class="sxs-lookup"><span data-stu-id="40bdc-137">This indicates that a synchronous request cannot be granted.</span></span>

<span data-ttu-id="40bdc-138">Se o documento estiver bloqueado e a solicitação de bloqueio for assíncrona, o aplicativo deverá enfileirar a solicitação, definir *phrSession* como TS \_ S \_ Async e retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40bdc-138">If the document is locked and the lock request is asynchronous, the application should queue the request, set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="40bdc-139">Quando o documento estiver disponível, o aplicativo deverá remover a solicitação da fila e chamar **OnLockGranted**.</span><span class="sxs-lookup"><span data-stu-id="40bdc-139">When the document becomes available, the application should remove the request from the queue and call **OnLockGranted**.</span></span> <span data-ttu-id="40bdc-140">Esse enfileiramento de solicitações de bloqueio é opcional; Há um cenário ao qual um aplicativo deve dar suporte.</span><span class="sxs-lookup"><span data-stu-id="40bdc-140">This queuing of lock requests is optional; there is one scenario that an application must support.</span></span> <span data-ttu-id="40bdc-141">Se o documento tiver um bloqueio somente leitura, a nova solicitação de bloqueio será leitura/gravação e a solicitação será assíncrona, o aplicativo terá se chamado em **OnLockGranted** , o que causou uma chamada reentrante para **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="40bdc-141">If the document has a read-only lock, the new lock request is read/write and the request is asynchronous, the application has called into **OnLockGranted** , which has caused a reentrant call to **RequestLock**.</span></span> <span data-ttu-id="40bdc-142">O aplicativo deve definir *phrSession* como TS \_ S \_ Async e retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40bdc-142">The application should set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="40bdc-143">Depois que a chamada para **OnLockGranted** retorna, o aplicativo deve processar a solicitação de atualização chamando **ONLOCKGRANTED** novamente com TS \_ LF \_ ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="40bdc-143">After the call to **OnLockGranted** returns, the application should process the upgrade request by calling **OnLockGranted** again with TS\_LF\_READWRITE.</span></span>

## <a name="lock-enforcement"></a><span data-ttu-id="40bdc-144">Imposição de bloqueio</span><span class="sxs-lookup"><span data-stu-id="40bdc-144">Lock Enforcement</span></span>

<span data-ttu-id="40bdc-145">O aplicativo deve garantir que o tipo apropriado de bloqueio exista antes de permitir o acesso ao documento.</span><span class="sxs-lookup"><span data-stu-id="40bdc-145">The application must ensure that the proper type of lock exists before allowing access to the document.</span></span> <span data-ttu-id="40bdc-146">Por exemplo, o aplicativo deve verificar se um documento tem pelo menos um bloqueio somente leitura antes de permitir [ITextStoreACP:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) ou [ITextStoreAnchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) para continuar.</span><span class="sxs-lookup"><span data-stu-id="40bdc-146">For example, the application should verify that a document has at least a read-only lock before allowing [ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) or [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) to proceed.</span></span> <span data-ttu-id="40bdc-147">Se o bloqueio apropriado não existir, o aplicativo deverá retornar TF \_ E \_ NOLOCK.</span><span class="sxs-lookup"><span data-stu-id="40bdc-147">If the proper lock does not exist, the application should return TF\_E\_NOLOCK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40bdc-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40bdc-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40bdc-149">Armazenamentos de texto</span><span class="sxs-lookup"><span data-stu-id="40bdc-149">Text Stores</span></span>](text-stores.md)
</dt> <dt>

[<span data-ttu-id="40bdc-150">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="40bdc-150">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="40bdc-151">ITextStoreACPSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="40bdc-151">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="40bdc-152">ITextStoreACP:: gettext</span><span class="sxs-lookup"><span data-stu-id="40bdc-152">ITextStoreACP::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[<span data-ttu-id="40bdc-153">ITextStoreAnchor:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="40bdc-153">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="40bdc-154">ITextStoreAnchorSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="40bdc-154">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="40bdc-155">ITextStoreAnchor:: gettext</span><span class="sxs-lookup"><span data-stu-id="40bdc-155">ITextStoreAnchor::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




