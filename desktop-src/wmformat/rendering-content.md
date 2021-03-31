---
title: Renderizando conteúdo
description: Renderizando conteúdo
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- SDK do Windows Media Format, Renderizando conteúdo
- Formato de sistema avançado (ASF), renderização de conteúdo
- ASF (formato de sistemas avançados), Renderizando conteúdo
- ASF (Advanced Systems Format), renderização de conteúdo
- ASF (formato de sistemas avançados), renderização de conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822984"
---
# <a name="rendering-content"></a>Renderizando conteúdo

O Windows Media Format SDK não fornece nenhuma rotina para renderizar o conteúdo fornecido pelo objeto Reader. Se você escrever aplicativos para reproduzir o conteúdo em arquivos ASF, deverá implementar suas próprias rotinas de renderização.

Você deve ter cuidado ao renderizar conteúdo para garantir que os exemplos sejam renderizados em ordem de tempo de apresentação e que os exemplos de fluxos diferentes sejam sincronizados durante a renderização. O método que você emprega para garantir a sincronização de fluxo dependerá da técnica de renderização usada para seu aplicativo. Em geral, se você tiver fluxos de áudio e vídeo, deverá sincronizar com o fluxo de áudio, pois a inconsistência no fluxo de áudio é mais perceptível do que alguns quadros descartados em um fluxo de vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Para recuperar amostras de mídia com o leitor assíncrono**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Para recuperar amostras de mídia com o leitor síncrono**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




