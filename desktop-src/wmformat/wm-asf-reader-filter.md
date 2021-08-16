---
title: filtro de leitor de ASF do WM (SDK do formato de mídia do Windows 11)
description: saiba mais sobre o filtro de leitor ASF do WM para o SDK do Windows Media Format 11. Examine as informações de filtro e consulte os tópicos relacionados.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows SDK do formato de mídia, leitor de ASF do WM
- DirectShow, leitor de ASF do WM
- Filtros de QASF, leitor de ASF do WM
- Leitor ASF do WM
- ASF (Advanced Systems Format), leitor ASF do WM
- ASF (formato de sistemas avançados), leitor ASF do WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c825835e6d838a8a5d9b058f8bcf6ef52bd2a3d6a645787e0cf44da0f7573c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844919"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>filtro de leitor de ASF do WM (SDK do formato de mídia do Windows 11)

Ao receber o nome de um arquivo ASF ou uma URL, o leitor ASF do WM lê o conteúdo compactado, analisa os fluxos e expõe um pino de saída para cada um. esse filtro conecta o downstream à Windows vídeo de mídia de áudio ou Windows media DMOs, que faz a descompactação. A busca será suportada se o arquivo ASF for pesquisável. O leitor de ASF do WM aplica carimbos de data/hora aos exemplos de mídia com base no carimbo de data/hora no arquivo ASF, mas não modifica os carimbos de data/hora de nenhuma forma. internamente, o filtro usa o objeto leitor de formato de mídia Windows para ler o conteúdo baseado em mídia Windows.

> [!Note]  
> No SDK do DirectX, esse filtro não é o filtro de origem padrão para arquivos ASF, de modo que com esse SDK você não pode usar esse filtro com o método **RenderFile** ; Você deve adicioná-lo explicitamente ao grafo de filtro usando seu CLSID (identificador de classe). esse comportamento é diferente com o SDK do formato de mídia Windows. quando você instala as bibliotecas de tempo de execução do SDK do formato de mídia Windows, o leitor ASF do WM é registrado como o filtro padrão para arquivos ASF.

 

A tabela a seguir contém informações sobre o filtro de leitor ASF do WM, como as interfaces e os tipos de mídia aos quais ele dá suporte.



|  Informações de filtro                      |  Tipos                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces      | **IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (parcialmente implementado. Consulte comentários.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (por meio de **IServiceProvider**) |
| Tipos de mídia de pino de entrada  | Não se aplica                                                                                                                                                                                                                                |
| Interfaces de pino de entrada   | Não se aplica                                                                                                                                                                                                                                |
| Tipos de mídia do pino de saída | \_Vídeo de MediaType, \_ áudio de MEDIATYPE, MediaType \_ ScriptCommand, \_ FileTransfer de MediaType                                                                                                                                                         |
| Tipo de formato            | **VIDEOINFOHEADER2** se o conteúdo estiver [*entrelaçado*](wmformat-glossary.md), caso contrário **VIDEOINFOHEADER**                                                                                                                    |
| Interfaces de pino de saída  | **IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (por meio de **IServiceProvider**)                                                                                                                             |
| CLSID do filtro           | \_WMASFREADER CLSID                                                                                                                                                                                                                            |
| CLSID de página de propriedades    | Nenhuma página de propriedades                                                                                                                                                                                                                              |
| Executável             | Qasf.dll                                                                                                                                                                                                                                      |
| Núcleo                  | MÉRITO \_ improvável                                                                                                                                                                                                                               |
| Categoria do filtro        | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

O leitor ASF do WM implementa parcialmente as interfaces **IWMReaderAdvanced** e **IWMReaderAdvanced2** para fornecer aos aplicativos acesso aos métodos informativos no objeto Reader. A implementação do filtro simplesmente passa as chamadas para a interface no objeto leitor. Os métodos de streaming não são implementados porque o filtro deve ter controle total sobre o processo de streaming. Os seguintes métodos **IWMReaderAdvanced** e **IWMReaderAdvanced2** são implementados:

-   [**IWMReaderAdvanced:: getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2:: getplaymode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2:: getprotocolname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2:: SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**DirectShow Referência de QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Lendo arquivos ASF no DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




