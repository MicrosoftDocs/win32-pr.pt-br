---
title: Enviando dados ASF para um ponto de publicação
description: Enviando dados ASF para um ponto de publicação
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- SDK do Windows Media Format, enviando dados do ASF
- SDK do Windows Media Format, pontos de publicação
- ASF (Advanced Systems Format), enviando dados
- ASF (formato de sistemas avançados), enviando dados
- ASF (Advanced Systems Format), pontos de publicação
- ASF (formato de sistemas avançados), pontos de publicação
- pontos de publicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f38f4d24a458681c4b0dc4ee6d1a73563bdd2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640305"
---
# <a name="sending-asf-data-to-a-publishing-point"></a><span data-ttu-id="ee45b-110">Enviando dados ASF para um ponto de publicação</span><span class="sxs-lookup"><span data-stu-id="ee45b-110">Sending ASF Data to a Publishing Point</span></span>

<span data-ttu-id="ee45b-111">Você pode usar o Windows Media Format SDK para enviar dados ASF para um ponto de publicação em um Windows Media Server.</span><span class="sxs-lookup"><span data-stu-id="ee45b-111">You can use the Windows Media Format SDK to push ASF data to a publishing point on a Windows Media server.</span></span> <span data-ttu-id="ee45b-112">Em seguida, o servidor transmite os dados desse ponto de publicação.</span><span class="sxs-lookup"><span data-stu-id="ee45b-112">The server then broadcasts the data from that publishing point.</span></span> <span data-ttu-id="ee45b-113">Esse cenário será útil se você estiver capturando ou recodificando o conteúdo em um computador e desejar distribuir o conteúdo de outro computador (ou vários computadores).</span><span class="sxs-lookup"><span data-stu-id="ee45b-113">This scenario is useful if you are capturing or re-encoding content on one computer, and wish to distribute the content from another computer (or several computers).</span></span> <span data-ttu-id="ee45b-114">Ele também será útil se você precisar mover o conteúdo de um computador dentro de um firewall para um servidor de mídia do Windows fora do firewall, pois a distribuição por push usa o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="ee45b-114">It is also useful if you need to move content from a computer inside a firewall to a Windows Media server outside the firewall, because push distribution uses the HTTP protocol.</span></span>

> [!Note]  
> <span data-ttu-id="ee45b-115">Um *ponto de publicação* funciona basicamente como um redirecionador.</span><span class="sxs-lookup"><span data-stu-id="ee45b-115">A *publishing point* acts essentially like a redirector.</span></span> <span data-ttu-id="ee45b-116">O cliente especifica o ponto de publicação na URL (por exemplo, mms://MyServer/MyPublishingPoint) e o servidor converte isso em uma solicitação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ee45b-116">The client specifies the publishing point in the URL (for example, mms://MyServer/MyPublishingPoint) and the server translates this into a request for content.</span></span>

 

<span data-ttu-id="ee45b-117">Para enviar dados por push ao ponto de publicação, anexe o objeto de coletor de push ao objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="ee45b-117">To push data to the publishing point, attach the push sink object to the writer object.</span></span> <span data-ttu-id="ee45b-118">O coletor de Push é usado para abrir a conexão com o servidor e gerenciar a sessão de push.</span><span class="sxs-lookup"><span data-stu-id="ee45b-118">The push sink is used to open the connection to the server and manage the push session.</span></span> <span data-ttu-id="ee45b-119">O objeto gravador manipula todos os outros aspectos da criação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ee45b-119">The writer object handles all the other aspects of creating the file.</span></span>

<span data-ttu-id="ee45b-120">Execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ee45b-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="ee45b-121">Crie o objeto gravador chamando a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) , que retorna um ponteiro [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) .</span><span class="sxs-lookup"><span data-stu-id="ee45b-121">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function, which returns an [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) pointer.</span></span>
2.  <span data-ttu-id="ee45b-122">Crie o objeto de coletor de push chamando a função [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) , que retorna um ponteiro [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) .</span><span class="sxs-lookup"><span data-stu-id="ee45b-122">Create the push sink object by calling the [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) function, which returns an [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) pointer.</span></span>
3.  <span data-ttu-id="ee45b-123">Anexe o coletor de rede ao gravador chamando [**IWMWriterAdvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) no gravador, com um ponteiro para a interface **IWMWriterPushSink** do coletor de rede.</span><span class="sxs-lookup"><span data-stu-id="ee45b-123">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterPushSink** interface.</span></span>
4.  <span data-ttu-id="ee45b-124">Conecte-se ao servidor chamando [**IWMWriterPushSink:: Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).</span><span class="sxs-lookup"><span data-stu-id="ee45b-124">Connect to the server by calling [**IWMWriterPushSink::Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).</span></span>
5.  <span data-ttu-id="ee45b-125">Grave o fluxo.</span><span class="sxs-lookup"><span data-stu-id="ee45b-125">Write the stream.</span></span> <span data-ttu-id="ee45b-126">Esta etapa envolve a definição do perfil no objeto do gravador, o envio de amostras ao gravador e, possivelmente, outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="ee45b-126">This step involves setting the profile on the writer object, sending samples to the writer, and possibly other tasks.</span></span> <span data-ttu-id="ee45b-127">Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="ee45b-127">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span> <span data-ttu-id="ee45b-128">Tarefas adicionais podem incluir atributos de metadados de configuração (conforme descrito em [trabalhando com metadados](working-with-metadata.md)) ou configurar o DRM ao vivo no fluxo (conforme descrito em [habilitando o suporte a DRM](enabling-drm-support.md)).</span><span class="sxs-lookup"><span data-stu-id="ee45b-128">Additional tasks might include setting metadata attributes (as described in [Working with Metadata](working-with-metadata.md)) or setting live-DRM on the stream (as described in [Enabling DRM Support](enabling-drm-support.md)).</span></span> <span data-ttu-id="ee45b-129">Essas tarefas são executadas exatamente como são para gravação de arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ee45b-129">These tasks are performed exactly as they are for ASF file writing.</span></span>
6.  <span data-ttu-id="ee45b-130">Depois de terminar de escrever, chame [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) no gravador para desanexar o objeto do coletor de push.</span><span class="sxs-lookup"><span data-stu-id="ee45b-130">After you are done writing, call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the push sink object.</span></span>
7.  <span data-ttu-id="ee45b-131">Chame [**IWMWriterPushSink:: EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) no coletor de push para encerrar a sessão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="ee45b-131">Call [**IWMWriterPushSink::EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) on the push sink to end the session with the server.</span></span>

