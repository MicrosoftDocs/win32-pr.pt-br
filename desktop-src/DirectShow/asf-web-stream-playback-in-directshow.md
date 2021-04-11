---
description: Reprodução de fluxo da Web ASF no DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Reprodução de fluxo da Web ASF no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d14a83d2baf9c11aa824f5d6358f62790c16b30
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296036"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Reprodução de fluxo da Web ASF no DirectShow

O Microsoft DirectShow dá suporte a fluxos da Web em cenários de reprodução de arquivos por meio do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) , mas você deve escrever seu próprio filtro do DirectShow para capturar e manter o fluxo.

> [!Note]  
> Para reproduzir fluxos da Web no conteúdo que está sendo transmitido de um servidor que executa os serviços de mídia do Windows, use o controle de® do ActiveX do Windows Media Player 9 Series inserido em uma página da Web.

 

Ao receber um arquivo contendo fluxos do tipo WMMEDIATYPE \_ FileTransfer, o leitor ASF do WM criará um PIN de saída para ele. O bloco de formato será uma estrutura de [**\_ \_ formato webstream WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . (Essa estrutura está documentada na documentação do SDK do Windows Media Format.) Se não houver um filtro downstream disponível que possa lidar com esse tipo de mídia, o PIN permanecerá desconectado, mas o arquivo ainda reproduzirá os fluxos de áudio e/ou vídeo.

Cada amostra de mídia em um fluxo da Web contém uma estrutura de [**\_ cabeçalho de \_ exemplo \_ do webstream WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , documentada na documentação do Windows Media Format SDK. A estrutura tem um comprimento variável, dependendo do comprimento de seu membro **wszURL** . O ponteiro para os dados de exemplo aponta inicialmente para essa estrutura, e você deve avançar o ponteiro após a estrutura para acessar os dados reais no fluxo.

O filtro do manipulador de fluxo da Web deve ser baseado na classe [**CBaseRenderer**](cbaserenderer.md) . No método [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md) , o filtro precisará analisar a estrutura para obter informações sobre o fluxo da Web e, em seguida, executar a ação apropriada. Normalmente, isso envolverá salvar o arquivo em disco e, em seguida, chamar as funções [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) e [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) ou [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) para colocar os arquivos no cache do Internet Explorer. O filtro deve tratar arquivos com várias partes, ou seja, arquivos que são maiores que um exemplo, e também deve manipular comandos de renderização, que são especificados pelo membro **\_ \_ \_ header. WSAMPLETYPE de exemplo webstream WMT** . O filtro envia um evento de [**\_ \_ evento OLE do EC**](ec-ole-event.md) para o aplicativo, junto com o texto do **cabeçalho de \_ exemplo webstream do WMT \_ \_ .** cadeia de caracteres wszURL que contém o nome do arquivo a ser renderizado. O aplicativo faz com que o navegador exiba a página especificada. Se o fluxo da Web tiver sido criado corretamente, o arquivo já deverá estar no cache.

Para obter mais informações sobre \_ o formato WEBstream do WMT \_ e \_ \_ \_ o cabeçalho de exemplo webstream do WMT, consulte a documentação do SDK do Windows Media Format.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
