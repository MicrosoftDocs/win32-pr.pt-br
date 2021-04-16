---
description: Usando a categoria de imagem do Windows Media Video 9,1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Usando a categoria de imagem do Windows Media Video 9,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b545d37b61a1c89ffdd69615b28f636aa98b32
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105758187"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Usando a categoria de imagem do Windows Media Video 9,1

A categoria de imagem do Windows Media Video 9,1 é diferente das outras categorias de saída com suporte do codificador e do codificador do Windows Media Video 9. Em vez de processar vídeo descompactado, ele usa exemplos de entrada especiais que consistem em dados de transformação estruturados e, ocasionalmente, imagens de bitmap RGB nas quais as transformações são executadas.

O conteúdo codificado da imagem do vídeo 9,1 do Windows Media é praticamente idêntico ao conteúdo codificado regular do Windows Media Video 9, mas é identificado por seu próprio FOURCC ("WMVP").

O tipo de saída do codificador para imagem de vídeo é definido exatamente da mesma forma que o vídeo padrão do Windows Media, exceto que os valores de subtipo e de compactação devem ser definidos para os identificadores de imagem de vídeo. Isso inclui a necessidade de obter dados privados do codec e acrescentá-los à estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Para obter mais informações, consulte [Configurando a codificação de vídeo](configuringvideoencoding.md).

A configuração de tipo de entrada para imagem de vídeo também é muito semelhante à configuração de entrada para os outros codificadores de vídeo. Você pode recuperar um [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) parcialmente concluído do codificador chamando [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)ou se estiver usando o SDK do Media Foundation, chamando [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) e recuperando o tipo de **\_ mídia DMO \_** usando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). Em seguida, você define o tamanho do quadro e a estrutura do formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , assim como faria com o vídeo padrão. Assim como com o tipo de saída, você precisa garantir que os valores de subtipo e compactação sejam definidos adequadamente.

## <a name="creating-input-samples"></a>Criando exemplos de entrada

Os exemplos de entrada para o codec de imagem de vídeo são estruturados. A definição da estrutura e das constantes usadas para a imagem de vídeo não está incluída nas interfaces do codec de áudio e vídeo do Windows Media. Essas definições estão incluídas no Windows Media Format SDK, e seu uso é totalmente explicado na documentação do SDK do Windows Media Format.

## <a name="decoding"></a>Decodificação

Não há requisitos especiais para decodificar vídeo de captura de tela. Além de um subtipo diferente (MEDIASUBTYPE \_ WMVP) usado para entrada de decodificador, o fluxo de imagem de vídeo compactado é essencialmente idêntico a um fluxo de vídeo de mídia padrão do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 
