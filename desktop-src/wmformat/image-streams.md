---
title: Imagem Fluxos
description: Imagem Fluxos
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows SDK de Formato de Mídia, fluxos de imagem
- ASF (Advanced Systems Format), fluxos de imagem
- ASF (Formato de Sistemas Avançados), fluxos de imagem
- Windows SDK de Formato de Mídia, fluxos
- ASF (Advanced Systems Format), streams
- ASF (Formato de Sistemas Avançados), fluxos
- fluxos de imagem, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2067710e6b2be627bd16125d73e567a2f1ba1557ae01b81f55712d8c5a7b8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702860"
---
# <a name="image-streams"></a>Imagem Fluxos

Um fluxo de imagem é um tipo especial de fluxo que contém imagens ainda atribuídas aos tempos de apresentação. Um aplicativo pode exibir as imagens em um fluxo de imagem conforme desejado, mas a implementação típica é exibir cada imagem até que a próxima imagem seja entregue, como uma apresentação de slides. Normalmente, um fluxo de imagem é codificado em um arquivo com um fluxo de áudio para produzir uma apresentação simples de imagens sincronizadas com música ou fala.

Os fluxos de imagem são como fluxos de vídeo, pois são criados com base em amostras descompactadas que são compactadas como parte do processo de gravação de arquivo, mas também são como fluxos arbitrários porque você deve atribuir uma taxa de bits e uma janela de buffer apropriadas ao conteúdo sem depender de propriedades atribuídas a codec.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Dados arbitrários Fluxos**](arbitrary-streams.md)
</dt> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Áudio e vídeo Fluxos**](audio-and-video-streams.md)
</dt> <dt>

[**Escrevendo imagens Fluxos**](writing-image-streams.md)
</dt> </dl>

 

 




