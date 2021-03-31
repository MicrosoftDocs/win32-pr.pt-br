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
# <a name="how-to-print-with-the-xps-print-api"></a>Como: imprimir com a API de impressão XPS

Este tópico descreve como usar a [API de impressão XPS](xpsprint-api.md) para imprimir de um aplicativo do Windows.

A [API de impressão XPS](xpsprint-api.md) permite que aplicativos nativos do Windows imprimam documentos XPS. Um aplicativo pode criar um documento XPS usando a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). O tópico da ajuda de [tarefas comuns de programação de documentos XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)) descreve como fazer isso. Depois que um documento XPS tiver sido criado, o aplicativo poderá usar a API de impressão XPS para imprimi-lo.

Usar a [API de impressão XPS](xpsprint-api.md) para imprimir um documento de um aplicativo envolve as etapas a seguir.

-   [Inicializar interface COM](#initialize-com-interface)
-   [Criar um evento de conclusão](#create-a-completion-event)
-   [Iniciar um trabalho de impressão XPS](#start-an-xps-print-job)
-   [Criar uma interface IXpsOMPackageWriter](#create-an-ixpsompackagewriter-interface)
-   [Fechar a interface IXpsOMPackageWriter](#close-the-ixpsompackagewriter-interface)
-   [Fechar o fluxo do trabalho de impressão](#close-the-print-job-stream)
-   [Aguardar o evento de conclusão](#wait-for-the-completion-event)
-   [Liberar recursos](#release-resources)

A [API de impressão XPS](xpsprint-api.md) requer um documento XPS para imprimir. No exemplo a seguir, o documento XPS é criado, pois ele é enviado para a impressora pela API de impressão XPS. Também é possível criar um documento XPS sem enviá-lo para uma impressora usando a API de [documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e mantendo-o como um om XPS ou salvando o OM XPS como um documento XPS. Para obter mais informações sobre como usar um OM XPS, consulte a API de documento XPS.

### <a name="initialize-com-interface"></a>Inicializar interface COM

Inicialize a interface COM, se o aplicativo ainda não tiver feito isso.


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



### <a name="create-a-completion-event"></a>Criar um evento de conclusão

Crie um evento de conclusão, que a [API de impressão XPS](xpsprint-api.md) usa para notificar o aplicativo quando o spooler de impressão tiver recebido o documento inteiro do aplicativo. A API de impressão XPS também dá suporte a um evento de progresso para que um aplicativo possa saber sobre outras atividades de spooling.


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



### <a name="start-an-xps-print-job"></a>Iniciar um trabalho de impressão XPS

Inicie um trabalho de impressão XPS chamando [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob). **StartXpsPrintJob** retorna um fluxo no qual o aplicativo enviará o documento a ser impresso.


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



### <a name="create-an-ixpsompackagewriter-interface"></a>Criar uma interface IXpsOMPackageWriter

Crie uma interface [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) chamando [**IXpsOMObjectFactory:: CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) no fluxo retornado por [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).


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



Para cada documento deste trabalho de impressão, inicie um novo documento e, em seguida, adicione páginas a esse documento.

### <a name="start-a-new-document"></a>Iniciar um novo documento

Inicie um novo documento no gravador de pacote chamando [**IXpsOMPackageWriter:: StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument). Se um documento estiver aberto quando esse método for chamado, ele será fechado e um novo documento será aberto.


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



### <a name="add-a-page"></a>Adicionar uma página

Chame [**IXpsOMPackageWriter:: AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) para gravar cada uma das páginas do documento do aplicativo no novo documento no gravador do pacote.

> [!Note]  
> Supõe-se que o aplicativo criou a página antes desta etapa. Para obter mais informações sobre como criar páginas de documentos e adicionar conteúdo a elas, consulte as [tarefas comuns de programação de documento XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)).

 


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



### <a name="close-the-ixpsompackagewriter-interface"></a>Fechar a interface IXpsOMPackageWriter

Depois que todos os documentos tiverem sido gravados para esse trabalho de impressão, chame [**IXpsOMPackageWriter:: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) para fechar o pacote.


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



### <a name="close-the-print-job-stream"></a>Fechar o fluxo do trabalho de impressão

Feche o fluxo do trabalho de impressão chamando [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), que informa ao spooler de impressão que todo o trabalho de impressão foi enviado pelo aplicativo.


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



### <a name="wait-for-the-completion-event"></a>Aguardar o evento de conclusão

Aguarde o evento de conclusão do trabalho de impressão.


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



Depois que o evento de conclusão for sinalizado, chame [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) para obter o status do trabalho.


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



### <a name="release-resources"></a>Liberar recursos

Depois que um status de trabalho indica a conclusão, libere as interfaces e os recursos usados para esse trabalho de impressão.


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



 

 
