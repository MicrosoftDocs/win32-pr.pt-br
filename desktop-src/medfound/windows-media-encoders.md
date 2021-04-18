---
description: Um codificador converte áudio ou vídeo descompactado em pacotes compactados no formato especificado pelo aplicativo. Para converter arquivos de mídia em formato ASF, você pode usar os codecs de áudio e vídeo do Windows Media.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Codificadores de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763856"
---
# <a name="windows-media-encoders"></a>Codificadores de mídia do Windows

Um codificador converte áudio ou vídeo descompactado em pacotes compactados no formato especificado pelo aplicativo. Para converter arquivos de mídia em formato ASF, você pode usar os codecs de áudio e vídeo do Windows Media.

Um codificador é identificado pelo GUID que representa a categoria: áudio ou vídeo. O tipo de saída do codificador é representado por um tipo de mídia principal e o GUID de subtipo.

-   Codecs de áudio do Windows Media

    Categoria: **\_ \_ \_ codificador de áudio de categoria de MFT**

    Tipo principal: \_ áudio MFMediaType

    Subtipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Codecs de vídeo do Windows Media

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
| [Configurando um codificador WMV](configuring-a-wmv-encoder.md)                         | Explica como configurar um codificador de vídeo do Windows Media (WMV).                              |
| [Configurando um tipo de saída para um codificador WMA](configuring-a-wma-encoder.md)          | Explica como definir um tipo de saída em um codificador de áudio do Windows Media (WMA).                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



