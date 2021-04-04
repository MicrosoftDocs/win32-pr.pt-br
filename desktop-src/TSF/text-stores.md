---
title: Armazenamentos de texto
description: Armazenamentos de texto
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- TSF (estrutura de serviços de texto), armazenamentos de texto
- TSF (estrutura de serviços de texto), armazenamentos de texto
- Aplicativos habilitados para TSF, armazenamentos de texto
- armazenamentos de texto
- TSF (estrutura de serviços de texto), função de caractere do aplicativo (ACP)
- TSF (estrutura de serviços de texto), função de caractere do aplicativo (ACP)
- Aplicativos habilitados para TSF, posição de caracteres do aplicativo (ACP)
- Posição de caracteres do aplicativo (ACP)
- ACP (posição do caractere do aplicativo)
- TSF (estrutura de serviços de texto), âncoras
- TSF (estrutura de serviços de texto), âncoras
- Aplicativos habilitados para TSF, âncoras
- âncoras
- TSF (estrutura de serviços de texto), bloqueios de documentos
- TSF (estrutura de serviços de texto), bloqueios de documentos
- Aplicativos habilitados para TSF, bloqueios de documentos
- bloqueios de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007738"
---
# <a name="text-stores"></a><span data-ttu-id="69abb-120">Armazenamentos de texto</span><span class="sxs-lookup"><span data-stu-id="69abb-120">Text Stores</span></span>

## <a name="application-character-position-acp"></a><span data-ttu-id="69abb-121">Posição de caracteres do aplicativo (ACP)</span><span class="sxs-lookup"><span data-stu-id="69abb-121">Application Character Position (ACP)</span></span>

<span data-ttu-id="69abb-122">Um ACP é o local de um caractere, ou caracteres, em um fluxo de texto que é expresso como o número de caracteres desde o início do fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="69abb-122">An ACP is the location of a character, or characters, in a text stream that is expressed as the number of characters from the start of the text stream.</span></span> <span data-ttu-id="69abb-123">Como o modelo ACP é baseado em zero, o primeiro caractere em um fluxo de texto tem um ACP igual a zero.</span><span class="sxs-lookup"><span data-stu-id="69abb-123">Because the ACP model is zero-based, the first character in a text stream has an ACP of zero.</span></span> <span data-ttu-id="69abb-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="69abb-124">For example:</span></span>


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



<span data-ttu-id="69abb-125">Um armazenamento de texto implementa um objeto que dá suporte à interface [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , que permite que o fluxo de texto seja expresso em um ACP.</span><span class="sxs-lookup"><span data-stu-id="69abb-125">A text store implements an object that supports the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) interface, which enables the text stream to be expressed in an ACP.</span></span> <span data-ttu-id="69abb-126">Os métodos de interface **ITextStoreACP** usam o intervalo de ACP do fluxo de texto para modificar o texto.</span><span class="sxs-lookup"><span data-stu-id="69abb-126">The **ITextStoreACP** interface methods use the ACP range of the text stream to modify the text.</span></span>

## <a name="anchor-based-applications"></a><span data-ttu-id="69abb-127">Anchor-Based aplicativos</span><span class="sxs-lookup"><span data-stu-id="69abb-127">Anchor-Based Applications</span></span>

<span data-ttu-id="69abb-128">O Gerenciador usa os métodos baseados em ACP nativamente para manipular o texto.</span><span class="sxs-lookup"><span data-stu-id="69abb-128">The manager uses the ACP-based methods natively to manipulate text.</span></span> <span data-ttu-id="69abb-129">No entanto, uma abordagem baseada em âncora está disponível para clientes do [Microsoft acessibilidade ativa](../winauto/microsoft-active-accessibility.md) que dão suporte a [âncoras](ranges.md), no qual o gerente usa métodos [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) e [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) para encapsular os métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .</span><span class="sxs-lookup"><span data-stu-id="69abb-129">However, an anchor-based approach is available for [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) clients that support [anchors](ranges.md), whereby the manager uses [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) and [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) methods to wrap the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) methods.</span></span>

## <a name="document-access-control"></a><span data-ttu-id="69abb-130">Controle de acesso a documentos</span><span class="sxs-lookup"><span data-stu-id="69abb-130">Document Access Control</span></span>

