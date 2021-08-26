---
description: Saiba mais sobre exemplos de mídia Microsoft Media Foundation. Um exemplo de mídia é um objeto que contém uma lista ordenada de zero ou mais buffers.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Exemplos de mídia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83bad0186d54d99b6c7f7666a5971f6c35e8e2a561109e7bfd6afd45fd5f5e6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061066"
---
# <a name="media-samples-microsoft-media-foundation"></a>Exemplos de mídia (Microsoft Media Foundation)

Um exemplo de mídia é um objeto que contém uma lista ordenada de zero ou mais buffers. Exemplos de mídia expõem a interface [**IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) A quantidade de dados contidos em um exemplo depende do componente que cria o exemplo e do tipo de dados nos buffers. Para vídeo descompactado, um exemplo geralmente contém um único quadro de vídeo. Para áudio descompactado, a quantidade de dados pode variar, mas geralmente um quadro de áudio não abrange dois exemplos. Para dados compactados, essas diretrizes podem não se aplicar.

Um único exemplo pode conter vários buffers por motivos de eficiência. Por exemplo, em um arquivo ASF, um quadro de vídeo geralmente é distribuído entre vários pacotes ASF. A fonte de mídia pode ler os pacotes em vários buffers. Em vez de copiar cada fragmento em um buffer, a origem simplesmente coloca todos os buffers em um exemplo. Os componentes downstream podem decidir se os buffers menores são copiados em um buffer contíguo. Em geral, se você estiver escrevendo um componente de pipeline, deverá supor que qualquer exemplo pode conter mais de um buffer.

Esta seção contém os seguintes tópicos.



| Tópico                                                        | Descrição                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Trabalhando com exemplos de mídia](working-with-media-samples.md) | Descreve o comportamento geral de exemplos de mídia.                                                                         |
| [Exemplos de vídeo](video-samples.md)                           | Descreve uma implementação especializada de [**IMFSample projetada**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para manter quadros de vídeo descompactados. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de mídia](media-buffers.md)
</dt> <dt>

[Media Foundation primitivos](media-foundation-primitives.md)
</dt> </dl>

 

 



