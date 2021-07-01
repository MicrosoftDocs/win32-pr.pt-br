---
description: Saiba mais sobre o filtro Leitor do WM ASF para DirectShow. Este é um filtro wrapper para o objeto de leitor fornecido com o SDK Windows Media Format dados.
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Filtro de Leitor do WM ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330ab870b97fc3e84ccb5b0f726d4f35ef1af147
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118661"
---
# <a name="wm-asf-reader-filter-directshow"></a>Filtro de Leitor do WM ASF (DirectShow)

O Leitor do WM ASF é um filtro de wrapper para o objeto de leitor fornecido com o SDK do Windows Media Format e é o filtro de origem recomendado para reprodução de arquivo de conteúdo baseado em Mídia do Windows e conteúdo criado com qualquer um dos DMOs do Codificador do Microsoft MPEG-4.



| Rótulo | Valor |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) [**IAMExtendedSeeking,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking) **IServiceProvider** Além disso, o filtro expõe as seguintes interfaces do SDK do Windows Media Format: [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (por meio **de IServiceProvider**)<br/> |
| Tipos de mídia de pino de entrada                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Interfaces de pino de entrada                     | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipos de mídia de pino de saída                   | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| Interfaces de pino de saída                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider** Além disso, os pinos expõem as seguintes interfaces do SDK do Windows Media Format: **IWMStreamConfig2** (por meio **de IServiceProvider**)<br/>                                                                                                                                                                                                                                    |
| Filtrar CLSID                             | CLSID \_ WMAsfReader                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID da página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Executável                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Mérito](merit.md)                       | IMPROVÁVEL DE \_ VERÃO                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

Quando dado o nome de um arquivo ASF ou uma URL, o Leitor do WM ASF lê o conteúdo compactado, analisado os fluxos compactados e expõe um pino de saída para cada um deles. Esse filtro conecta downstream a filtros de codecs de áudio e/ou vídeo, que fazem a descompactação. A busca será suportada se o arquivo ASF for buscado. O horário do Leitor do ASF marca os exemplos antes de enviá-los downstream, mas não modifica os carimbos de data/hora de forma alguma.

Não há suporte para reprodução em velocidades que não 1.0 (conforme especificado em [**IMediaSeeking::SetRate).**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)

Quando o runtime do SDK do Windows Media Format envia mensagens [**\_ WMT STATUS**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) para o filtro Wm ASF Writer, o filtro encaminha todas as mensagens relacionadas à aquisição de licença DRM como eventos [**EC \_ WMT \_ EVENT.**](ec-wmt-event.md) Para obter mais informações, consulte [Leitura DRM-Protected arquivos ASF no DirectShow](reading-drm-protected-asf-files-in-directshow.md).

O Leitor do WM ASF implementa parcialmente as interfaces [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) e [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) para dar aos aplicativos acesso aos métodos informacionais no objeto de leitor. A implementação do filtro simplesmente passa as chamadas para a interface no objeto de leitor. Os métodos de streaming não são implementados porque o filtro deve ter controle total sobre o processo de streaming. Os seguintes métodos são implementados:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
