---
title: Para interromper a indexação em andamento
description: Para interromper a indexação em andamento
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- SDK do Windows Media Format, parando a indexação em andamento
- ASF (Advanced Systems Format), parando a indexação em andamento
- ASF (formato de sistemas avançados), parando a indexação em andamento
- índices, parando a indexação em andamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007134"
---
# <a name="to-stop-indexing-in-progress"></a><span data-ttu-id="cb8d1-107">Para interromper a indexação em andamento</span><span class="sxs-lookup"><span data-stu-id="cb8d1-107">To Stop Indexing in Progress</span></span>

<span data-ttu-id="cb8d1-108">Depois de começar a indexação com uma chamada para [**IWMIndexer:: startIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), o indexador normalmente continuará até que o arquivo seja indexado.</span><span class="sxs-lookup"><span data-stu-id="cb8d1-108">After you begin indexing with a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), the indexer will normally continue until the file is indexed.</span></span> <span data-ttu-id="cb8d1-109">Você pode parar a indexação de operações chamando o método [**IWMIndexer:: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) .</span><span class="sxs-lookup"><span data-stu-id="cb8d1-109">You can stop indexing operations by calling the [**IWMIndexer::Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) method.</span></span> <span data-ttu-id="cb8d1-110">Depois de ter cancelado a indexação, você **pode chamar de** forma diferente, mas o indexador começará a partir do início do arquivo, em vez de retomar a partir do ponto de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="cb8d1-110">After you have canceled indexing, you can call **StartIndexing** again, but the indexer will start from the beginning of the file rather than resuming from the point of cancellation.</span></span>

<span data-ttu-id="cb8d1-111">Como o **startIndex** é uma chamada assíncrona, normalmente você precisará chamar **Cancel** de algum outro thread ou manipulador de eventos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cb8d1-111">Because **StartIndexing** is an asynchronous call, you will normally need to call **Cancel** from some other thread or event handler in your application.</span></span> <span data-ttu-id="cb8d1-112">Normalmente, o **cancelamento** será chamado a partir de um procedimento de evento associado a um controle de botão de um aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="cb8d1-112">Typically **Cancel** will be called from an event procedure associated with a button control of a Windows application.</span></span>

<span data-ttu-id="cb8d1-113">Quando a indexação for cancelada, o indexador passará uma mensagem de status de WMT \_ fechada, assim como se o arquivo tivesse sido indexado corretamente.</span><span class="sxs-lookup"><span data-stu-id="cb8d1-113">When indexing is canceled, the indexer will pass a status message of WMT\_CLOSED, just as if the file had been indexed properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb8d1-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb8d1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb8d1-115">**Interface IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-115">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="cb8d1-116">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-116">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




