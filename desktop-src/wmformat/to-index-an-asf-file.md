---
title: Para indexar um arquivo ASF
description: Para indexar um arquivo ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- SDK do Windows Media Format, indexando arquivos ASF
- ASF (Advanced Systems Format), arquivos de indexação
- ASF (formato de sistemas avançados), indexando arquivos
- índices, indexando arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105759920"
---
# <a name="to-index-an-asf-file"></a><span data-ttu-id="32908-107">Para indexar um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="32908-107">To Index an ASF File</span></span>

<span data-ttu-id="32908-108">O processo de indexação de um arquivo ASF é muito simples.</span><span class="sxs-lookup"><span data-stu-id="32908-108">The process of indexing an ASF file is very simple.</span></span> <span data-ttu-id="32908-109">Faça uma chamada para [**IWMIndexer:: startIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) e passe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="32908-109">Make a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) and pass the file name.</span></span> <span data-ttu-id="32908-110">O indexador faz o resto.</span><span class="sxs-lookup"><span data-stu-id="32908-110">The indexer does the rest.</span></span> <span data-ttu-id="32908-111">A chamada para **startIndex** é assíncrona, portanto, o status deve ser monitorado usando o retorno de chamada **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="32908-111">The call to **StartIndexing** is asynchronous, so status must be monitored using the **OnStatus** callback.</span></span>

<span data-ttu-id="32908-112">O código a seguir mostra como indexar um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="32908-112">The following code shows how to index an ASF file.</span></span> <span data-ttu-id="32908-113">Se você quiser configurar o indexador antes de indexar o arquivo, será necessário incluir o código do exemplo incluído no [para configurar o indexador](to-configure-the-indexer.md).</span><span class="sxs-lookup"><span data-stu-id="32908-113">If you want to configure the indexer prior to indexing the file, you will need to include code from the example included in [To Configure the Indexer](to-configure-the-indexer.md).</span></span>

<span data-ttu-id="32908-114">Para este exemplo, o identificador que aponta para o evento deve ser criado como uma variável global para que possa ser acessado pelo retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="32908-114">For this example, the handle that points to the event must be created as a global variable so it will be accessible by the callback.</span></span> <span data-ttu-id="32908-115">A declaração a seguir deve aparecer em um escopo global.</span><span class="sxs-lookup"><span data-stu-id="32908-115">The following declaration should appear in a global scope.</span></span>


```C++
HANDLE g_hEvent = NULL;

```



<span data-ttu-id="32908-116">Em um cenário mais realista, o identificador de evento deve ser um membro de dados da classe que contém o retorno de chamada e a lógica para iniciar o indexador.</span><span class="sxs-lookup"><span data-stu-id="32908-116">In a more realistic scenario, the event handle should be a data member of the class that contains both the callback and the logic for starting the indexer.</span></span>

<span data-ttu-id="32908-117">O indexador envia vários eventos para o retorno de chamada **OnStatus** após a chamada para **IWMIndexer:: startIndex**.</span><span class="sxs-lookup"><span data-stu-id="32908-117">The indexer sends several events to the **OnStatus** callback after the call to **IWMIndexer::StartIndexing**.</span></span> <span data-ttu-id="32908-118">Você pode interceptar esses itens conforme necessário para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="32908-118">You can trap them as needed for your application.</span></span> <span data-ttu-id="32908-119">No mínimo, é necessário interceptar WMT \_ closed, que é enviado quando a indexação é concluída.</span><span class="sxs-lookup"><span data-stu-id="32908-119">At a minimum, you need to trap WMT\_CLOSED, which is sent when indexing is complete.</span></span> <span data-ttu-id="32908-120">Use a lógica a seguir dentro da chave de mensagem em sua implementação do retorno de chamada **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="32908-120">Use the following logic within the message switch in your implementation of the **OnStatus** callback.</span></span>


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



<span data-ttu-id="32908-121">Para este exemplo, supõe-se que a implementação do retorno de chamada **OnStatus** seja acessada por meio de um objeto chamado MyCallback.</span><span class="sxs-lookup"><span data-stu-id="32908-121">For this example it is assumed that your implementation of the **OnStatus** callback is accessed through an object called MyCallback.</span></span> <span data-ttu-id="32908-122">Para obter mais informações sobre como usar eventos e retornos de chamada com este SDK, consulte [usando os métodos de retorno de chamada](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="32908-122">For more information about using events and callbacks with this SDK, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="32908-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32908-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32908-124">**Interface IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="32908-124">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="32908-125">**Para configurar o indexador**</span><span class="sxs-lookup"><span data-stu-id="32908-125">**To Configure the Indexer**</span></span>](to-configure-the-indexer.md)
</dt> <dt>

[<span data-ttu-id="32908-126">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="32908-126">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="32908-127">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="32908-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




