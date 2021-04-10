---
description: Filtro de leitor ASF do WM
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Filtro de leitor ASF do WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df563667ed614a238e8fb31e08a2d71c721c2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169878"
---
# <a name="wm-asf-reader-filter-directshow"></a>Filtro de leitor ASF do WM (DirectShow)

O leitor ASF do WM é um filtro de wrapper para o objeto leitor fornecido com o Windows Media Format SDK e é o filtro de origem recomendado para reprodução de arquivo de conteúdo baseado no Windows Media e conteúdo criado com qualquer um dos DMOs do codificador MPEG-4 da Microsoft.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** além disso, o filtro expõe as seguintes interfaces SDK do Windows Media Format: [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), IWMReaderAdvanced [**, IWMReaderAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (por meio de **IServiceProvider**) [](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)<br/> |
| Tipos de mídia de pino de entrada                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Interfaces de pino de entrada                     | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, \_ áudio de MEDIATYPE, MediaType \_ ScriptCommand, \_ FileTransfer de MediaType                                                                                                                                                                                                                                                                                                                                                                                                     |
| Interfaces de pino de saída                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider** além disso, os Pins expõem as seguintes interfaces do SDK do Windows Media Format: **IWMStreamConfig2** (por meio de **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| CLSID do filtro                             | \_WMASFREADER CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Executável                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Núcleo](merit.md)                       | MÉRITO \_ improvável                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

Ao receber o nome de um arquivo ASF ou uma URL, o leitor ASF do WM lê o conteúdo compactado, analisa os fluxos compactados e expõe um pino de saída para cada um. Esse filtro conecta os filtros downstream aos codecs de áudio e/ou vídeo, que fazem a descompactação. A busca será suportada se o arquivo ASF for pesquisável. O tempo do leitor ASF carimba os exemplos antes de enviá-los para downstream, mas não modifica os carimbos de data/hora de forma alguma.

Não há suporte para a reprodução em velocidades diferentes de 1,0 (conforme especificado em [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)).

Quando o tempo de execução do SDK do Windows Media Format envia mensagens de [**\_ status WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) para o filtro de gravador ASF do WM, o filtro encaminha todas as mensagens relacionadas à aquisição de licença do DRM como eventos de [**\_ \_ evento do EC WMT**](ec-wmt-event.md) . Para obter mais informações, consulte [lendo DRM-Protected arquivos ASF no DirectShow](reading-drm-protected-asf-files-in-directshow.md).

O leitor ASF do WM implementa parcialmente as interfaces [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) e [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) para fornecer aos aplicativos acesso aos métodos informativos no objeto Reader. A implementação do filtro simplesmente passa as chamadas para a interface no objeto leitor. Os métodos de streaming não são implementados porque o filtro deve ter controle total sobre o processo de streaming. Os seguintes métodos são implementados:

-   [**IWMReaderAdvanced:: getstatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2:: getplaymode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2:: getprotocolname**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2:: SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
