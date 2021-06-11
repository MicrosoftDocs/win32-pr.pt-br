---
description: Saiba mais sobre exemplos de mídia no Microsoft Media Foundation. Um exemplo de mídia é um objeto que contém uma lista ordenada de zero ou mais buffers.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Amostras de mídia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5d29b11fb6db316e3fbf6e33e24218ddbbf062
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989151"
---
# <a name="media-samples-microsoft-media-foundation"></a>Amostras de mídia (Microsoft Media Foundation)

Um exemplo de mídia é um objeto que contém uma lista ordenada de zero ou mais buffers. Amostras de mídia expõem a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) . A quantidade de dados contida em um exemplo depende do componente que cria o exemplo e do tipo de dados nos buffers. Para vídeo descompactado, um exemplo geralmente mantém um único quadro de vídeo. Para áudio descompactado, a quantidade de dados pode variar, mas geralmente um quadro de áudio não abrange dois exemplos. Para dados compactados, essas diretrizes podem não se aplicar.

Um único exemplo pode conter vários buffers por motivos de eficiência. Por exemplo, em um arquivo ASF, um quadro de vídeo geralmente é distribuído entre vários pacotes ASF. A origem da mídia pode ler os pacotes em vários buffers. Em vez de copiar cada fragmento em um buffer, a origem simplesmente coloca todos os buffers em uma amostra. Os componentes downstream podem decidir se os buffers menores devem ser copiados em um buffer contíguo. Em geral, se você estiver escrevendo um componente de pipeline, deverá assumir que qualquer exemplo pode conter mais de um buffer.

Esta seção contém os seguintes tópicos.



| Tópico                                                        | Descrição                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Trabalhando com exemplos de mídia](working-with-media-samples.md) | Descreve o comportamento geral de amostras de mídia.                                                                         |
| [Exemplos de vídeo](video-samples.md)                           | Descreve uma implementação especializada do [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) projetado para conter quadros de vídeo descompactados. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de mídia](media-buffers.md)
</dt> <dt>

[Primitivos de Media Foundation](media-foundation-primitives.md)
</dt> </dl>

 

 



