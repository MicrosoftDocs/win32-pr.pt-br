---
title: Para indexar um arquivo ASF
description: Para indexar um arquivo ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows SDK de Formato de Mídia, indexação de arquivos ASF
- ASF (Advanced Systems Format), indexando arquivos
- ASF (Formato de Sistemas Avançados), indexação de arquivos
- índices, indexação de arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c2e41ed60ecb8fcee39da35dbc79ec44cece8db62f3e040d42aee3374c5690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845574"
---
# <a name="to-index-an-asf-file"></a>Para indexar um arquivo ASF

O processo de indexação de um arquivo ASF é muito simples. Faça uma chamada para [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) e passe o nome do arquivo. O indexador faz o restante. A chamada para **StartIndexing** é assíncrona, portanto, o status deve ser monitorado usando o retorno de chamada **OnStatus.**

O código a seguir mostra como indexar um arquivo ASF. Se você quiser configurar o indexador antes de indexar o arquivo, precisará incluir o código do exemplo incluído em Para configurar [o indexador](to-configure-the-indexer.md).

Para este exemplo, o handle que aponta para o evento deve ser criado como uma variável global para que ele seja acessível pelo retorno de chamada. A declaração a seguir deve aparecer em um escopo global.


```C++
HANDLE g_hEvent = NULL;

```



Em um cenário mais realista, o handle de evento deve ser um membro de dados da classe que contém o retorno de chamada e a lógica para iniciar o indexador.

O indexador envia vários eventos para o retorno de chamada **OnStatus** após a chamada para **IWMIndexer::StartIndexing**. Você pode interceptá-los conforme necessário para seu aplicativo. No mínimo, você precisa interceptar WMT \_ CLOSED, que é enviado quando a indexação é concluída. Use a lógica a seguir na opção de mensagem em sua implementação do retorno **de chamada OnStatus.**


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



Neste exemplo, supõe-se que sua implementação do retorno **de chamada OnStatus** seja acessada por meio de um objeto chamado MyCallback. Para obter mais informações sobre como usar eventos e retornos de chamada com esse SDK, consulte [Usando os métodos de retorno de chamada](using-the-callback-methods.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMIndexer Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Para configurar o indexador**](to-configure-the-indexer.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




