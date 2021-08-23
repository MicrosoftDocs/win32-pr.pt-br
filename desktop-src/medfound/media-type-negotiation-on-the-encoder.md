---
description: Negociação de tipo de mídia no codificador
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: Negociação de tipo de mídia no codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ac5dd5a107633feba4ce2a74da7e9aea7e9f71d51be1b5cad5b85ab4adda35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941506"
---
# <a name="media-type-negotiation-on-the-encoder"></a>Negociação de tipo de mídia no codificador

Em Microsoft Media Foundation, os codificadores são implementados como [transformações de Media Foundation](media-foundation-transforms.md) (MFTs) com uma entrada e uma saída. Antes de uma sessão de codificação, um codificador precisa saber as características do fluxo que ele receberá como entrada e o formato do fluxo que ele produzirá como saída. Você deve definir os tipos de mídia de entrada e saída e as características relacionadas antes de passar os dados por meio do codificador. Você deve fornecer os formatos de entrada e saída especificando os [GUIDs de tipo de mídia](media-type-guids.md) apropriados e definir as características do fluxo de saída definindo os [atributos de tipo de mídia](media-type-attributes.md) relevantes no tipo de mídia de saída. Um codificador instanciado recentemente não tem nenhum tipo de mídia definido.

O tipo de mídia de entrada é um formato descompactado, como áudio PCM ou vídeo RGB. Os tipos de formato usados pelo codificador são limitados aos descritos pelas estruturas **VIDEOINFOHEADER** e **WAVEFORMATEX** . para obter mais informações sobre essas estruturas, consulte a documentação do SDK do Windows. O Media Foundation fornece funções auxiliares para criar tipos de mídia a partir de estruturas de formato. Por exemplo, a função [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) Inicializa um tipo de vídeo de uma estrutura **VIDEOINFOHEADER** e a função [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) Inicializa um tipo de vídeo de uma estrutura **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE** . Para obter mais informações, consulte [conversões de tipo de mídia](media-type-conversions.md). Você deve definir o tipo de mídia de entrada no codificador chamando [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

O tipo de mídia de saída é o formato de compactação usado no arquivo ou fluxo de origem final. Você pode definir o tipo de mídia de saída disponível somente depois de definir o tipo de mídia de entrada. Você pode recuperar os tipos de saída com suporte chamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) em um loop até que o codificador retorne o **MF \_ E \_ não \_ mais \_ tipos**. Incrementar o índice de tipo com cada iteração. Quando encontrar um tipo de mídia apropriado, defina o tipo de mídia de saída chamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

O fator decisivo na escolha do tipo de mídia de saída depende do tipo de codificação e dos requisitos de codificação. Por exemplo, para fluxos de áudio que são codificados em CBR, você deseja encontrar um tipo de mídia que corresponde à sua entrada e tem uma taxa de bits mais próxima possível de um valor de destino.

Se você quiser usar um modo de codificação diferente de CBR, deverá definir o modo e, em seguida, enumerar os tipos de saída para esse modo, pois o codificador altera os tipos de saída com suporte, dependendo do conjunto de modos. As propriedades que controlam o modo de codificação são [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) e [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md). Por exemplo, se você estiver enumerando tipos de saída para codificação de qualidade VBR, o tipo de mídia dependerá do valor de qualidade que você decidir usar. Para obter informações sobre como definir essas propriedades, consulte [Propriedades de codificação](configuring-the-encoder.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma instância de um MFT do codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores de mídia](windows-media-encoders.md)
</dt> </dl>

 

 



