---
description: Descreve como enviar um OM XPS para uma impressora como um documento XPS.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Imprimir um OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f1386352cff1556a5ce2403f34ebe4258c4110d4c3bf455990f3f1eb226d17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470899"
---
# <a name="print-an-xps-om"></a>Imprimir um OM XPS

Descreve como enviar um OM XPS para uma impressora como um documento XPS.

Para obter instruções sobre como imprimir um OM XPS que contém um documento XPS completo, consulte Imprimir um [OM XPS completo.](#print-a-complete-xps-om) Para conter um documento XPS, um OM XPS deve incluir os itens listados em [Criar um OM XPS em branco.](create-a-blank-xps-om.md)

Para obter instruções sobre como imprimir um OM XPS que está sendo criado ou processado uma página por vez, consulte Imprimir incrementalmente um [OM XPS.](#incrementally-print-an-xps-om)

Antes de usar esses exemplos de código em seu programa, leia a isenção de responsabilidade em [Tarefas comuns de programação de documentos XPS.](common-xps-document-tasks.md)

Neste tópico, você aprenderá a executar as seguintes tarefas:

-   [Imprimir um OM XPS completo](#print-a-complete-xps-om)
-   [Imprimir incrementalmente um OM XPS](#incrementally-print-an-xps-om)
-   [Tópicos relacionados](#related-topics)

## <a name="print-a-complete-xps-om"></a>Imprimir um OM XPS completo

Quando um OM XPS contém um documento XPS completo, o método [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) da interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) pode enviar o conteúdo do OM XPS para uma impressora ou uma fila de impressão.

Para detectar quando o trabalho de impressão for concluído, crie um identificador de evento, conforme mostrado no exemplo a seguir.


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



Para imprimir um OM XPS completo:

1.  Crie um fluxo de trabalho de impressão chamando [**StartXpsPrintJob.**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
2.  Envie o conteúdo do OM XPS para o fluxo chamando o método [**WriteToStream do**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) pacote.
3.  Feche o fluxo de trabalho de impressão chamando o método **Close do** fluxo.
4.  Aguarde até que o trabalho de impressão sinalize que ele foi concluído.
5.  Verifique o status de conclusão.
6.  Feche e libere recursos.


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



## <a name="incrementally-print-an-xps-om"></a>Imprimir incrementalmente um OM XPS

Você pode enviar os componentes de documento de um OM XPS para um trabalho de impressora de forma incremental, criando um fluxo de trabalho de impressão XPS e, em seguida, passando os componentes de documento individuais para o fluxo de trabalho de impressão, um de cada vez. A sequência na qual os componentes do documento são enviados determina como eles aparecerão no documento concluído. Portanto, antes que um programa possa chamar o código neste exemplo, ele deve organizar corretamente os componentes do documento.

Antes de usar interfaces OM XPS, inicialize COM no thread, conforme mostrado no código de exemplo a seguir.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Para monitorar a conclusão do trabalho de impressão, crie um alça de evento, conforme mostrado no código de exemplo a seguir.


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



Crie um novo fluxo de trabalho de impressão e um novo autor do pacote. Passe cada um dos componentes do documento para os métodos correspondentes do package writer na mesma sequência que eles aparecerão no documento concluído.

Inicie cada documento novo e adicione páginas a ele. Depois de passar todos os componentes do documento para o fluxo de trabalho de impressão, feche o fluxo, aguarde a conclusão do trabalho de impressão e feche e libere recursos abertos.

1.  Crie um fluxo de trabalho de impressão chamando [**StartXpsPrintJob.**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
2.  Crie um URI de parte para a parte FixedDocumentSequence.
3.  Crie um novo autor do pacote no fluxo de trabalho de impressão.
4.  Para cada documento a ser gravado:
    1.  Crie um novo URI de parte para a parte FixedDocument.
    2.  Inicie um novo documento no autor do pacote.
    3.  Para cada página no documento atual, crie um URI de parte para a parte FixedPage e adicione a página ao autor do pacote.
5.  Depois que todas as páginas foram adicionadas ao autor do pacote, feche-a.
6.  Feche o fluxo de trabalho de impressão.
7.  Aguarde a conclusão do trabalho de impressão.
8.  Verifique o status de conclusão.
9.  Feche e libere recursos abertos.


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



Quando o programa está escrevendo os componentes do documento incrementalmente, conforme mostrado neste exemplo, ele deve gerar os nomes das partes para cada parte do documento que ele envia para o fluxo de trabalho de impressão. No exemplo anterior, o URI da parte FixedDocumentSequence é criado a partir de uma cadeia de caracteres estática porque há uma e apenas uma parte desse tipo no documento XPS. O URI de cada parte fixedPage e FixedDocument deve ser exclusivo no documento XPS. Criar o URI da parte usando o índice desses componentes pode ajudar a garantir que a cadeia de caracteres de URI resultante seja exclusiva no documento XPS.


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



Para obter mais informações sobre a estrutura de um documento XPS, consulte o [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Gravar um OM XPS em um documento XPS](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

**Usado nesta seção**
</dt> <dt>

[**Coinitializeex**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[**Createevent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**IXpsPrintJob**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[**IXpsPrintJobStream**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[**Waitforsingleobject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[Inicializar um OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Referência da API de Documento XPS](xps-programming-reference.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
