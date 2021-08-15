---
description: Usando a categoria Windows imagem do vídeo de mídia 9.1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Usando a categoria Windows imagem do vídeo de mídia 9.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c630be78ec3edef1a47322b31f6a2331f15134a0cdffa4107b5a79daa86e9091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972625"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Usando a categoria Windows imagem do vídeo de mídia 9.1

A Windows imagem do vídeo de mídia 9.1 é diferente das outras categorias de saída com suporte pelo codificador e decodificador Windows Media Video 9. Em vez de processar vídeo descompactado, ele recebe amostras de entrada especiais que consistem em dados de transformação estruturados e, ocasionalmente, imagens de bitmap RGB nas quais as transformações são executadas.

O conteúdo da imagem Windows Media Video 9.1 codificado é praticamente idêntico ao conteúdo codificado regular do Windows Media Video 9, mas é identificado por seu próprio FOURCC ("WMVP").

O tipo de saída do codificador para imagem de vídeo é definido exatamente da mesma maneira que o vídeo Windows Media padrão, exceto que os valores de subtipo e compactação devem ser definidos para os identificadores de imagem de vídeo. Isso inclui a necessidade de obter dados particulares do codec e aendá-los à [**estrutura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) Para obter mais informações, [consulte Configuring Video Encoding](configuringvideoencoding.md).

A configuração de tipo de entrada para imagem de vídeo também é muito semelhante à configuração de entrada para outros codificadores de vídeo. Você pode recuperar um [**DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) parcialmente concluído do codificador chamando [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)ou se estiver usando o SDK do Media Foundation chamando [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) e recuperando o tipo de **mídia DMO \_ \_** usando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). Em seguida, você definirá o tamanho do quadro e a estrutura de formato [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) assim como faria para o vídeo padrão. Assim como no tipo de saída, você precisa garantir que os valores de subtipo e compactação sejam definidos adequadamente.

## <a name="creating-input-samples"></a>Criando exemplos de entrada

Os exemplos de entrada para o codec de imagem de vídeo são estruturados. A definição da estrutura e das constantes usadas para a imagem de vídeo não está incluída nas interfaces Windows codec de Áudio de Mídia e Vídeo. Essas definições estão incluídas no SDK Windows Formato de Mídia do Windows e seu uso é totalmente explicado na documentação do SDK Windows Formato de Mídia.

## <a name="decoding"></a>Decodificação

Não há requisitos especiais para decodificar o vídeo de captura de tela. Além de um subtipo diferente (MEDIASUBTYPE WMVP) usado para entrada do decodificador, o fluxo de imagem de vídeo compactado é essencialmente idêntico a um fluxo de vídeo de mídia \_ Windows padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 
