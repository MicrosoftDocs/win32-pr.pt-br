---
description: Este tópico descreve como usar a API de impressão XPS para imprimir de um aplicativo do Windows.
ms.assetid: 3d7ab169-412c-434f-a865-4da4af370eaf
title: 'Como: imprimir com a API de impressão XPS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4be5f083fb31eccaf2dc4b555435bd15a7fb45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829598"
---
# <a name="how-to-print-with-the-xps-print-api"></a><span data-ttu-id="d6b16-103">Como: imprimir com a API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="d6b16-103">How To: Print with the XPS Print API</span></span>

<span data-ttu-id="d6b16-104">Este tópico descreve como usar a [API de impressão XPS](xpsprint-api.md) para imprimir de um aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6b16-104">This topic describes how to use the [XPS Print API](xpsprint-api.md) to print from a Windows application.</span></span>

<span data-ttu-id="d6b16-105">A [API de impressão XPS](xpsprint-api.md) permite que aplicativos nativos do Windows imprimam documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="d6b16-105">The [XPS Print API](xpsprint-api.md) enables native Windows applications to print XPS documents.</span></span> <span data-ttu-id="d6b16-106">Um aplicativo pode criar um documento XPS usando a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d6b16-106">An application can create an XPS document by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="d6b16-107">O tópico da ajuda de [tarefas comuns de programação de documentos XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)) descreve como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="d6b16-107">The [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)) help topic describes how to do this.</span></span> <span data-ttu-id="d6b16-108">Depois que um documento XPS tiver sido criado, o aplicativo poderá usar a API de impressão XPS para imprimi-lo.</span><span class="sxs-lookup"><span data-stu-id="d6b16-108">Once an XPS document has been created, the application can use the XPS Print API to print it.</span></span>

<span data-ttu-id="d6b16-109">Usar a [API de impressão XPS](xpsprint-api.md) para imprimir um documento de um aplicativo envolve as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6b16-109">Using the [XPS Print API](xpsprint-api.md) to print a document from an application involves the following steps.</span></span>

