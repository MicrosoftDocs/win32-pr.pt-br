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
# <a name="to-index-an-asf-file"></a>Para indexar um arquivo ASF

O processo de indexação de um arquivo ASF é muito simples. Faça uma chamada para [**IWMIndexer:: startIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) e passe o nome do arquivo. O indexador faz o resto. A chamada para **startIndex** é assíncrona, portanto, o status deve ser monitorado usando o retorno de chamada **OnStatus** .

O código a seguir mostra como indexar um arquivo ASF. Se você quiser configurar o indexador antes de indexar o arquivo, será necessário incluir o código do exemplo incluído no [para configurar o indexador](to-configure-the-indexer.md).

Para este exemplo, o identificador que aponta para o evento deve ser criado como uma variável global para que possa ser acessado pelo retorno de chamada. A declaração a seguir deve aparecer em um escopo global.


```C++
HANDLE g_hEvent = NULL;

```



Em um cenário mais realista, o identificador de evento deve ser um membro de dados da classe que contém o retorno de chamada e a lógica para iniciar o indexador.

O indexador envia vários eventos para o retorno de chamada **OnStatus** após a chamada para **IWMIndexer:: startIndex**. Você pode interceptar esses itens conforme necessário para seu aplicativo. No mínimo, é necessário interceptar WMT \_ closed, que é enviado quando a indexação é concluída. Use a lógica a seguir dentro da chave de mensagem em sua implementação do retorno de chamada **OnStatus** .


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



Para este exemplo, supõe-se que a implementação do retorno de chamada **OnStatus** seja acessada por meio de um objeto chamado MyCallback. Para obter mais informações sobre como usar eventos e retornos de chamada com este SDK, consulte [usando os métodos de retorno de chamada](using-the-callback-methods.md).


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

[**Interface IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Para configurar o indexador**](to-configure-the-indexer.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




