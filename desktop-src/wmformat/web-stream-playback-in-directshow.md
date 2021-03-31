---
title: Reprodução de fluxo da Web no DirectShow
description: Reprodução de fluxo da Web no DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- SDK do Windows Media Format, DirectShow
- Windows Media Format SDK, reprodução de fluxo da Web
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), reprodução de fluxo da Web
- ASF (formato de sistemas avançados), reprodução de fluxo da Web
- DirectShow, reprodução de fluxo da Web
- Fluxos da Web, DirectShow
- Fluxos da Web, reprodução no DirectShow
- fluxos, reprodução de fluxo da Web no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916093"
---
# <a name="web-stream-playback-in-directshow"></a>Reprodução de fluxo da Web no DirectShow

O Microsoft DirectShow dá suporte a fluxos da Web (consulte [Web streams](web-streams.md) para obter mais informações) em cenários de reprodução de arquivos por meio do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) , mas você deve escrever seu próprio filtro do DirectShow para capturar e manter o fluxo.

> [!Note]  
> Para reproduzir fluxos da Web no conteúdo que está sendo transmitido de um servidor que executa os serviços de mídia do Windows, use o controle de® do ActiveX do Windows Media Player 9 Series inserido em uma página da Web.

 

Ao receber um arquivo contendo fluxos do tipo WMMEDIATYPE \_ FileTransfer, o leitor ASF do WM criará um PIN de saída para ele. O bloco de formato será uma estrutura de [**\_ \_ formato webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . Se não houver um filtro downstream disponível que possa lidar com esse tipo de mídia, o PIN permanecerá desconectado, mas o arquivo ainda reproduzirá os fluxos de áudio e/ou vídeo.

É importante entender que cada exemplo de mídia em um fluxo da Web contém uma estrutura de [**cabeçalho de \_ \_ exemplo \_ do webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , que tem um comprimento variável, dependendo do comprimento de seu membro **wszURL** . O ponteiro para os dados de exemplo aponta inicialmente para essa estrutura, e você deve avançar o ponteiro após a estrutura para acessar os dados reais no fluxo. O filtro do manipulador de fluxo da Web deve ser baseado na classe **CBaseRenderer** . No método **DoRenderSample** , o filtro precisará analisar a estrutura para obter informações sobre o fluxo da Web e, em seguida, executar a ação apropriada. Normalmente, isso envolverá salvar o arquivo em disco e, em seguida, chamar **CommitUrlCacheEntry** e **CreateUrlCacheEntry** para colocar os arquivos no cache do Internet Explorer. O filtro deve tratar arquivos com várias partes, ou seja, arquivos que são maiores que um exemplo, e também deve manipular comandos de renderização, que são especificados pelo membro **\_ \_ \_ header. WSAMPLETYPE de exemplo webstream WMT** . O filtro envia um **\_ \_ evento OLE do EC** para o aplicativo, junto com o texto do **cabeçalho de \_ exemplo webstream do WMT \_ \_ .** cadeia de caracteres wszURL que contém o nome do arquivo a ser renderizado. O aplicativo faz com que o navegador exiba a página especificada. Se o fluxo da Web tiver sido criado corretamente, o arquivo já deverá estar no cache.

Para obter mais informações sobre o **\_ \_ evento OLE** **CBaseRenderer**, **DoRenderSample** e EC, consulte a documentação do SDK do DirectShow.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fluxos da Web**](web-streams.md)
</dt> </dl>

 

 




