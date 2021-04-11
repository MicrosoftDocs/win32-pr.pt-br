---
description: Configurando codificação de áudio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configurando codificação de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164211"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Configurando codificação de áudio (Microsoft Media Foundation)

O codificador de áudio do Windows Media enumera todos os tipos de saída com suporte em seu formato completo. Recupere o tipo desejado chamando **IMediaObject:: GetOutputType** ou **IMFTransform:: GetAvailableOutputType** e, em seguida, defina o tipo recuperado, inalterado, como o tipo de saída chamando **IMediaObject:: SetOutputType** ou **IMFTransform:: SetOutputType**.

Os tipos de mídia de saída com suporte do codificador de áudio mudam conforme as propriedades do codificador são configuradas. Você deve configurar todas as propriedades do codificador que deseja usar antes de enumerar o tipo de saída.

Os modos de dois passos e VBR são compatíveis com os codificadores de áudio, mas são configurados de forma diferente de vídeo. Para obter mais informações, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).

Os tipos de entrada com suporte pelo codificador de áudio não estarão disponíveis até que você defina o tipo de saída. Se você chamar **IMediaObject:: GetInputType** ou **IMFTransform:: GetInputType** antes de definir um tipo de saída, o método retornará DMO \_ e não mais nenhum \_ tipo de \_ \_ MFT \_ e \_ nenhum mais, \_ \_ respectivamente. Depois que o tipo de saída é definido, o codificador enumera os tipos de entrada aos quais ele dá suporte para o tipo de saída selecionado.

Nenhuma reamostragem de áudio é executada pelo codificador de áudio do Windows Media. Isso significa que o tipo de saída do codificador e o tipo de entrada do codificador devem ter o mesmo número de canais, bits por amostra e taxa de amostragem. Para obter mais informações, consulte [localizando tipos de saída do codificador de áudio](findingaudioencoderoutputtypes.md).

> [!Note]  
>    Cada tipo de saída enumerado pelo codificador de áudio contém uma estrutura **WAVEFORMATEX** (apontada por **am \_ Media \_ Type. pbFormat**) com dados estendidos anexados a ela. O tamanho dos dados estendidos é especificado por **WAVEFORMATEX. cbSize**. Esses dados devem ser mantidos com o conteúdo codificado para que possam ser entregues ao decodificador. O conteúdo não pode ser descompactado sem os dados de formato estendido.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> </dl>

 

 



