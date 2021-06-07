---
title: Filtro de Leitor do WM ASF (Windows Media Format SDK 11)
description: Saiba mais sobre o filtro leitor do WM ASF.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, Leitor do WM ASF
- DirectShow, Leitor do WM ASF
- Filtros QASF, Leitor do WM ASF
- Leitor do WM ASF
- AsF (Advanced Systems Format), WM ASF Reader
- ASF (formato de sistemas avançados), leitor do WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444277"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>Filtro de Leitor do WM ASF (Windows Media Format SDK 11)

Quando dado o nome de um arquivo ASF ou uma URL, o Leitor do WM ASF lê o conteúdo compactado, analisado os fluxos e expõe um pino de saída para cada um deles. Esse filtro conecta-se downstream aos DMOs de Áudio de Mídia do Windows ou Vídeo de Mídia do Windows, que fazem a descompactação. A busca será suportada se o arquivo ASF for buscado. O Leitor do WM ASF aplica carimbos de data/hora aos exemplos de mídia com base no carimbo de data/hora no arquivo ASF, mas não modifica os carimbos de data/hora de forma alguma. Internamente, o filtro usa o Windows Media Format de leitura para ler o conteúdo baseado em Mídia do Windows.

> [!Note]  
> No SDK do DirectX, esse filtro não é o filtro de origem padrão para arquivos ASF, portanto, com esse SDK, você não pode usar esse filtro com o **método RenderFile;** você deve adicioná-lo explicitamente ao grafo de filtro usando seu CLSID (identificador de classe). Esse comportamento é diferente com o Windows Media Format SDK. Quando você instala as bibliotecas de runtime Windows Media Format SDK, o Leitor do WM ASF é registrado como o filtro padrão para arquivos ASF.

 

A tabela a seguir contém informações sobre o filtro leitor do WM ASF, como as interfaces e tipos de mídia aos quais ele dá suporte.



|  Informações de filtro                      |  Tipos                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro      | **IBaseFilter,** **IFileSourceFilter,** **IServiceProvider,** **IWMHeaderInfo,** **IWMReaderAdvanced** (parcialmente implementado. Consulte Comentários.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (por **meio de IServiceProvider**) |
| Tipos de mídia de pino de entrada  | Não aplicável                                                                                                                                                                                                                                |
| Interfaces de pino de entrada   | Não aplicável                                                                                                                                                                                                                                |
| Tipos de mídia de pino de saída | MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer                                                                                                                                                         |
| Tipo de formato            | **VIDEOINFOHEADER2** se o conteúdo estiver [*entrelaçado;*](wmformat-glossary.md)caso contrário, **VIDEOINFOHEADER**                                                                                                                    |
| Interfaces de pino de saída  | **IMediaSeeking,** **IAMWMBufferPass,** **IServiceProvider,** **IWMStreamConfig2** (por **meio de IServiceProvider**)                                                                                                                             |
| Filtrar CLSID           | CLSID \_ WMAsfReader                                                                                                                                                                                                                            |
| CLSID da página de propriedades    | Nenhuma página de propriedades                                                                                                                                                                                                                              |
| Executável             | Qasf.dll                                                                                                                                                                                                                                      |
| Mérito                  | IMPROVÁVEL DE \_ VERÃO                                                                                                                                                                                                                               |
| Categoria de filtro        | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

O Leitor do WM ASF implementa parcialmente as interfaces **IWMReaderAdvanced** e **IWMReaderAdvanced2** para dar aos aplicativos acesso aos métodos informacionais no objeto de leitor. A implementação do filtro simplesmente passa as chamadas para a interface no objeto de leitor. Os métodos de streaming não são implementados porque o filtro deve ter controle total sobre o processo de streaming. Os seguintes **métodos IWMReaderAdvanced** **e IWMReaderAdvanced2** são implementados:

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de QASF do DirectShow**](directshow-qasf-reference.md)
</dt> <dt>

[**Lendo arquivos ASF no DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




