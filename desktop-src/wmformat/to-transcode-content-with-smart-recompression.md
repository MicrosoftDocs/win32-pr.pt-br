---
title: Para transcodificar conteúdo com recompactação inteligente
description: Para transcodificar conteúdo com recompactação inteligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- SDK do Windows Media Format, transcodificação de conteúdo
- SDK do Windows Media Format, recompactação inteligente
- SDK do Windows Media Format, recompactação
- SDK do Windows Media Format, codecs de áudio do Windows Media
- Formato de sistema avançado (ASF), transcodificação de conteúdo
- ASF (formato de sistemas avançados), transcodificação de conteúdo
- Formato de sistema avançado (ASF), recompactação inteligente
- ASF (formato de sistemas avançados), recompactação inteligente
- Formato de sistema avançado (ASF), recompactação
- ASF (formato de sistemas avançados), recompactação
- Formato de sistema avançado (ASF), codecs de áudio do Windows Media
- ASF (formato de sistemas avançados), codecs de áudio do Windows Media
- transcodificação de conteúdo
- recompactação inteligente
- recompactação
- Codecs de áudio do Windows Media, transcodificação de conteúdo
- codecs, codecs de áudio do Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293778"
---
# <a name="to-transcode-content-with-smart-recompression"></a>Para transcodificar conteúdo com recompactação inteligente

Você pode transcodificar o conteúdo de uma taxa de bits para outra usando o SDK do Windows Media Format. Normalmente, isso envolve simplesmente decodificar o conteúdo e codificá-lo novamente para a taxa de bits desejada. O codec Windows Media Audio 9 dá suporte à recompactação inteligente, o que permite transcodificação que atinge uma qualidade melhor do que o normal.

Para a recompactação inteligente, o fluxo de áudio original deve ser codificado com o codec de áudio do Windows Media. Todas as versões do codec têm suporte, mas os codecs de áudio especializados (Windows Media Audio 9 Professional e Windows Media Audio 9 Voice) não são. Se o áudio original foi codificado com o codec Windows Media Audio 9 sem perdas, não há necessidade de usar a recompactação inteligente, pois nenhuma informação foi perdida na codificação original.

Para usar a recompactação inteligente, execute as etapas a seguir.

1.  Configure um objeto de leitor com o arquivo de origem para leitura. Para obter mais informações, consulte [lendo arquivos ASF](reading-asf-files.md).
2.  Configure um objeto gravador a ser usado para transcodificar o arquivo. Defina o nome do arquivo para o novo arquivo. Selecione um perfil a ser usado para o novo arquivo. Defina o perfil selecionado no objeto gravador. Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).
3.  Obtenha um ponteiro para a interface [**IWMProfile**](iwmprofile.md) do objeto leitor chamando **IWMReader:: QueryInterface**.
4.  Recupere a interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) para que o fluxo de áudio seja transcodificado chamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).
5.  Obtenha a interface [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) para o objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.
6.  Recupere a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o fluxo fazendo duas chamadas para [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Obtenha o tamanho da estrutura na primeira chamada e aloque a memória de um buffer para passar na segunda chamada.
7.  Obtenha um ponteiro para a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para a entrada no gravador chamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
8.  Obtenha a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) para o objeto de propriedades de mídia de entrada chamando **IWMInputMediaProps:: QueryInterface**.
9.  Use o método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para definir a \_ Propriedade g wszOriginalWaveFormat. Use a estrutura **WAVEFORMATEX** obtida na etapa 6 como o valor da propriedade.
10. Inclua alterações feitas nas propriedades de mídia de entrada chamando [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passando um ponteiro para a interface **IWMInputMediaProps** .
11. Comece a ler exemplos do arquivo original e passá-los para o gravador com chamadas para [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**Interface IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**Interface IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**Interface IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




