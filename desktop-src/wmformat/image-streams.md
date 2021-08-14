---
title: Fluxos de imagem
description: Fluxos de imagem
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows SDK do formato de mídia, fluxos de imagem
- ASF (Advanced Systems Format), fluxos de imagem
- ASF (formato de sistemas avançados), fluxos de imagem
- Windows SDK do formato de mídia, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
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
# <a name="image-streams"></a>Fluxos de imagem

Um fluxo de imagem é um tipo especial de fluxo que contém imagens ainda atribuídas a tempos de apresentação. Um aplicativo pode exibir as imagens em um fluxo de imagem conforme desejado, mas a implementação típica é exibir cada imagem até que a próxima imagem seja entregue, como uma apresentação de slides. Normalmente, um fluxo de imagem é codificado em um arquivo com um fluxo de áudio para produzir uma apresentação simples de imagens sincronizadas com música ou fala.

Os fluxos de imagem são como fluxos de vídeo, pois são criados a partir de exemplos descompactados que são compactados como parte do processo de gravação de arquivo, mas também são como fluxos arbitrários, pois você deve atribuir uma taxa de bits e uma janela de buffer apropriada ao conteúdo sem depender de propriedades atribuídas ao codec.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fluxos arbitrário**](arbitrary-streams.md)
</dt> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Fluxos de áudio e vídeo**](audio-and-video-streams.md)
</dt> <dt>

[**Fluxos de gravação de imagem**](writing-image-streams.md)
</dt> </dl>

 

 