<span data-ttu-id="69abb-131">O armazenamento de texto controla o acesso ao fluxo de texto usando [bloqueios de documento](document-locks.md).</span><span class="sxs-lookup"><span data-stu-id="69abb-131">The text store controls access to the text stream by using [document locks](document-locks.md).</span></span> <span data-ttu-id="69abb-132">Para ler ou modificar o armazenamento de texto, o gerente deve primeiro instalar um coletor de aviso que dê suporte à interface [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) chamando o método [ITextStoreACP:: AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) e passando um ponteiro para um coletor de aviso.</span><span class="sxs-lookup"><span data-stu-id="69abb-132">To read or modify the text store, the manager must first install an advise sink that supports the [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) interface by calling the [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) method and passing a pointer to an advise sink.</span></span> <span data-ttu-id="69abb-133">O coletor de aviso permite que o gerente obtenha bloqueios de documentos no armazenamento de texto e receba notificações quando o armazenamento de texto for modificado por algo diferente do gerente, como entrada do usuário por meio do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69abb-133">The advise sink enables the manager to obtain a document locks on the text store and receive notifications when the text store is modified by something other than the manager, such as user input through the application.</span></span> <span data-ttu-id="69abb-134">Os coletores de aviso são discutidos posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="69abb-134">Advise sinks are discussed later in this topic.</span></span>

## <a name="how-to-initialize-the-text-store"></a><span data-ttu-id="69abb-135">Como inicializar o armazenamento de texto</span><span class="sxs-lookup"><span data-stu-id="69abb-135">How To Initialize the Text Store</span></span>

<span data-ttu-id="69abb-136">Um aplicativo Inicializa um repositório de texto concluindo as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="69abb-136">An application initializes a text store by completing the following steps:</span></span>

1.  <span data-ttu-id="69abb-137">Crie um objeto do Gerenciador de threads baseado na interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) chamando a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com um ponteiro para um objeto do Gerenciador de threads.</span><span class="sxs-lookup"><span data-stu-id="69abb-137">Create a thread manager object based on the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function with a pointer to a thread manager object.</span></span> <span data-ttu-id="69abb-138">Veja a seguir um exemplo de código de implementação de um objeto do Gerenciador de threads.</span><span class="sxs-lookup"><span data-stu-id="69abb-138">The following is a code example of implementing a thread manager object.</span></span>
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  <span data-ttu-id="69abb-139">Ative o objeto Gerenciador de threads chamando o método [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) .</span><span class="sxs-lookup"><span data-stu-id="69abb-139">Activate the thread manager object by calling the [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) method.</span></span> <span data-ttu-id="69abb-140">Esse método fornece um ponteiro para um [identificador de cliente](tfclientid.md) usado para criar um objeto de contexto.</span><span class="sxs-lookup"><span data-stu-id="69abb-140">This method supplies a pointer to a [client identifier](tfclientid.md) used to create a context object.</span></span> <span data-ttu-id="69abb-141">O Gerenciador de threads é usado para implementar um objeto do Gerenciador de documentos.</span><span class="sxs-lookup"><span data-stu-id="69abb-141">The thread manager is used to implement a document manager object.</span></span>
3.  <span data-ttu-id="69abb-142">Crie um objeto do Gerenciador de documentos com base na interface [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) chamando o método [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) com um ponteiro para o objeto do Gerenciador de documentos.</span><span class="sxs-lookup"><span data-stu-id="69abb-142">Create a document manager object based on the [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) interface by calling the [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) method with a pointer to the document manager object.</span></span> <span data-ttu-id="69abb-143">O objeto Gerenciador de documentos é usado para implementar um objeto de contexto que é o armazenamento de texto.</span><span class="sxs-lookup"><span data-stu-id="69abb-143">The document manager object is used to implement a context object that is the text store.</span></span>
4.  <span data-ttu-id="69abb-144">Crie um objeto de contexto do Gerenciador de documentos chamando o método [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) com o ponteiro para o objeto de armazenamento de texto e um ponteiro para o identificador do cliente de ativar o Gerenciador de threads.</span><span class="sxs-lookup"><span data-stu-id="69abb-144">Create a context object from the document manager by calling the [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) method with the pointer to the text store object and a pointer to the client identifier from activating the thread manager.</span></span> <span data-ttu-id="69abb-145">Veja a seguir um exemplo de criação de um objeto de contexto:</span><span class="sxs-lookup"><span data-stu-id="69abb-145">The following is an example of creating a context object:</span></span>
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  <span data-ttu-id="69abb-146">Envie por push o objeto de contexto para a pilha com o método [ITfDocumentMgr::P USH](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) .</span><span class="sxs-lookup"><span data-stu-id="69abb-146">Push the context object onto the stack with the [ITfDocumentMgr::Push](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) method.</span></span> <span data-ttu-id="69abb-147">Veja a seguir um exemplo de envio do objeto de contexto para a pilha:</span><span class="sxs-lookup"><span data-stu-id="69abb-147">The following is an example of pushing the context object onto the stack:</span></span>
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a><span data-ttu-id="69abb-148">Como modificar o armazenamento de texto</span><span class="sxs-lookup"><span data-stu-id="69abb-148">How To Modify the Text Store</span></span>

