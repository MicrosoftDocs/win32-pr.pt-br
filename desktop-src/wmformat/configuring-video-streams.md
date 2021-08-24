---
title: configurando Fluxos de vídeo
description: configurando Fluxos de vídeo
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- fluxos, configurando fluxos de vídeo
- codecs, configurando fluxos de vídeo
- fluxos de vídeo, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bc6e011f32d1ea9a9905c718ad8ff0c13f7d57650a30316ecfec6332978fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809586"
---
# <a name="configuring-video-streams"></a>configurando Fluxos de vídeo

Os fluxos de vídeo são mais flexíveis em sua configuração do que os fluxos de áudio. Isso ocorre porque as propriedades dos quadros que compõem o vídeo podem variar muito de um arquivo para o outro. Ao recuperar o formato de codec para o codec que você está usando, você deve definir os valores a seguir para objetos de configuração de fluxo de vídeo.



| Valor                                 | Descrição                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Taxa de bits                              | Chame [**IWMStreamConfig:: settaxa de bits**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) para definir como o valor desejado. O codec de vídeo tentará compactar a mídia para atender às suas especificações. Se os valores forem muito baixos, o vídeo compactado resultante será muito degradado.           |
| Janela de buffer                         | Chame [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) para definir o valor desejado. O codec de vídeo tentará compactar a mídia para atender às suas especificações. Se os valores forem muito baixos, o vídeo compactado resultante será muito degradado. |
| **WMVIDEOINFOHEADER.rcSource**        | O canto superior esquerdo deve ser definido como 0, 0. O canto inferior direito deve ser definido para as dimensões do quadro. Por exemplo, em um fluxo de 640x480, essas configurações seriam 0, 0640480.                                                                                                |
| **WMVIDEOINFOHEADER.rcTarget**        | Deve corresponder a **rcSource**.                                                                                                                                                                                                                                                    |
| **WMVIDEOINFOHEADER.dwBitRate**       | Deve corresponder à taxa de bits definida para o fluxo.                                                                                                                                                                                                                                 |
| **WMVIDEOINFOHEADER. AvgTimePerFrame** | Defina para o tempo aproximado por quadro.                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER. bilargura**          | Defina para a largura, em pixels, do tamanho do quadro desejado.                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER. biHeight**         | Defina para a altura, em pixels, do tamanho do quadro desejado.                                                                                                                                                                                                                    |



 

O conteúdo de vídeo não é reproduzido corretamente, a menos que esteja codificado para um tamanho que seja um múltiplo de quatro para largura e altura. A exceção é um vídeo [*RGB*](wmformat-glossary.md) descompactado, que pode ser qualquer tamanho. Se você tentar definir um tamanho que não seja um múltiplo de quatro, um dos seguintes erros será retornado pelo gravador:

-   \_formato de \_ \_ entrada inválido \_ do NS E
-   \_formato de saída NS E \_ inválido \_ \_
-   NS \_ E \_ INVALIDPROFILE

Se você estiver usando a codificação de taxa de bits variável, talvez seja necessário fazer outros ajustes. para obter mais informações, consulte [configuring VBR Fluxos](configuring-vbr-streams.md).

alguns codecs de vídeo de mídia Windows dão suporte a vários níveis de complexidade. Os níveis de complexidade determinam os algoritmos que o codec usará ao codificar um fluxo de vídeo. O uso de um nível de complexidade alta exigirá mais capacidade de processamento para codificação e decodificação.

Cada codec que dá suporte às configurações de complexidade expõe as seguintes configurações que você pode recuperar com o método [**IWMCodecInfo3:: GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .



| Configuração                 | Descrição                                         |
|-------------------------|-----------------------------------------------------|
| g \_ wszComplexityMax     | O nível de qualidade máximo suportado pelo codec.   |
| g \_ wszComplexityOffline | O nível de qualidade sugerido para reprodução offline.   |
| g \_ wszComplexityLive    | O nível de qualidade sugerido para reprodução de streaming. |



 

Para definir a complexidade de um fluxo de vídeo em um perfil, use o método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) usando a propriedade g \_ wszComplexity. O valor definido deve ser menor ou igual à complexidade máxima com suporte para o codec.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configuração comum a todos os Fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**configurando Fluxos**](configuring-streams.md)
</dt> <dt>

[**Configurações de complexidade de vídeo**](video-complexity-settings.md)
</dt> </dl>

 

 




