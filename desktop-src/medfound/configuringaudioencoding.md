---
description: Configurando a codificação de áudio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configurando a codificação de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2344808decffd4b50d5926074dbf71d60445580adb4556703367369e1e146d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880361"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Configurando a codificação de áudio (Microsoft Media Foundation)

O Windows codificador de Áudio de Mídia enumera todos os seus tipos de saída com suporte em sua forma completa. Recupere o tipo que você deseja chamando **IMediaObject::GetOutputType** ou **IMFTransform::GetAvailableOutputType** e, em seguida, de definido o tipo recuperado, inalterado, como o tipo de saída chamando **IMediaObject::SetOutputType** ou **IMFTransform::SetOutputType**.

Os tipos de mídia de saída com suporte pelo codificador de áudio mudam conforme as propriedades do codificador são configuradas. Você deve configurar todas as propriedades do codificador que deseja usar antes de enumerar o tipo de saída.

Os modos de duas pass e VBR têm suporte dos codificadores de áudio, mas são configurados de maneira diferente do vídeo. Para obter mais informações, [consulte Enumerando tipos de áudio para modos de codificação específicos.](enumeratingaudiotypesforspecificencodingmodes.md)

Os tipos de entrada com suporte pelo codificador de áudio não estarão disponíveis até que você de definido o tipo de saída. Se você chamar **IMediaObject::GetInputType** ou **IMFTransform::GetInputType** antes de definir um tipo de saída, o método retornará DMO E NO MORE ITEMS ou \_ \_ \_ \_ MFT \_ E NO \_ MORE \_ \_ TYPES, respectivamente. Depois que o tipo de saída é definido, o codificador enumera os tipos de entrada aos quais ele dá suporte para o tipo de saída selecionado.

Nenhuma resamplagem de áudio é executada pelo codificador Windows Media Audio. Isso significa que o tipo de saída do codificador e o tipo de entrada do codificador devem ter o mesmo número de canais, bits por exemplo e taxa de amostra. Para obter mais informações, consulte [Localizar tipos de saída do codificador de áudio](findingaudioencoderoutputtypes.md).

> [!Note]  
>    Cada tipo de saída enumerado pelo codificador de áudio contém uma estrutura **WAVEFORMATEX** (apontada por **AM MEDIA \_ \_ TYPE.pbFormat**) com dados estendidos anexados a ela. O tamanho dos dados estendidos é especificado por **WAVEFORMATEX.cbSize.** Esses dados devem ser mantidos com o conteúdo codificado para que possam ser entregues ao decodificador. O conteúdo não pode ser descompactado sem os dados de formato estendido.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> </dl>

 

 



