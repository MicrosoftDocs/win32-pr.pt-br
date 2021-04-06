---
description: Descreve como enviar um OM XPS para uma impressora como um documento XPS.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Imprimir um OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01ae1081c4f0c58c66efedc30406e310dd8dd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011198"
---
# <a name="print-an-xps-om"></a><span data-ttu-id="33165-103">Imprimir um OM XPS</span><span class="sxs-lookup"><span data-stu-id="33165-103">Print an XPS OM</span></span>

<span data-ttu-id="33165-104">Descreve como enviar um OM XPS para uma impressora como um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="33165-104">Describes how to send an XPS OM to a printer as an XPS document.</span></span>

<span data-ttu-id="33165-105">Para obter instruções sobre como imprimir um OM XPS que contém um documento XPS completo, consulte [imprimir um om XPS completo](#print-a-complete-xps-om).</span><span class="sxs-lookup"><span data-stu-id="33165-105">For instructions on how to print an XPS OM that contains a complete XPS document, see [Print a complete XPS OM](#print-a-complete-xps-om).</span></span> <span data-ttu-id="33165-106">Para conter um documento XPS, um OM XPS deve incluir os itens listados em [criar um om XPS em branco](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="33165-106">To contain an XPS document, an XPS OM must include the items listed in [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>

<span data-ttu-id="33165-107">Para obter instruções sobre como imprimir um OM XPS que está sendo criado ou processado uma página por vez, consulte [incrementalmente um om XPS](#incrementally-print-an-xps-om).</span><span class="sxs-lookup"><span data-stu-id="33165-107">For instructions on how to print an XPS OM that is being created or processed one page at a time, see [Incrementally print an XPS OM](#incrementally-print-an-xps-om).</span></span>

<span data-ttu-id="33165-108">Antes de usar esses exemplos de código em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="33165-108">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

<span data-ttu-id="33165-109">Neste tópico, você aprenderá a executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="33165-109">In this topic, you will learn how to perform the following tasks:</span></span>

-   [<span data-ttu-id="33165-110">Imprimir um OM XPS completo</span><span class="sxs-lookup"><span data-stu-id="33165-110">Print a complete XPS OM</span></span>](#print-a-complete-xps-om)
-   [<span data-ttu-id="33165-111">Imprimir incrementalmente um OM XPS</span><span class="sxs-lookup"><span data-stu-id="33165-111">Incrementally print an XPS OM</span></span>](#incrementally-print-an-xps-om)
-   [<span data-ttu-id="33165-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33165-112">Related topics</span></span>](#related-topics)

## <a name="print-a-complete-xps-om"></a><span data-ttu-id="33165-113">Imprimir um OM XPS completo</span><span class="sxs-lookup"><span data-stu-id="33165-113">Print a complete XPS OM</span></span>

<span data-ttu-id="33165-114">Quando um OM XPS contém um documento XPS completo, o método [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) da interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) pode enviar o conteúdo do OM XPS para uma impressora ou uma fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="33165-114">When an XPS OM contains a complete XPS document, the [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface can send the contents of the XPS OM to a printer or a print queue.</span></span>

<span data-ttu-id="33165-115">Para detectar quando o trabalho de impressão foi concluído, crie um identificador de evento, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="33165-115">To detect when the print job has completed, create an event handle as shown in the following example.</span></span>


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="33165-116">Para imprimir um OM XPS completo:</span><span class="sxs-lookup"><span data-stu-id="33165-116">To print a complete XPS OM:</span></span>

1.  <span data-ttu-id="33165-117">Crie um novo fluxo de trabalho de impressão chamando [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="33165-117">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="33165-118">Envie o conteúdo do OM XPS para o fluxo chamando o método [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) do pacote.</span><span class="sxs-lookup"><span data-stu-id="33165-118">Send the contents of the XPS OM to the stream by calling the package's [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method.</span></span>
3.  <span data-ttu-id="33165-119">Feche o fluxo do trabalho de impressão chamando o método **Close** do fluxo.</span><span class="sxs-lookup"><span data-stu-id="33165-119">Close the print job stream by calling the stream's **Close** method.</span></span>
4.  <span data-ttu-id="33165-120">Aguarde até que o trabalho de impressão sinalize que foi concluído.</span><span class="sxs-lookup"><span data-stu-id="33165-120">Wait for the print job to signal that it has completed.</span></span>
5.  <span data-ttu-id="33165-121">Verifique o status de conclusão.</span><span class="sxs-lookup"><span data-stu-id="33165-121">Check the completion status.</span></span>
6.  <span data-ttu-id="33165-122">Fechar e liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="33165-122">Close and release resources.</span></span>


```C++
    IXpsPrintJob *job = NULL;
    IXpsPrintJobStream *jobStream = NULL;
    hr = StartXpsPrintJob(
                printerName,
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Write package to print job stream
    hr = package->WriteToStream (jobStream, FALSE);

    // Close the stream to tell the print job
    // that the entire document has been sent.
    hr = jobStream->Close();

    // Wait for the print job to finish spooling...
    if (NULL != completionEvent) {
        if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
        {
            // Get the print job status to see why the wait completed.
            //  Note that without waiting for a completion event, 
            //  the print job may not be complete when the status is queried.
            XPS_JOB_STATUS jobStatus;
            hr = job->GetJobStatus(&jobStatus);

            // Evaluate the job status returned.
            switch (jobStatus.completion)
            {
                case XPS_JOB_COMPLETED:
                    // The job completed as expected.
                    hr = S_OK;
                    break;
                case XPS_JOB_CANCELLED:
                    // The job was canceled.
                    hr = E_FAIL;
                    break;
                case XPS_JOB_FAILED:
                    // The job failed, 
                    // jobStatus.jobStatus has the reason.
                    hr = E_FAIL;
                    break;
                default:
                    // An unexpected value was returned.
                    hr = E_UNEXPECTED;
                    break;
            }
                
            // Release completion event handle
            CloseHandle(completionEvent);
        }
        else
        {    // there was a problem, set hr to error status
            hr  = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // hr contains the result of the print operation

    CoUninitialize(); // if COM is no longer needed in this thread
```



## <a name="incrementally-print-an-xps-om"></a><span data-ttu-id="33165-123">Imprimir incrementalmente um OM XPS</span><span class="sxs-lookup"><span data-stu-id="33165-123">Incrementally print an XPS OM</span></span>

<span data-ttu-id="33165-124">Você pode enviar os componentes do documento de um OM XPS para um trabalho de impressora incrementalmente, criando um fluxo de trabalho de impressão XPS e, em seguida, passando os componentes de documento individuais para o fluxo do trabalho de impressão, um de cada vez.</span><span class="sxs-lookup"><span data-stu-id="33165-124">You can send the document components of an XPS OM to a printer job incrementally, by creating an XPS print job stream and then passing the individual document components to the print job stream, one at a time.</span></span> <span data-ttu-id="33165-125">A sequência na qual os componentes do documento são enviados determina como eles serão exibidos no documento concluído.</span><span class="sxs-lookup"><span data-stu-id="33165-125">The sequence in which the document components are sent determines how they will appear in the finished document.</span></span> <span data-ttu-id="33165-126">Portanto, antes que um programa possa chamar o código neste exemplo, ele deve organizar corretamente os componentes do documento.</span><span class="sxs-lookup"><span data-stu-id="33165-126">Thus, before a program can call the code in this example, it must correctly organize the document components.</span></span>

<span data-ttu-id="33165-127">Antes de usar interfaces de OM XPS, inicialize COM no thread, conforme mostrado no código de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="33165-127">Before using XPS OM interfaces, initialize COM in the thread as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="33165-128">Para monitorar a conclusão do trabalho de impressão, crie um identificador de evento, conforme mostrado no código de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="33165-128">To monitor the print job completion, create an event handle as shown in the following example code.</span></span>


```C++
    HANDLE completionEvent = NULL;
    completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="33165-129">Crie um novo fluxo de trabalho de impressão e um novo gravador de pacote.</span><span class="sxs-lookup"><span data-stu-id="33165-129">Create a new print job stream and a new package writer.</span></span> <span data-ttu-id="33165-130">Passe cada um dos componentes do documento para os métodos de gravador de pacote correspondentes na mesma sequência, pois eles aparecerão no documento concluído.</span><span class="sxs-lookup"><span data-stu-id="33165-130">Pass each of the document components to the corresponding package writer methods in the same sequence as they will appear in the finished document.</span></span>

<span data-ttu-id="33165-131">Inicie cada documento novo e adicione páginas a ele.</span><span class="sxs-lookup"><span data-stu-id="33165-131">Start each document new, then add pages to it.</span></span> <span data-ttu-id="33165-132">Depois de passar todos os componentes do documento para o fluxo do trabalho de impressão, feche o fluxo, aguarde a conclusão do trabalho de impressão e feche e libere os recursos abertos.</span><span class="sxs-lookup"><span data-stu-id="33165-132">After passing all document components to the print job stream, close the stream, wait for the print job to complete, and then close and release open resources.</span></span>

1.  <span data-ttu-id="33165-133">Crie um novo fluxo de trabalho de impressão chamando [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="33165-133">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="33165-134">Crie um URI de parte para a parte FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="33165-134">Create a part URI for the FixedDocumentSequence part.</span></span>
3.  <span data-ttu-id="33165-135">Crie um novo gravador de pacote no fluxo do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="33165-135">Create a new package writer on the print job stream.</span></span>
4.  <span data-ttu-id="33165-136">Para cada documento a ser escrito:</span><span class="sxs-lookup"><span data-stu-id="33165-136">For each document to be written:</span></span>
    1.  <span data-ttu-id="33165-137">Crie um novo URI de parte para a parte de FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="33165-137">Create a new part URI for the FixedDocument part.</span></span>
    2.  <span data-ttu-id="33165-138">Inicie um novo documento no gravador de pacote.</span><span class="sxs-lookup"><span data-stu-id="33165-138">Start a new document in the package writer.</span></span>
    3.  <span data-ttu-id="33165-139">Para cada página no documento atual, crie um URI de parte para a parte FixedPage e adicione a página ao gravador de pacote.</span><span class="sxs-lookup"><span data-stu-id="33165-139">For each page in the current document, create a part URI for the FixedPage part and add the page to the package writer.</span></span>
5.  <span data-ttu-id="33165-140">Depois que todas as páginas tiverem sido adicionadas ao gravador de pacote, feche-o.</span><span class="sxs-lookup"><span data-stu-id="33165-140">After all pages have been added to the package writer, close it.</span></span>
6.  <span data-ttu-id="33165-141">Feche o fluxo do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="33165-141">Close the print job stream.</span></span>
7.  <span data-ttu-id="33165-142">Aguarde a conclusão do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="33165-142">Wait for the print job to complete.</span></span>
8.  <span data-ttu-id="33165-143">Verifique o status de conclusão.</span><span class="sxs-lookup"><span data-stu-id="33165-143">Check the completion status.</span></span>
9.  <span data-ttu-id="33165-144">Feche e libere os recursos abertos.</span><span class="sxs-lookup"><span data-stu-id="33165-144">Close and release open resources.</span></span>


```C++
    IXpsPrintJob* job = NULL;
    IXpsPrintJobStream* jobStream = NULL;
    hr = StartXpsPrintJob(
                argv[1],
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Note the implicit requirement that CoInitializeEx 
    //  has previously been called from this thread.
    IXpsOMObjectFactory *xpsFactory = NULL;
    hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IXpsOMObjectFactory),
                reinterpret_cast<void**>(&xpsFactory)
                );
    // Create part URI for FixedDocumentSequence part
    //  This can use a static string because there is only one
    //  FixedDocumentSequence part in the print job.
    IOpcPartUri *partUri = NULL;
    hr = xpsFactory->CreatePartUri(L"/FixedDocumentSequence.fdseq", &partUri);

    // Create the package writer on the print job stream
    //  Note that the interleaving parameter set to 
    //  XPS_INTERLEAVING_ON, the package writer will create
    //  empty print ticket parts when a NULL pointer is
    //  passed in the print ticket argument of this method,
    //  the StartNewDocument method, and the AddPage method.
    //  For more information, see the help for these methods.
    IXpsOMPackageWriter *packageWriter = NULL;
    hr = xpsFactory->CreatePackageWriterOnStream(
            jobStream,
            TRUE,
            XPS_INTERLEAVING_ON, // to create blank print ticket objects
            partUri,
            NULL,
            NULL,
            NULL,
            NULL,
            &packageWriter);
    // release partUri after it's been used to create new doc. seq.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    // Add document content to the print job stream.
    int docNumber = 1;
    int docsInPackage = 1; // Change this value as required.
    while (docNumber <= docsInPackage) {

        // Create a unique part URI for the current document.
        WCHAR DocPartUri[MAX_PATH];
        hr = MakeDocumentPartUri (docNumber, MAX_PATH, DocPartUri);
        hr = xpsFactory->CreatePartUri(DocPartUri, &partUri);
        
        // Initialize the new document in the package writer.
        hr = packageWriter->StartNewDocument(partUri, NULL, NULL, NULL, NULL);

        // release part URI after it's been used to create new doc.
        if (partUri)
        {
            partUri->Release();
            partUri = NULL;
        }

        // Add the pages
        int pageNumber = 1;
        int pagesInDocument = 1; // Change this value as required.
        while (pageNumber <= pagesInDocument) {

            // Create a unique part URI for the current page
            WCHAR PagePartUri[MAX_PATH];
            hr = MakePagePartUri (
                docNumber, 
                pageNumber, 
                MAX_PATH, 
                PagePartUri);
            hr = xpsFactory->CreatePartUri(PagePartUri, &partUri);

            // create page in OM
            XPS_SIZE pageSize = {816, 1056};
            IXpsOMPage *xpsPage = NULL;
            hr = xpsFactory->CreatePage(
                &pageSize, 
                L"en-US", 
                partUri, 
                &xpsPage);

            // release pagePartUri after it's been used to create the page
            if (partUri)
            {
                partUri->Release();
                partUri = NULL;
            }

            // add content to the page or retrieve 
            //  the page from the XPS OM.
            //  (not shown in this example)

            // add page to document
            hr = packageWriter->AddPage(
                        xpsPage,
                        &pageSize,
                        NULL,
                        NULL,
                        NULL,
                        NULL);

             if (xpsPage)
              {
                 xpsPage->Release();
                 xpsPage = NULL;
             }

            // go to the next page
            pageNumber++;
        }
        // the fixed document does not need to be closed.
        // it will be closed when a new fixed doc is opened
        // or the package is closed.

        // go to the next document
        docNumber++;
    }

    // Close the package writer when finished
    hr = packageWriter->Close();

    if (SUCCEEDED(hr))
    {
        // Close the print stream to tell the print
        //  job that the all document contents have
        //  been sent
        hr = jobStream->Close();
        // Wait for the print job to finish spooling...
        if (NULL != completionEvent) {
            if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
            {
                // Get the print job status to see why the wait completed.
                //  Note that without waiting for a completion event, 
                //  the print job may not be complete when the status is queried.
                XPS_JOB_STATUS jobStatus;
                hr = job->GetJobStatus(&jobStatus);

                // Evaluate the job status returned.
                switch (jobStatus.completion)
                {
                    case XPS_JOB_COMPLETED:
                        // The job completed as expected.
                        hr = S_OK;
                        break;
                    case XPS_JOB_CANCELLED:
                        // The job was canceled.
                        hr = E_FAIL;
                        break;
                    case XPS_JOB_FAILED:
                        // The job failed, 
                        // jobStatus.jobStatus has the reason.
                        hr = E_FAIL;
                        break;
                    default:
                        // An unexpected value was returned.
                        hr = E_UNEXPECTED;
                        break;
                }
                    
                // Release completion event handle
                CloseHandle(completionEvent);
            }
            else
            {    // there was a problem, set hr to error status
                hr  = HRESULT_FROM_WIN32(GetLastError());
            }
        }
    } 
    else
    {
        // cancel the job, if one exists, because
        //  the close call returned an error
        if (job) job->Cancel();
    }
    // hr contains the result of the print operation

    // free/release pointers and handles used.

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

    CoUninitialize(); // If done with COM in this thread.
```



<span data-ttu-id="33165-145">Quando o programa está gravando os componentes do documento de forma incremental, conforme mostrado neste exemplo, ele deve gerar os nomes de parte para cada parte do documento que ele envia para o fluxo do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="33165-145">When the program is writing the document components incrementally, as shown in this example, it must generate the part names for each document part that it sends to the print job stream.</span></span> <span data-ttu-id="33165-146">No exemplo anterior, o URI da parte FixedDocumentSequence é criado a partir de uma cadeia de caracteres estática porque existe uma e apenas uma dessas partes no documento XPS.</span><span class="sxs-lookup"><span data-stu-id="33165-146">In the preceding example, the FixedDocumentSequence part URI is created from a static string because there is one and only one such part in the XPS document.</span></span> <span data-ttu-id="33165-147">O URI de cada parte FixedPage e FixedDocument deve ser exclusivo no documento XPS.</span><span class="sxs-lookup"><span data-stu-id="33165-147">The URI of each FixedPage and FixedDocument part must be unique within the XPS document.</span></span> <span data-ttu-id="33165-148">A criação do URI da parte usando o índice desses componentes pode ajudar a garantir que a cadeia de caracteres do URI resultante seja exclusiva no documento XPS.</span><span class="sxs-lookup"><span data-stu-id="33165-148">Building the part URI by using the index of these components can help ensure that the resulting URI string is unique within the XPS document.</span></span>


```C++
HRESULT MakeDocumentPartUri (
                              __in int docNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //  that was passed as an argument
    // for example, "/Documents/1/FixedDocument.fdoc"
    //  where "1" specifies the document number, which would
    //  change with each document printed
    return S_OK;
}
 
HRESULT MakePagePartUri (
                              __in int docNumber,
                              __in int pageNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //   and page number that were passed as an argument
    // for example: "/Documents/1/Pages/1.fpage"
    //  where the first "1" between Documents and Pages 
    //  specifies the document number, which would change with
    //  each document. The second "1" specifies the page number,
    //  which would change with each page in the document.
    return S_OK;
}
```



<span data-ttu-id="33165-149">Para obter mais informações sobre a estrutura de um documento XPS, consulte a [especificação de papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="33165-149">For more information on the structure of an XPS document, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

## <a name="related-topics"></a><span data-ttu-id="33165-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33165-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="33165-151">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="33165-151">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="33165-152">Gravar um OM XPS em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="33165-152">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

<span data-ttu-id="33165-153">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="33165-153">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="33165-154">**CoInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="33165-154">**CoInitializeEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="33165-155">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="33165-155">**CreateEvent**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="33165-156">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="33165-156">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="33165-157">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="33165-157">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="33165-158">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="33165-158">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="33165-159">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="33165-159">**IXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[<span data-ttu-id="33165-160">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="33165-160">**IXpsPrintJobStream**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[<span data-ttu-id="33165-161">**StartXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="33165-161">**StartXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[<span data-ttu-id="33165-162">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="33165-162">**WaitForSingleObject**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

<span data-ttu-id="33165-163">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="33165-163">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="33165-164">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="33165-164">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="33165-165">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="33165-165">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="33165-166">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="33165-166">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
