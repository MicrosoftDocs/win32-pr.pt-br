---
title: Para implementar mensagens de leitor no retorno de chamada OnStatus
description: Para implementar mensagens de leitor no retorno de chamada OnStatus
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- ASF (Advanced Systems Format), implementando mensagens de leitor
- ASF (formato de sistemas avançados), implementando mensagens de leitor
- ASF (Advanced Systems Format), retorno de chamada OnStatus
- ASF (formato de sistemas avançados), retorno de chamada OnStatus
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, implementando mensagens de leitor
- Método de retorno de chamada OnStatus, implementando mensagens de leitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007100"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a><span data-ttu-id="4dd11-111">Para implementar mensagens de leitor no retorno de chamada OnStatus</span><span class="sxs-lookup"><span data-stu-id="4dd11-111">To Implement Reader Messages in the OnStatus Callback</span></span>

<span data-ttu-id="4dd11-112">Para usar o leitor assíncrono para fornecer conteúdo de um arquivo ASF, você deve implementar um mínimo de dois métodos de retorno de chamada, [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) e [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="4dd11-112">To use the asynchronous reader to deliver content from an ASF file, you must implement a minimum of two callback methods, [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) and [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="4dd11-113">Esta seção descreve como implementar **IWMStatusCallback:: OnStatus** para receber e responder a mensagens de status enviadas pelo leitor.</span><span class="sxs-lookup"><span data-stu-id="4dd11-113">This section describes how to implement **IWMStatusCallback::OnStatus** to receive and respond to status messages sent by the reader.</span></span> <span data-ttu-id="4dd11-114">**OnStatus** é usado por outros objetos no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4dd11-114">**OnStatus** is used by other objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="4dd11-115">Para obter informações gerais sobre **OnStatus**, consulte [usando o retorno de chamada OnStatus](using-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="4dd11-115">For general information about **OnStatus**, see [Using the OnStatus Callback](using-the-onstatus-callback.md).</span></span>

<span data-ttu-id="4dd11-116">Ao usar o leitor assíncrono, você deve interceptar as seguintes mensagens em **IWMStatusCallback:: OnStatus**.</span><span class="sxs-lookup"><span data-stu-id="4dd11-116">When using the asynchronous reader, you must trap the following messages in **IWMStatusCallback::OnStatus**.</span></span>



| <span data-ttu-id="4dd11-117">Mensagem de status</span><span class="sxs-lookup"><span data-stu-id="4dd11-117">Status message</span></span> | <span data-ttu-id="4dd11-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dd11-118">Description</span></span>                                     |
|----------------|-------------------------------------------------|
| <span data-ttu-id="4dd11-119">WMT \_ aberto</span><span class="sxs-lookup"><span data-stu-id="4dd11-119">WMT\_OPENED</span></span>    | <span data-ttu-id="4dd11-120">Enviado quando as operações de abertura de arquivo são concluídas.</span><span class="sxs-lookup"><span data-stu-id="4dd11-120">Sent when file opening operations are complete.</span></span> |
| <span data-ttu-id="4dd11-121">WMT \_ fechado</span><span class="sxs-lookup"><span data-stu-id="4dd11-121">WMT\_CLOSED</span></span>    | <span data-ttu-id="4dd11-122">Enviado quando as operações de fechamento de arquivo são concluídas.</span><span class="sxs-lookup"><span data-stu-id="4dd11-122">Sent when file closing operations are complete.</span></span> |



 

<span data-ttu-id="4dd11-123">Você deve usar as mensagens de status listadas acima para controlar a execução do seu aplicativo de leitura.</span><span class="sxs-lookup"><span data-stu-id="4dd11-123">You should use the status messages listed above to control execution of your reading application.</span></span> <span data-ttu-id="4dd11-124">Por exemplo, você deve aguardar até receber a mensagem **\_ aberta WMT** para iniciar o leitor ou chamar outros métodos que exigem que o leitor tenha um arquivo pronto.</span><span class="sxs-lookup"><span data-stu-id="4dd11-124">For example, you must wait until receiving the **WMT\_OPENED** message to start the reader or call other methods that require the reader to have a file ready.</span></span> <span data-ttu-id="4dd11-125">Frequentemente, os aplicativos criados com o leitor assíncrono usam um evento para sinalizar a conclusão de chamadas assíncronas e prosseguir com o processamento.</span><span class="sxs-lookup"><span data-stu-id="4dd11-125">Frequently, applications built with the asynchronous reader use an event to signal the completion of asynchronous calls and proceed with processing.</span></span> <span data-ttu-id="4dd11-126">Para obter mais informações sobre como usar eventos para sinalizar a conclusão de operações, consulte [usando eventos com chamadas assíncronas](using-events-with-asynchronous-calls.md).</span><span class="sxs-lookup"><span data-stu-id="4dd11-126">For more information about using events for signaling completion of operations, see [Using Events with Asynchronous Calls](using-events-with-asynchronous-calls.md).</span></span>

<span data-ttu-id="4dd11-127">Muitas outras mensagens são enviadas ao **OnStatus** pelo objeto leitor para permitir que o aplicativo responda ao status das operações de leitura.</span><span class="sxs-lookup"><span data-stu-id="4dd11-127">Many other messages are sent to **OnStatus** by the reader object to enable the application to respond to the status of reading operations.</span></span> <span data-ttu-id="4dd11-128">Os valores de mensagem de status possíveis são definidos no tipo de enumeração [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="4dd11-128">The possible status message values are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dd11-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4dd11-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd11-130">**IWMStatusCallback:: OnStatus**</span><span class="sxs-lookup"><span data-stu-id="4dd11-130">**IWMStatusCallback::OnStatus**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[<span data-ttu-id="4dd11-131">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="4dd11-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="4dd11-132">**Usando o retorno de chamada OnStatus**</span><span class="sxs-lookup"><span data-stu-id="4dd11-132">**Using the OnStatus Callback**</span></span>](using-the-onstatus-callback.md)
</dt> </dl>

 

 




