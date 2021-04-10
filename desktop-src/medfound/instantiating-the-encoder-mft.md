---
description: Criando uma instância de um MFT do codificador
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Criando uma instância de um MFT do codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170520"
---
# <a name="instantiating-an-encoder-mft"></a>Criando uma instância de um MFT do codificador

Em Microsoft Media Foundation, os codificadores são implementados como [transformações de Media Foundation](media-foundation-transforms.md) (MFTs). Antes de criar um codificador, você deve primeiro encontrar o codificador mais adequado às suas necessidades.

-   Codecs de áudio do Windows Media

    Categoria: **\_ \_ \_ codificador de áudio de categoria de MFT**

    Tipo principal: \_ áudio MFMediaType

    Subtipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Codecs de vídeo do Windows Media

    Categoria: **\_ \_ \_ codificador de vídeo de categoria MFT**

    Tipo principal: \_ vídeo MFMediaType

    Subtipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

O Media Foundation fornece várias funções que seu aplicativo pode chamar para enumerar os vários codificadores disponíveis no seu sistema. Os codificadores são registrados como objetos COM e a entrada do registro segue o formato padrão para fábricas de classes COM. O registro mantém os CLSIDs para os codificadores, que são categorizados pelo formato de mídia (áudio ou vídeo). Os identificadores de classe dos codificadores de mídia do Windows são definidos como constantes no arquivo de cabeçalho wmcodecdsp. h. No Media Foundation, os codificadores podem ser registrados por meio de chamadas para [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) especificando o catergory, os tipos de entrada com suporte e os tipos de saída com suporte. Após o registro bem-sucedido por meio dessas funções, os MFTs são considerados pelas funções de enumeração de Media Foundation.

Para criar uma instância de um MFT do codificador, um aplicativo tem as seguintes opções.

-   Crie o MFT do codificador diretamente e receba um ponteiro para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Para obter mais informações, consulte [criando um codificador usando CoCreateInstance](using-an-encoder-s-imftransform--interface.md).
-   Crie uma instância do objeto de ativação para o MFT do codificador e receba um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Para obter mais informações, consulte [usando objetos de ativação de um codificador](using-an-encoder-s-activation-objects.md).

Se seu aplicativo estiver usando [componentes ASF da camada de pipeline](pipeline-layer-asf-components.md) para codificar um arquivo para o formato ASF, você deverá inserir o MFT do codificador no pipeline como um nó de transformação. Ao criar o nó de transformação na topologia de codificação, você pode definir o tipo de objeto como um ponteiro para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ou o objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . O Media Foundation fornece objetos de ativação para codificadores de mídia do Windows para que possam ser definidos convenientemente como o nó de transformação na topologia de codificação. Quando a topologia é resolvida, a sessão de mídia usa o objeto de ativação para criar uma instância do MFT do codificador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificadores de mídia do Windows](windows-media-encoders.md)
</dt> </dl>

 

 



