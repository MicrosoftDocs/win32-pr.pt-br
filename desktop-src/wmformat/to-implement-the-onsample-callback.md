---
title: Para implementar o retorno de chamada onsample
description: Para implementar o retorno de chamada onsample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- ASF (Advanced Systems Format), implementando o retorno de chamada OnStatus
- ASF (formato de sistemas avançados), implementando o retorno de chamada OnStatus
- ASF (Advanced Systems Format), retorno de chamada OnStatus
- ASF (formato de sistemas avançados), retorno de chamada OnStatus
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, implementando o retorno de chamada OnStatus
- Método de retorno de chamada OnStatus, implementando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00523ae28ec14feefb8249ff86a2b1600629c84cb245eb627b59b619a28a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027284"
---
# <a name="to-implement-the-onsample-callback"></a>Para implementar o retorno de chamada onsample

O leitor assíncrono fornece amostras para o aplicativo de controle em ordem de tempo de apresentação fazendo chamadas para o método de retorno de chamada [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) . Ao criar um aplicativo usando o leitor assíncrono, você deve implementar **onsample** para lidar com amostras não compactadas. Normalmente, as funções ou métodos criados para renderizar conteúdo serão chamados de dentro de **onsample**.

A implementação típica do retorno de chamada **onsample** inclui as etapas a seguir.

1.  Recupere o local e o tamanho do buffer que contém o exemplo chamando [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) no buffer passado como *pSample*.
2.  Ramificar sua lógica dependendo do número de saída. O número de saída é passado para **onsample** como *dwOutputNumber*.
3.  Inclua a lógica de renderização para cada número de saída ao qual você deseja dar suporte. Se você estiver renderizando exemplos de várias saídas, talvez seja necessário sincronizar sua renderização.

Os aplicativos que fornecem amostras compactadas de arquivos ASF precisam implementar o método de retorno de chamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . O **OnStreamSample** funciona quase de forma idêntica ao **onsample**, exceto pelo fato de receber amostras compactadas por número de fluxo em vez de amostras não compactadas por número de saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**Interface IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Usando os métodos de retorno de chamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




