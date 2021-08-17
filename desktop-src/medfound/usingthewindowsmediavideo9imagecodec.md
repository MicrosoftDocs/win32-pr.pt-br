---
description: usando a categoria de imagem do Windows Media Video 9,1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: usando a categoria de imagem do Windows Media Video 9,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c630be78ec3edef1a47322b31f6a2331f15134a0cdffa4107b5a79daa86e9091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972625"
---
# <a name="using-the-windows-media-video-91-image-category"></a>usando a categoria de imagem do Windows Media Video 9,1

a categoria de imagem do Windows media video 9,1 é diferente das outras categorias de saída com suporte no codificador e no codificador de mídia de vídeo 9 do Windows Media. Em vez de processar vídeo descompactado, ele usa exemplos de entrada especiais que consistem em dados de transformação estruturados e, ocasionalmente, imagens de bitmap RGB nas quais as transformações são executadas.

o conteúdo codificado da imagem 9,1 do vídeo de mídia Windows é praticamente idêntico ao conteúdo codificado em vídeo de mídia normal Windows media 9, mas é identificado por seu próprio FOURCC ("WMVP").

o tipo de saída do codificador para imagem de vídeo é definido exatamente da mesma forma que o vídeo de mídia padrão Windows, exceto que os valores de subtipo e de compactação devem ser definidos para os identificadores de imagem de vídeo. Isso inclui a necessidade de obter dados privados do codec e acrescentá-los à estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Para obter mais informações, consulte [Configurando a codificação de vídeo](configuringvideoencoding.md).

A configuração de tipo de entrada para imagem de vídeo também é muito semelhante à configuração de entrada para os outros codificadores de vídeo. você pode recuperar um [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) parcialmente concluído do codificador chamando [**IMediaObject:: getinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)ou se estiver usando o SDK do Media Foundation, chamando [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) e recuperando o tipo de **\_ mídia DMO \_** usando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). Em seguida, você define o tamanho do quadro e a estrutura do formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , assim como faria com o vídeo padrão. Assim como com o tipo de saída, você precisa garantir que os valores de subtipo e compactação sejam definidos adequadamente.

## <a name="creating-input-samples"></a>Criando exemplos de entrada

Os exemplos de entrada para o codec de imagem de vídeo são estruturados. a definição da estrutura e das constantes usadas para a imagem de vídeo não está incluída nas interfaces Windows áudio de mídia e codec de vídeo. essas definições estão incluídas no sdk do formato de mídia do Windows, e seu uso é totalmente explicado na documentação do sdk do formato de mídia do Windows.

## <a name="decoding"></a>Decodificação

Não há requisitos especiais para decodificar vídeo de captura de tela. além de um subtipo diferente (MEDIASUBTYPE \_ WMVP) usado para entrada de decodificador, o fluxo de imagem de vídeo compactado é essencialmente idêntico a um fluxo de vídeo de mídia padrão Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 