-   [<span data-ttu-id="d6b16-110">Inicializar interface COM</span><span class="sxs-lookup"><span data-stu-id="d6b16-110">Initialize COM Interface</span></span>](#initialize-com-interface)
-   [<span data-ttu-id="d6b16-111">Criar um evento de conclusão</span><span class="sxs-lookup"><span data-stu-id="d6b16-111">Create a Completion Event</span></span>](#create-a-completion-event)
-   [<span data-ttu-id="d6b16-112">Iniciar um trabalho de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="d6b16-112">Start an XPS Print Job</span></span>](#start-an-xps-print-job)
-   [<span data-ttu-id="d6b16-113">Criar uma interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="d6b16-113">Create an IXpsOMPackageWriter Interface</span></span>](#create-an-ixpsompackagewriter-interface)
-   [<span data-ttu-id="d6b16-114">Fechar a interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="d6b16-114">Close the IXpsOMPackageWriter Interface</span></span>](#close-the-ixpsompackagewriter-interface)
-   [<span data-ttu-id="d6b16-115">Fechar o fluxo do trabalho de impressão</span><span class="sxs-lookup"><span data-stu-id="d6b16-115">Close the Print Job Stream</span></span>](#close-the-print-job-stream)
-   [<span data-ttu-id="d6b16-116">Aguardar o evento de conclusão</span><span class="sxs-lookup"><span data-stu-id="d6b16-116">Wait for the Completion Event</span></span>](#wait-for-the-completion-event)
-   [<span data-ttu-id="d6b16-117">Liberar recursos</span><span class="sxs-lookup"><span data-stu-id="d6b16-117">Release Resources</span></span>](#release-resources)

<span data-ttu-id="d6b16-118">A [API de impressão XPS](xpsprint-api.md) requer um documento XPS para imprimir.</span><span class="sxs-lookup"><span data-stu-id="d6b16-118">The [XPS Print API](xpsprint-api.md) requires an XPS document to print.</span></span> <span data-ttu-id="d6b16-119">No exemplo a seguir, o documento XPS é criado, pois ele é enviado para a impressora pela API de impressão XPS.</span><span class="sxs-lookup"><span data-stu-id="d6b16-119">In the following example, the XPS document is created as it is sent to the printer by the XPS Print API.</span></span> <span data-ttu-id="d6b16-120">Também é possível criar um documento XPS sem enviá-lo para uma impressora usando a API de [documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e mantendo-o como um om XPS ou salvando o OM XPS como um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="d6b16-120">It is also possible to create an XPS document without sending it to a printer by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and maintaining it as an XPS OM or by saving the XPS OM as an XPS document.</span></span> <span data-ttu-id="d6b16-121">Para obter mais informações sobre como usar um OM XPS, consulte a API de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="d6b16-121">For more information about using an XPS OM, see the XPS Document API.</span></span>

### <a name="initialize-com-interface"></a><span data-ttu-id="d6b16-122">Inicializar interface COM</span><span class="sxs-lookup"><span data-stu-id="d6b16-122">Initialize COM Interface</span></span>

<span data-ttu-id="d6b16-123">Inicialize a interface COM, se o aplicativo ainda não tiver feito isso.</span><span class="sxs-lookup"><span data-stu-id="d6b16-123">Initialize the COM interface, if the application has not already done so.</span></span>


```C++
    // Initialize the COM interface, if the application has not 
    //  already done so.
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        fwprintf(stderr, 
            L"ERROR: CoInitializeEx failed with HRESULT 0x%X\n", hr);
        return 1;
    }
```



### <a name="create-a-completion-event"></a><span data-ttu-id="d6b16-124">Criar um evento de conclusão</span><span class="sxs-lookup"><span data-stu-id="d6b16-124">Create a Completion Event</span></span>

<span data-ttu-id="d6b16-125">Crie um evento de conclusão, que a [API de impressão XPS](xpsprint-api.md) usa para notificar o aplicativo quando o spooler de impressão tiver recebido o documento inteiro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6b16-125">Create a completion event, which the [XPS Print API](xpsprint-api.md) uses to notify the application when the print spooler has received the entire document from the application.</span></span> <span data-ttu-id="d6b16-126">A API de impressão XPS também dá suporte a um evento de progresso para que um aplicativo possa saber sobre outras atividades de spooling.</span><span class="sxs-lookup"><span data-stu-id="d6b16-126">The XPS Print API also supports a progress event so an application can know about other spooling activity.</span></span>


```C++
        // Create the completion event
        completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
        if (!completionEvent)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(stderr, 
                L"ERROR: Could not create completion event: %08X\n", hr);
        }
```



### <a name="start-an-xps-print-job"></a><span data-ttu-id="d6b16-127">Iniciar um trabalho de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="d6b16-127">Start an XPS Print Job</span></span>

<span data-ttu-id="d6b16-128">Inicie um trabalho de impressão XPS chamando [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="d6b16-128">Start an XPS print job by calling [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span> <span data-ttu-id="d6b16-129">**StartXpsPrintJob** retorna um fluxo no qual o aplicativo enviará o documento a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="d6b16-129">**StartXpsPrintJob** returns a stream into which the application will send the document to be printed.</span></span>


```C++
        // Start an XPS Print Job
        if (FAILED(hr = StartXpsPrintJob(
                    printerName,
                    NULL,
                    NULL,
                    NULL,
                    completionEvent,
                    NULL,
                    0,
                    &job,
                    &jobStream,
                    NULL
                    )))
        {
            fwprintf(stderr, 
                L"ERROR: Could not start XPS print job: %08X\n", hr);
        }
```



### <a name="create-an-ixpsompackagewriter-interface"></a><span data-ttu-id="d6b16-130">Criar uma interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="d6b16-130">Create an IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="d6b16-131">Crie uma interface [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) chamando [**IXpsOMObjectFactory:: CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) no fluxo retornado por [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="d6b16-131">Create an [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface by calling [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) on the stream returned by [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span>


```C++
    // Create an XPS OM Object Factory. If one has already been 
    //  created by the application, a new one is not necessary.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory), 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&xpsFactory))))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create XPS OM Object Factory: %08X\n", 
                hr);
        }
    }
    // Create the Part URI for the Fixed Document Sequence. The
    //  Fixed Document Sequence is the top-level element in the
    //  package hierarchy of objects. There is one Fixed Document
    //  Sequence in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name used in this example is the part name
    //  used by convention.
    //
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/FixedDocumentSequence.fdseq", 
                    &partUri)))
        {
            fwprintf(stderr, 
                L"ERROR: Could not create part URI: %08X\n", hr);
        }
    }

    // Create the package writer on the print job stream.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePackageWriterOnStream(
                    jobStream,
                    TRUE,
                    XPS_INTERLEAVING_ON,
                    partUri,
                    NULL,
                    NULL,
                    NULL,
                    NULL,
                    &packageWriter
                    )
                )
           )
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create package writer: 0x%X\n", 
                hr);
        }
    }

    // Release the part URI interface.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



<span data-ttu-id="d6b16-132">Para cada documento deste trabalho de impressão, inicie um novo documento e, em seguida, adicione páginas a esse documento.</span><span class="sxs-lookup"><span data-stu-id="d6b16-132">For each document in this print job, start a new document and then add pages to that document.</span></span>

### <a name="start-a-new-document"></a><span data-ttu-id="d6b16-133">Iniciar um novo documento</span><span class="sxs-lookup"><span data-stu-id="d6b16-133">Start a New Document</span></span>

<span data-ttu-id="d6b16-134">Inicie um novo documento no gravador de pacote chamando [**IXpsOMPackageWriter:: StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span><span class="sxs-lookup"><span data-stu-id="d6b16-134">Start a new document in the package writer by calling [**IXpsOMPackageWriter::StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span></span> <span data-ttu-id="d6b16-135">Se um documento estiver aberto quando esse método for chamado, ele será fechado e um novo documento será aberto.</span><span class="sxs-lookup"><span data-stu-id="d6b16-135">If a document is open when this method is called, it is closed and a new document is opened.</span></span>


```C++
    // Create the Part URI for the Fixed Document. The
    //  Fixed Document part contains the pages of the document. 
    //  There can be one or more Fixed Documents in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name format used in this example is the format 
    //  used by convention. The number "1" in this example must be 
    //  changed for each document in the package. For example, 1 
    //  for the first document, 2 for the second, and so on.
    //

    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/Documents/1/FixedDocument.fdoc", 
                    &partUri)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create part URI: %08X\n", 
                hr);
        }
    }

    // Start the new document.
    //
    //  If there was already a document started in this page,
    //  this call will close it and start a new one.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->StartNewDocument(
                    partUri, 
                    NULL, 
                    NULL, 
                    NULL,
                    NULL)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not start new document: 0x%X\n", 
                hr);
        }
    }
    
    // Release the part URI interface
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



### <a name="add-a-page"></a><span data-ttu-id="d6b16-136">Adicionar uma página</span><span class="sxs-lookup"><span data-stu-id="d6b16-136">Add a Page</span></span>

<span data-ttu-id="d6b16-137">Chame [**IXpsOMPackageWriter:: AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) para gravar cada uma das páginas do documento do aplicativo no novo documento no gravador do pacote.</span><span class="sxs-lookup"><span data-stu-id="d6b16-137">Call [**IXpsOMPackageWriter::AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) to write each of the document's pages from the application to the new document in the package writer.</span></span>

> [!Note]  
> <span data-ttu-id="d6b16-138">Supõe-se que o aplicativo criou a página antes desta etapa.</span><span class="sxs-lookup"><span data-stu-id="d6b16-138">The application is assumed to have created the page prior to this step.</span></span> <span data-ttu-id="d6b16-139">Para obter mais informações sobre como criar páginas de documentos e adicionar conteúdo a elas, consulte as [tarefas comuns de programação de documento XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d6b16-139">For more information about creating document pages and adding content to them, see the [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        // Add the current page to the document.
        if (FAILED(hr = packageWriter->AddPage(
                    xpsPage,
                    &pageSize,
                    NULL,
                    NULL,
                    NULL,
                    NULL
                    )))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not add page to document: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-ixpsompackagewriter-interface"></a><span data-ttu-id="d6b16-140">Fechar a interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="d6b16-140">Close the IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="d6b16-141">Depois que todos os documentos tiverem sido gravados para esse trabalho de impressão, chame [**IXpsOMPackageWriter:: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) para fechar o pacote.</span><span class="sxs-lookup"><span data-stu-id="d6b16-141">After all the documents have been written for this print job, call [**IXpsOMPackageWriter::Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) to close the package.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->Close()))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not close package writer: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-print-job-stream"></a><span data-ttu-id="d6b16-142">Fechar o fluxo do trabalho de impressão</span><span class="sxs-lookup"><span data-stu-id="d6b16-142">Close the Print Job Stream</span></span>

<span data-ttu-id="d6b16-143">Feche o fluxo do trabalho de impressão chamando [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), que informa ao spooler de impressão que todo o trabalho de impressão foi enviado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6b16-143">Close the print job stream by calling [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), which tells the print spooler that the entire print job has been sent by the application.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = jobStream->Close()))
        {
            fwprintf(
                stderr,
                L"ERROR: Could not close job stream: %08X\n",
                hr);
        }
    }
    else
    {
        // Only cancel the job if we succeeded in creating a job.
        if (job)
        {
            // Tell the XPS Print API that we're giving up.  
            //  Don't overwrite hr with the return from this function.
            job->Cancel();
        }
    }
```



### <a name="wait-for-the-completion-event"></a><span data-ttu-id="d6b16-144">Aguardar o evento de conclusão</span><span class="sxs-lookup"><span data-stu-id="d6b16-144">Wait for the Completion Event</span></span>

<span data-ttu-id="d6b16-145">Aguarde o evento de conclusão do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="d6b16-145">Wait for the print job's completion event.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        wprintf(L"Waiting for job completion...\n");

        if (WaitForSingleObject(completionEvent, INFINITE) != 
                                                    WAIT_OBJECT_0)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(
                stderr, 
                L"ERROR: Wait for completion event failed: %08X\n", 
                hr);
        }
    }
```



<span data-ttu-id="d6b16-146">Depois que o evento de conclusão for sinalizado, chame [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) para obter o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d6b16-146">After the completion event is signaled, call [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) to get the job status.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = job->GetJobStatus(&jobStatus)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not get job status: %08X\n", 
                hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        switch (jobStatus.completion)
        {
            case XPS_JOB_COMPLETED:
                break;
            case XPS_JOB_CANCELLED:
                fwprintf(stderr, L"ERROR: job was cancelled\n");
                hr = E_FAIL;
                break;
            case XPS_JOB_FAILED:
                fwprintf(
                    stderr, 
                    L"ERROR: Print job failed: %08X\n", 
                    jobStatus.jobStatus);
                hr = E_FAIL;
                break;
            default:
                fwprintf(stderr, L"ERROR: unexpected failure\n");
                hr = E_UNEXPECTED;
                break;
        }
    }
```



### <a name="release-resources"></a><span data-ttu-id="d6b16-147">Liberar recursos</span><span class="sxs-lookup"><span data-stu-id="d6b16-147">Release Resources</span></span>

<span data-ttu-id="d6b16-148">Depois que um status de trabalho indica a conclusão, libere as interfaces e os recursos usados para esse trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="d6b16-148">After a job status indicates completion, release the interfaces and resources used for this print job.</span></span>


```C++
    if (packageWriter)
    {
        packageWriter->Release();
        packageWriter = NULL;
    }

    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    if (xpsFactory)
    {
        xpsFactory->Release();
        xpsFactory = NULL;
    }

    if (jobStream)
    {
        jobStream->Release();
        jobStream = NULL;
    }

    if (job)
    {
        job->Release();
        job = NULL;
    }

    if (completionEvent)
    {
        CloseHandle(completionEvent);
        completionEvent = NULL;
    }
```



 

 
