---
description: Saiba mais sobre o filtro de leitor ASF do WM para DirectShow. este é um filtro de wrapper para o objeto leitor que é fornecido com o SDK do formato de mídia Windows.
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Filtro de leitor ASF do WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e87642637e7a210707c049d9b3c6a1a431b0a277774ce432b1c5c962ff2f317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049156"
---
# <a name="wm-asf-reader-filter-directshow"></a>Filtro de leitor ASF do WM (DirectShow)

o leitor ASF do WM é um filtro de wrapper para o objeto leitor fornecido com o SDK do formato de mídia Windows e é o filtro de origem recomendado para reprodução de arquivo de conteúdo baseado em mídia Windows e conteúdo criado com qualquer um dos DMOs de codificador MPEG-4 da Microsoft.



| Rótulo | Valor |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** além disso, o filtro expõe as seguintes Windows interfaces SDK do formato de mídia: [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (por meio de **IServiceProvider**)<br/> |
| Tipos de mídia de pino de entrada                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Interfaces de pino de entrada                     | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, \_ áudio de MEDIATYPE, MediaType \_ ScriptCommand, \_ FileTransfer de MediaType                                                                                                                                                                                                                                                                                                                                                                                                     |
| Interfaces de pino de saída                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider** além disso, os pins expõem as seguintes Windows interfaces SDK do formato de mídia: **IWMStreamConfig2** (por meio de **IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| CLSID do filtro                             | \_WMASFREADER CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Executável                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Núcleo](merit.md)                       | MÉRITO \_ improvável                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

Ao receber o nome de um arquivo ASF ou uma URL, o leitor ASF do WM lê o conteúdo compactado, analisa os fluxos compactados e expõe um pino de saída para cada um. Esse filtro conecta os filtros downstream aos codecs de áudio e/ou vídeo, que fazem a descompactação. A busca será suportada se o arquivo ASF for pesquisável. O tempo do leitor ASF carimba os exemplos antes de enviá-los para downstream, mas não modifica os carimbos de data/hora de forma alguma.

Não há suporte para a reprodução em velocidades diferentes de 1,0 (conforme especificado em [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)).

quando o tempo de execução do SDK do formato de mídia do Windows envia mensagens de [**\_ STATUS WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) para o filtro de gravador ASF do WM, o filtro encaminha todas as mensagens relacionadas à aquisição de licença do DRM como eventos de [**\_ \_ evento do EC WMT**](ec-wmt-event.md) . Para obter mais informações, consulte [lendo DRM-Protected arquivos ASF no DirectShow](reading-drm-protected-asf-files-in-directshow.md).

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

[DirectShow Filter](directshow-filters.md)
</dt> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
