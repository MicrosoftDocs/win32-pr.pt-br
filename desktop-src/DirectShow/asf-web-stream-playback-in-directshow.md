---
description: Reprodução de fluxo web do ASF DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Reprodução de fluxo web do ASF DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28d9d3b7ea4fba5537383a846e6eff64f3815eefa21613c6056a15a5e497f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824621"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Reprodução de fluxo web do ASF DirectShow

O Microsoft DirectShow dá suporte a fluxos da Web em cenários de reprodução de arquivo por meio do filtro [Leitor do WM ASF,](wm-asf-reader-filter.md) mas você deve escrever seu próprio filtro DirectShow para capturar e persistir o fluxo.

> [!Note]  
> Para reproduzir fluxos da Web no conteúdo que está sendo transmitido de um servidor que executa Windows Media Services, use o controle ActiveX® série Windows Media Player Série 9 inserido em uma página da Web.

 

Quando um arquivo que contém fluxos do tipo WMMEDIATYPE FileTransfer, o Leitor do WM ASF criará um \_ pino de saída para ele. O bloco de formato será uma estrutura [**WMT \_ WEBSTREAM \_ FORMAT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) (Essa estrutura está documentada na documentação Windows do SDK de Formato de Mídia.) Se nenhum filtro downstream estiver disponível que possa manipular esse tipo de mídia, o pino permanecerá desconectado, mas o arquivo ainda reproduzirá os fluxos de áudio e/ou vídeo.

Cada exemplo de mídia em um fluxo da Web contém uma estrutura [**DE \_ \_ \_ HEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) DE EXEMPLO DO WMT WEBSTREAM, que está documentada na documentação do SDK Windows Formato de Mídia. A estrutura tem um comprimento variável, dependendo do comprimento de seu **membro wszURL.** O ponteiro para os dados de exemplo inicialmente aponta para essa estrutura e você deve avançar o ponteiro para além da estrutura para acessar os dados reais no fluxo.

O filtro do manipulador de fluxo da Web deve ser baseado na [**classe CBaseRenderer.**](cbaserenderer.md) No [**método CBaseRenderer::D oRenderSample,**](cbaserenderer-dorendersample.md) o filtro precisará analisar a estrutura para obter informações sobre o fluxo da Web e executar a ação apropriada. Normalmente, isso envolverá salvar o arquivo no disco e, em seguida, chamar as funções [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) e [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) ou [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) para colocar os arquivos no cache Internet Explorer. O filtro deve manipular arquivos de várias partes, ou seja, arquivos maiores que um exemplo e também devem manipular comandos de renderização, que são especificados pelo membro **DO WMT \_ WEBSTREAM \_ SAMPLE \_ HEADER.wSampleType.** O filtro envia um evento [**\_ EC OLE \_ EVENT**](ec-ole-event.md) para o aplicativo, juntamente com o texto da cadeia de **\_ \_ \_ caracteres HEADER.wszURL do WMT WEBSTREAM** que contém o nome do arquivo a ser renderizado. Em seguida, o aplicativo faz com que o navegador exibe a página especificada. Se o fluxo da Web tiver sido autor correto, o arquivo já deverá estar no cache.

Para obter mais informações sobre o FORMATO DO WMT WEBSTREAM e o HEADER DE EXEMPLO \_ DO WMT WEBSTREAM, consulte a documentação \_ \_ do \_ \_ SDK Windows Formato de Mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