<span data-ttu-id="69abb-149">O método **ITfDocumentMgr::P USH** chama **ITextStoreACP:: AdviseSink** com um ponteiro para a interface do coletor de aviso para instalar um novo coletor de aviso ou modificar um coletor de aviso existente.</span><span class="sxs-lookup"><span data-stu-id="69abb-149">The **ITfDocumentMgr::Push** method calls **ITextStoreACP::AdviseSink** with a pointer to the advise sink interface to install a new advise sink or modify an existing advise sink.</span></span> <span data-ttu-id="69abb-150">O coletor de aviso recebe notificações quando o armazenamento de texto é modificado por algo diferente do gerente, como entrada do usuário para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69abb-150">The advise sink receives notifications when the text store is modified by something other than the manager, such as user input to the application.</span></span> <span data-ttu-id="69abb-151">Os aplicativos devem chamar o método [ITfThreadMgrEventSink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) quando o método de entrada obtiver o foco.</span><span class="sxs-lookup"><span data-stu-id="69abb-151">Applications must call the [ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) method when the input method obtains the focus.</span></span> <span data-ttu-id="69abb-152">Outras notificações para o Gerenciador de thread são fornecidas chamando para os métodos de interface **ITextStoreACPSink** apropriados.</span><span class="sxs-lookup"><span data-stu-id="69abb-152">Other notifications to the thread manager are provided by calling to the appropriate **ITextStoreACPSink** interface methods.</span></span>

<span data-ttu-id="69abb-153">No entanto, os aplicativos não devem chamar os métodos de interface **ITextStoreACPSink** em resposta aos métodos de interface **ITextStoreACP** .</span><span class="sxs-lookup"><span data-stu-id="69abb-153">However, applications should not call the **ITextStoreACPSink** interface methods in response to **ITextStoreACP** interface methods.</span></span> <span data-ttu-id="69abb-154">Os aplicativos só devem chamar métodos de interface **ITextStoreACPSink** quando o armazenamento de texto é modificado por algo diferente do gerente.</span><span class="sxs-lookup"><span data-stu-id="69abb-154">Applications should only call **ITextStoreACPSink** interface methods when the text store is modified by something other than the manager.</span></span>

<span data-ttu-id="69abb-155">O conteúdo do repositório de texto pode ser modificado com um estado de entrada temporário chamado de [composição](compositions.md).</span><span class="sxs-lookup"><span data-stu-id="69abb-155">The contents of the text store can be modified with a temporary input state called a [composition](compositions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69abb-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69abb-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69abb-157">Âncoras</span><span class="sxs-lookup"><span data-stu-id="69abb-157">Anchors</span></span>](ranges.md)
</dt> <dt>

[<span data-ttu-id="69abb-158">Composições</span><span class="sxs-lookup"><span data-stu-id="69abb-158">Compositions</span></span>](compositions.md)
</dt> <dt>

[<span data-ttu-id="69abb-159">Bloqueios de documentos</span><span class="sxs-lookup"><span data-stu-id="69abb-159">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="69abb-160">ITextStoreACPSink</span><span class="sxs-lookup"><span data-stu-id="69abb-160">ITextStoreACPSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[<span data-ttu-id="69abb-161">ITextStoreACP</span><span class="sxs-lookup"><span data-stu-id="69abb-161">ITextStoreACP</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="69abb-162">ITextStoreAnchor</span><span class="sxs-lookup"><span data-stu-id="69abb-162">ITextStoreAnchor</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[<span data-ttu-id="69abb-163">ITextStoreAnchorSink</span><span class="sxs-lookup"><span data-stu-id="69abb-163">ITextStoreAnchorSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[<span data-ttu-id="69abb-164">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="69abb-164">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="69abb-165">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="69abb-165">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="69abb-166">ITfThreadMgrEventSink:: OnSetFocus</span><span class="sxs-lookup"><span data-stu-id="69abb-166">ITfThreadMgrEventSink::OnSetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[<span data-ttu-id="69abb-167">TfClientId</span><span class="sxs-lookup"><span data-stu-id="69abb-167">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="69abb-168">Acessibilidade Ativa da Microsoft</span><span class="sxs-lookup"><span data-stu-id="69abb-168">Microsoft Active Accessibility</span></span>](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 