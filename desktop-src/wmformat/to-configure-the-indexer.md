---
title: Para configurar o indexador
description: Para configurar o indexador
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows SDK de Formato de Mídia, configurando indexadores
- ASF (Advanced Systems Format), configurando indexadores
- ASF (Formato de Sistemas Avançados), configurando indexadores
- índices, configurando indexadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5a624a4ed9ae749559a1908e3809500bf8aece2b29b8ad406769c5f639e547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845621"
---
# <a name="to-configure-the-indexer"></a>Para configurar o indexador

Você pode configurar o indexador antes de usá-lo para indexar um arquivo ASF. Cada fluxo no arquivo pode ser configurado separadamente ou você pode definir a mesma configuração para todos os fluxos.

Se você estiver configurando vários motores para indexação em um arquivo, deverá configurá-los todos e, em seguida, começar a indexação. Se você configurar e indexar um fluxo e, em seguida, configurar outro fluxo no mesmo arquivo, iniciar o indexador novamente excluirá o primeiro índice. Isso é para estar em conformidade com o formato de arquivo ASF.

O código a seguir mostra como configurar o indexador. O código pressupo que o arquivo a ser indexado tem dois fluxos: o primeiro é um fluxo de áudio que não precisa ser indexado e o segundo é um fluxo de vídeo. Esse código mostra apenas como configurar o indexador. Para indexar um arquivo, você deve seguir as etapas apresentadas em [Para indexar um arquivo ASF](to-index-an-asf-file.md).


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> O tipo de índice padrão é WMT \_ IT \_ NEAREST \_ CLEAN \_ POINT. Embora você possa definir o tipo de índice para outros valores, isso prejudicará o desempenho da busca.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**Para indexar um arquivo ASF**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




