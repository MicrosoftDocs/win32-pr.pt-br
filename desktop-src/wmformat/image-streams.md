---
title: Fluxos de imagem
description: Fluxos de imagem
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- SDK do Windows Media Format, fluxos de imagem
- ASF (Advanced Systems Format), fluxos de imagem
- ASF (formato de sistemas avançados), fluxos de imagem
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- fluxos de imagem, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292591"
---
# <a name="image-streams"></a>Fluxos de imagem

Um fluxo de imagem é um tipo especial de fluxo que contém imagens ainda atribuídas a tempos de apresentação. Um aplicativo pode exibir as imagens em um fluxo de imagem conforme desejado, mas a implementação típica é exibir cada imagem até que a próxima imagem seja entregue, como uma apresentação de slides. Normalmente, um fluxo de imagem é codificado em um arquivo com um fluxo de áudio para produzir uma apresentação simples de imagens sincronizadas com música ou fala.

Os fluxos de imagem são como fluxos de vídeo, pois são criados a partir de exemplos descompactados que são compactados como parte do processo de gravação de arquivo, mas também são como fluxos arbitrários, pois você deve atribuir uma taxa de bits e uma janela de buffer apropriada ao conteúdo sem depender de propriedades atribuídas ao codec.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fluxos arbitrários**](arbitrary-streams.md)
</dt> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Fluxos de áudio e vídeo**](audio-and-video-streams.md)
</dt> <dt>

[**Gravando fluxos de imagem**](writing-image-streams.md)
</dt> </dl>

 

 




