---
description: Configurando a codificação de vídeo
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: Configurando a codificação de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd82240ea9f540f283e0fb6340c06be00336226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089771"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>Configurando a codificação de vídeo (Microsoft Media Foundation)

Para configurar o codificador de vídeo, execute as seguintes etapas:

1.  Defina todas as propriedades no codificador DMO usando **IPropertyBag:: Write**. A lista a seguir resume o conjunto mínimo de propriedades que são necessárias para codificar um fluxo de vídeo CBR (todos esses valores têm padrões que podem ser usados):

    -   A propriedade[MFPKEY \_ VIDEOWINDOW](mfpkey-videowindowproperty.md) especifica a janela de buffer a ser usada para o fluxo. Para obter mais informações sobre a configuração de buffer do Windows e como ela afeta o conteúdo, consulte [métodos de codificação](encodingmethods.md). A janela de buffer padrão é de três segundos, que é apropriada para muitos cenários.
    -   A complexidade do vídeo é definida para determinar a compensação entre a qualidade do conteúdo codificado e o tempo necessário para a codificação. Se você não definir um valor, o valor padrão será usado. No entanto, você pode encontrar os modos recomendados para um codec específico chamando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar g \_ wszWMVCComplexityExLive, g \_ wszWMVCComplexityExOffline e g \_ wszWMVCComplexityExMax. Em seguida, você pode definir [MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md) como um valor entre 0 e a complexidade máxima relatada.
    -   [MFPKEY \_ CRISP](mfpkey-crispproperty.md) especifica a importância relativa da suavidade de vídeo e a qualidade da imagem de quadros codificados. Na maioria dos casos, o valor padrão funciona bem.
    -   Para conteúdo de vídeo armazenado em um contêiner diferente de ASF, a propriedade [MFPKEY \_ ASFOVERHEADPERFRAME](mfpkey-asfoverheadperframeproperty.md) deve ser definida como 0. Esse não é o valor padrão.

    Para obter informações sobre como configurar fluxos de VBR, consulte [usando a codificação de VBR](usingvbrencoding.md).

2.  Configure a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) para o tipo de entrada ou, se você estiver usando o SDK do Media Foundation, use a função [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) . Use uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) descrevendo o conteúdo de entrada descompactado. O codec não redimensiona o vídeo nem converte o espaço de cores.
3.  Defina o tipo de entrada usando [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) ou [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).
4.  Configure o tipo de saída para o codificador. Depois que o tipo de entrada é definido, o codificador enumera os tipos de saída que são concluídos, exceto o membro **dwBitrate** da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , ou o atributo de [**taxa de \_ \_ \_ bits média MF MT**](mf-mt-avg-bitrate-attribute.md) da interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Se você recuperar um tipo de saída antes de definir um tipo de entrada, a estrutura de [**\_ \_ tipo de mídia do DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) entregue não terá um **VIDEOINFOHEADER** associado.
5.  Recupere os dados privados do codec e acrescente-os à estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que você passa para a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) ou para [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype). Para obter mais informações, consulte [usando dados privados do codec de vídeo](usingvideocodecprivatedata.md).
6.  Defina o tipo de saída chamando o método [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) ou [**IMFTransform:: setoutputtypetype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . Passe a estrutura [**do \_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) com a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) concluída (incluindo dados privados acrescentados) referenciada no membro **pbFormat** ou Construa um [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) chamando [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader).

> [!Note]  
> O objeto codificador de vídeo dá suporte a duas saídas. A segunda saída é para o codificador "post View". Ele fornece os exemplos não compactados conforme eles serão entregues do decodificador. Isso permite que você monitore a qualidade da codificação sem precisar esperar até que todo o fluxo seja processado. Essa saída é opcional. Se você quiser usá-lo, configure seu tipo seguindo o mesmo processo usado para definir o tipo de entrada do codificador.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 
