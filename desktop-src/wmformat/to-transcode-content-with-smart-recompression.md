---
title: Para transcodificar conteúdo com recompactação inteligente
description: Para transcodificar conteúdo com recompactação inteligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows SDK de Formato de Mídia, transcodificação de conteúdo
- Windows SDK de Formato de Mídia, recompactação inteligente
- Windows SDK de Formato de Mídia, recompactação
- Windows SDK de formato de mídia, Windows de áudio de mídia
- ASF (Advanced Systems Format), transcodificação de conteúdo
- ASF (Formato de Sistemas Avançados), transcodificação de conteúdo
- ASF (Advanced Systems Format), recompactação inteligente
- ASF (Formato de Sistemas Avançados), recompactação inteligente
- ASF (Advanced Systems Format), recompression
- ASF (Formato de Sistemas Avançados),recompactação
- ASF (Advanced Systems Format), Windows de áudio de mídia
- ASF (formato de sistemas avançados), Windows de áudio de mídia
- transcodificação de conteúdo
- recompactação inteligente
- Recompressão
- Windows Codecs de áudio de mídia, transcodificação de conteúdo
- codecs,Windows de áudio de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1cf363e196feca81ef9757f006b211758c2ff7fbdd1f50b5136992b394f8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699087"
---
# <a name="to-transcode-content-with-smart-recompression"></a>Para transcodificar conteúdo com recompactação inteligente

Você pode transcodificar o conteúdo de uma taxa de bits para outra usando o SDK Windows Formato de Mídia. Normalmente, isso envolve simplesmente decodificar o conteúdo e codificá-lo novamente para a taxa de bits desejada. O codec Windows Media Audio 9 dá suporte à recompactação inteligente, que permite a transcodificação que atinge uma qualidade melhor do que a normal.

Para recompactação inteligente, o fluxo de áudio original deve ser codificado com o codec Windows Media Audio. Todas as versões do codec têm suporte, mas os codecs de áudio especializados (Windows Media Audio 9 Professional e Windows Media Audio 9 Voice) não são. Se o áudio original tiver sido codificado com o codec sem perda do Windows Media Audio 9, não será necessário usar a recompactação inteligente, pois nenhuma informação foi perdida na codificação original.

Para usar a recompactação inteligente, execute as etapas a seguir.

1.  Configurar um objeto de leitor com o arquivo de origem para leitura. Para obter mais informações, consulte [Lendo arquivos ASF](reading-asf-files.md).
2.  Configurar um objeto writer a ser usado para transcodificar o arquivo. De definir o nome do arquivo para o novo arquivo. Selecione um perfil a ser usado para o novo arquivo. De acordo com o perfil selecionado no objeto writer. Para obter mais informações, consulte [Escrevendo arquivos ASF](writing-asf-files.md).
3.  Obter um ponteiro para a interface [**IWMProfile**](iwmprofile.md) do objeto de leitor chamando **IWMReader::QueryInterface**.
4.  Recupere a interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) para que o fluxo de áudio seja transcodificado chamando [**IWMProfile::GetStream.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)
5.  Obter a interface [**IWMMediaProps para**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) o objeto de configuração de fluxo chamando **IWMStreamConfig::QueryInterface**.
6.  Recupere a [**estrutura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o fluxo fazendo duas chamadas para [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Obter o tamanho da estrutura na primeira chamada e alocar memória para um buffer passar na segunda chamada.
7.  Obter um ponteiro para a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para a entrada no autor chamando [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
8.  Obter a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) para o objeto de propriedades de mídia de entrada chamando **IWMInputMediaProps::QueryInterface**.
9.  Use o [**método IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para definir a propriedade g \_ wszOriginalWaveFormat. Use a **estrutura WAVEFORMATEX** obtida na etapa 6 como o valor da propriedade .
10. Inclua as alterações feitas nas propriedades da mídia de entrada chamando [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passando um ponteiro para a interface **IWMInputMediaProps.**
11. Comece a ler exemplos do arquivo original e passá-los para o autor com chamadas para [**IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**IWMInputMediaProps Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**IWMMediaProps Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMProfile Interface**](iwmprofile.md)
</dt> <dt>

[**IWMPropertyVault Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**IWMStreamConfig Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




