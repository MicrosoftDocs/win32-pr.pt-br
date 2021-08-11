---
description: Um codificador converte áudio ou vídeo descompactado em pacotes compactados no formato especificado pelo aplicativo. para converter arquivos de mídia em formato ASF, você pode usar os codecs de áudio e vídeo de mídia Windows.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows Codificadores de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d79ff55e98227c63e9761a8dec5ae068c8b1786c067230548ad0028dbe301a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237285"
---
# <a name="windows-media-encoders"></a>Windows Codificadores de mídia

Um codificador converte áudio ou vídeo descompactado em pacotes compactados no formato especificado pelo aplicativo. para converter arquivos de mídia em formato ASF, você pode usar os codecs de áudio e vídeo de mídia Windows.

Um codificador é identificado pelo GUID que representa a categoria: áudio ou vídeo. O tipo de saída do codificador é representado por um tipo de mídia principal e o GUID de subtipo.

-   Windows Codecs de áudio de mídia

    Categoria: **\_ \_ \_ codificador de áudio de categoria de MFT**

    Tipo principal: \_ áudio MFMediaType

    Subtipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Windows Codecs de vídeo de mídia

    Categoria: **\_ \_ \_ codificador de vídeo de categoria MFT**

    Tipo principal: \_ vídeo MFMediaType

    Subtipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Esses codificadores são implementados como [Media Foundation transformação](media-foundation-transforms.md) (MFT) e Media Foundation fornece acesso ao aplicativo por meio da interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) do codificador. Se você estiver usando componentes da camada de pipeline para codificação ASF, o MFT do codificador será inserido no pipeline como um nó de transformação porque é responsável por transformar dados de mídia que fluem pela origem para o coletor. Se a origem for um tipo compactado, o pipeline adicionará os decodificadores necessários para converter a origem em um tipo descompactado. Um codificador tem um fluxo de entrada e um fluxo de saída. O codificador recebe dados de entrada e produz dados codificados de acordo com a configuração e o formato definidos pelo aplicativo antes da sessão de codificação. O formato do fluxo de saída é descrito por um tipo de mídia.

Esta seção contém os seguintes tópicos.



| Tópico                                                                              | Descrição                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Criando uma instância de um MFT do codificador](instantiating-the-encoder-mft.md)                  | Explica como criar o codificador.                                                         |
| [Propriedades de codificação](configuring-the-encoder.md)                                 | Explica como configurar o codificador definindo as propriedades apropriadas no MFT do codificador. |
| [Negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md) | Explica como definir tipos de mídia de entrada e saída no codificador.                            |
| [Configurando um codificador WMV](configuring-a-wmv-encoder.md)                         | explica como configurar um codificador de vídeo de mídia Windows (WMV).                              |
| [Configurando um tipo de saída para um codificador WMA](configuring-a-wma-encoder.md)          | explica como definir um tipo de saída em um codificador de áudio de mídia Windows (WMA).                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



