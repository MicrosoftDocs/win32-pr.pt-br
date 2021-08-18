---
title: Renderização de conteúdo
description: Renderização de conteúdo
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows SDK de Formato de Mídia, renderização de conteúdo
- ASF (Advanced Systems Format), renderização de conteúdo
- ASF (Formato de Sistemas Avançados), renderização de conteúdo
- ASF (Advanced Systems Format), renderização de conteúdo
- ASF (Formato de Sistemas Avançados), renderização de conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7add8d31f1fd025327325256e56c9f38faa4c97fd7e2aa206cedfebcc84c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929647"
---
# <a name="rendering-content"></a>Renderização de conteúdo

O Windows SDK de Formato de Mídia não fornece nenhuma rotina para renderizar o conteúdo entregue pelo objeto de leitor. Se você escrever aplicativos para reproduzir o conteúdo em arquivos ASF, deverá implementar suas próprias rotinas de renderização.

Você deve ter cuidado ao renderizar conteúdo para garantir que os exemplos sejam renderizados em ordem de tempo de apresentação e que exemplos de fluxos diferentes sejam sincronizados durante a renderização. O método que você emprega para garantir que a sincronização de fluxo dependerá da técnica de renderização usada para seu aplicativo. Em geral, se você tiver fluxos de áudio e vídeo, deverá sincronizar com o fluxo de áudio, pois a inconsistência no fluxo de áudio é mais perceptível do que alguns quadros descartados em um fluxo de vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Para recuperar exemplos de mídia com o Leitor Assíncrono**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Para recuperar exemplos de mídia com o Leitor Síncrono**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




