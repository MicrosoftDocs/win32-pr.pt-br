---
title: Para configurar o indexador
description: Para configurar o indexador
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- SDK do Windows Media Format, configurando indexadores
- ASF (Advanced Systems Format), configurando indexadores
- ASF (formato de sistemas avançados), configurando indexadores
- índices, configurando indexadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365595"
---
# <a name="to-configure-the-indexer"></a>Para configurar o indexador

Você pode configurar o indexador antes de usá-lo para indexar um arquivo ASF. Cada fluxo no arquivo pode ser configurado separadamente ou você pode definir a mesma configuração para todos os fluxos.

Se você estiver configurando vários fluxos para indexação em um arquivo, deverá configurá-los todos e, em seguida, iniciar a indexação. Se você configurar e indexar um fluxo e, em seguida, configurar outro fluxo no mesmo arquivo, iniciar o indexador novamente excluirá o primeiro índice. Isso é para estar em conformidade com o formato de arquivo ASF.

O código a seguir mostra como configurar o indexador. O código pressupõe que o arquivo a ser indexado tem dois fluxos: o primeiro é um fluxo de áudio que não precisa ser indexado e o segundo é um fluxo de vídeo. Esse código mostra apenas como configurar o indexador. Para indexar um arquivo, você deve seguir as etapas apresentadas em [para indexar um arquivo ASF](to-index-an-asf-file.md).


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
> O tipo de índice padrão é WMT \_ ele \_ mais próximo do ponto de \_ limpeza \_ . Embora você possa definir o tipo de índice para outros valores, isso diminuirá o desempenho de busca.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMIndexer2:: configurar**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**Para indexar um arquivo ASF**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