<span data-ttu-id="ee45b-132">Essas etapas são ilustradas no aplicativo de exemplo WMVNetWrite.</span><span class="sxs-lookup"><span data-stu-id="ee45b-132">These steps are illustrated in the WMVNetWrite sample application.</span></span>

> [!Note]  
> <span data-ttu-id="ee45b-133">Se você estiver enviando um arquivo somente de vídeo de taxa de bits muito baixa, ele poderá não começar a ser reproduzido no ponto de publicação por vários segundos.</span><span class="sxs-lookup"><span data-stu-id="ee45b-133">If you are sending a very-low-bit-rate video-only file, it might not start playing on the publishing point for several seconds.</span></span> <span data-ttu-id="ee45b-134">Isso pode acontecer em vários casos, por exemplo, quando um único pacote contém muitos quadros de vídeo pequenos e sem áudio, ou quando há uma lacuna de tempo longa entre o primeiro pacote e o segundo pacote em um arquivo somente de vídeo de taxa de bits baixa.</span><span class="sxs-lookup"><span data-stu-id="ee45b-134">This can happen in various cases, for example when a single packet contains many small video frames and no audio, or when there is a long time gap between the first packet and the second packet in a low-bit-rate video-only file.</span></span> <span data-ttu-id="ee45b-135">Para evitar esse problema, insira um fluxo de áudio silencioso no arquivo.</span><span class="sxs-lookup"><span data-stu-id="ee45b-135">To avoid this problem, insert a silent audio stream into the file.</span></span>

 

## <a name="authentication"></a><span data-ttu-id="ee45b-136">Autenticação</span><span class="sxs-lookup"><span data-stu-id="ee45b-136">Authentication</span></span>

<span data-ttu-id="ee45b-137">A autenticação para o servidor é manipulada automaticamente pelo objeto de coletor de push.</span><span class="sxs-lookup"><span data-stu-id="ee45b-137">Authentication to the server is automatically handled by the push sink object.</span></span> <span data-ttu-id="ee45b-138">No entanto, o aplicativo pode precisar fornecer credenciais.</span><span class="sxs-lookup"><span data-stu-id="ee45b-138">However, the application may need to supply credentials.</span></span> <span data-ttu-id="ee45b-139">Isso é feito por meio da interface de retorno de chamada do **IWMCredentialCallback** , da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ee45b-139">This is done through the **IWMCredentialCallback** callback interface, as follows:</span></span>

1.  <span data-ttu-id="ee45b-140">Implemente a interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) e [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee45b-140">Implement the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) and [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) interface in your application.</span></span>
2.  <span data-ttu-id="ee45b-141">Consulte o objeto de coletor de push para a interface [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="ee45b-141">Query the push sink object for the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span>
3.  <span data-ttu-id="ee45b-142">Chame [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) com um ponteiro para a interface **IWMStatusCallback** do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee45b-142">Call [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) with a pointer to your application's **IWMStatusCallback** interface.</span></span>
4.  <span data-ttu-id="ee45b-143">Se o coletor de push precisar obter credenciais do aplicativo, ele consultará o ponteiro **IWMStatusCallback** para a interface **IWMCredentialCallback** e chamará [**IWMCredentialCallback:: AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials).</span><span class="sxs-lookup"><span data-stu-id="ee45b-143">If the push sink needs to get credentials from the application, it queries the **IWMStatusCallback** pointer for the **IWMCredentialCallback** interface and calls [**IWMCredentialCallback::AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials).</span></span> <span data-ttu-id="ee45b-144">Para obter informações sobre esse método, consulte [autenticação](authentication.md).</span><span class="sxs-lookup"><span data-stu-id="ee45b-144">For information about this method, see [Authentication](authentication.md).</span></span>
5.  <span data-ttu-id="ee45b-145">Quando terminar, chame [**IWMRegisterCallback:: Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) para parar de obter notificações de eventos do coletor de push.</span><span class="sxs-lookup"><span data-stu-id="ee45b-145">When you are done, call [**IWMRegisterCallback::Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) to stop getting event notifications from the push sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee45b-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee45b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee45b-147">**Enviando dados ASF por meio de uma rede**</span><span class="sxs-lookup"><span data-stu-id="ee45b-147">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="ee45b-148">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="ee45b-148">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> <dt>

[<span data-ttu-id="ee45b-149">**Objeto de coletor de push do gravador**</span><span class="sxs-lookup"><span data-stu-id="ee45b-149">**Writer Push Sink Object**</span></span>](writer-push-sink-object.md)
</dt> </dl>

 

 




