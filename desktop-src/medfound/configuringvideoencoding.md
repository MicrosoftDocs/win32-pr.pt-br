---
description: Configurando a codificação de vídeo
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: Configurando a codificação de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c6cb95a0bbe13ac9311bd55d45c67b3bcf4d0fc671fc6e6a6c3731081c2e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974835"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>Configurando a codificação de vídeo (Microsoft Media Foundation)

Para configurar o codificador de vídeo, execute as seguintes etapas:

1.  De acordo com as propriedades do codificador DMO usando **IPropertyBag::Write**. A lista a seguir resume o conjunto mínimo de propriedades necessárias para codificar um fluxo de vídeo CBR (todos esses valores têm padrões que podem ser usados):

    -   A[propriedade \_ VIDEOWINDOW MFPKEY](mfpkey-videowindowproperty.md) especifica a janela de buffer a ser usada para o fluxo. Para obter mais informações sobre a configuração de janelas de buffer e como ela afeta o conteúdo, consulte [Métodos de codificação](encodingmethods.md). A janela de buffer padrão é de três segundos, o que é apropriado para muitos cenários.
    -   A complexidade do vídeo é definida para determinar a diferença entre a qualidade do conteúdo codificado e o tempo necessário para codificar. Se você não definir um valor, o valor padrão será usado. No entanto, você pode encontrar os modos recomendados para um codec específico chamando [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar g \_ wszWMVCComplexityExLive, g \_ wszWMVCComplexityExOffline e g \_ wszWMVCComplexityExMax. Em seguida, você pode [definir MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md) como um valor entre 0 e a complexidade máxima relatada.
    -   [MFPKEY \_ O COD](mfpkey-crispproperty.md) especifica a importância relativa da suavidade de vídeo e a qualidade da imagem de quadros codificados. Na maioria dos casos, o valor padrão funciona bem.
    -   Para conteúdo de vídeo armazenado em um contêiner diferente de ASF, a propriedade [ \_ MFPKEY ASFOVERHEADPERFRAME](mfpkey-asfoverheadperframeproperty.md) deve ser definida como 0. Esse não é o valor padrão.

    Para obter informações sobre como configurar fluxos VBR, consulte [Using VBR Encoding](usingvbrencoding.md).

2.  Configure a [**estrutura DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) para o tipo de entrada ou, se você estiver usando o SDK do Media Foundation, use a [**função MFInitMediaTypeFromVideoInfoHeader.**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) Use uma [**estrutura VIDEOINFOHEADER que**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) descreve o conteúdo de entrada descompactado. O codec não resize o vídeo nem converte o espaço de cores.
3.  De definir o tipo de entrada [**usando IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) ou [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).
4.  Configure o tipo de saída para o codificador. Depois que o tipo de entrada é definido, o codificador enumera os tipos de saída completos, exceto o **membro dwBitrate** da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou o atributo [**\_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) da interface [**IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Se você recuperar um tipo de saída antes de definir um tipo de entrada, a estrutura DMO [**\_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) não terá um **VIDEOINFOHEADER associado.**
5.  Recupere os dados particulares do codec e adeque-os à estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que você passa para a estrutura [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) ou para [**IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Para obter mais informações, consulte [Using Video Codec Private Data](usingvideocodecprivatedata.md).
6.  De definir o tipo de saída chamando o [**método IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) [**ou IMFTransform::SetOutputType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) Passe a estrutura [**DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) com a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) concluída (incluindo dados privados anexados) referenciada no membro **pbFormat** ou construa [**um IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) chamando [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader).

> [!Note]  
> O objeto do codificador de vídeo dá suporte a duas saídas. A segunda saída é para o codificador "post view". Ele fornece as amostras descompactadas, pois elas serão entregues do decodificador. Isso permite que você monitore a qualidade da codificação sem precisar esperar até que todo o fluxo seja processado. Essa saída é opcional. Se você quiser usá-lo, configure seu tipo seguindo o mesmo processo usado para definir o tipo de entrada do codificador.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 
