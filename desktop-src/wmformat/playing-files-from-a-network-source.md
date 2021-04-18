---
title: Executando arquivos de uma fonte de rede
description: Executando arquivos de uma fonte de rede
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- SDK do Windows Media Format, lendo dados ASF
- SDK do Windows Media Format, reproduzindo arquivos de fontes de rede
- ASF (Advanced Systems Format), lendo dados
- ASF (formato de sistemas avançados), lendo dados
- ASF (Advanced Systems Format), reproduzindo arquivos de fontes de rede
- ASF (formato de sistemas avançados), reproduzindo arquivos de fontes de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1e4e41ddf94498ddeddf90e64439c1b11b7ba8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105763037"
---
# <a name="playing-files-from-a-network-source"></a>Executando arquivos de uma fonte de rede

A leitura de uma rede não é fundamentalmente diferente da leitura de um arquivo local. O aplicativo passa a URL para o método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) do objeto Reader e o objeto leitor manipula os detalhes dos protocolos de rede. O objeto leitor usa o gerenciamento de buffer inteligente para fornecer a reprodução mais suave possível. Se o aplicativo precisar de mais controle sobre as configurações de rede do objeto leitor, eles estarão disponíveis por meio das interfaces [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) e [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) .

O conteúdo de uma fonte de rede se encaixa em uma das duas categorias a seguir:

-   Transmiti. Os dados são transmitidos just in time para serem reproduzidos no computador local. Os servidores que executam os serviços de mídia do Windows podem fornecer dados de streaming. Se o conteúdo de taxa de bits múltipla (MBR) for transmitido, o cliente poderá solicitar uma taxa de bits diferente do servidor conforme o streaming progride.
-   Obteve. Todos os dados são transmitidos o mais rapidamente possível para que possam ser salvos como um arquivo no computador local. Os servidores Web fornecem dados baixados. Não há comunicação entre o cliente e o servidor após o início do download.

Quando o objeto de leitor baixa um arquivo de um servidor Web, ele usa uma técnica chamada streaming progressivo, que permite que um jogador comece a renderizar o conteúdo antes da conclusão do download. Os dados são armazenados em buffer para fornecer um fluxo de dados ininterrupto para o Player. Informações como a taxa de transferência e a duração do conteúdo são usadas para determinar por quanto tempo armazenar os dados em buffer antes de fornecê-los ao Player.

Para abrir um arquivo ou fluxo em uma rede, chame o método **IWMReader:: Open** do objeto Reader com a URL apropriada. **Open** é uma chamada assíncrona, portanto, retorna imediatamente. Quando a origem estiver pronta para leitura, o objeto leitor enviará uma \_ notificação WMT aberta para o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) do aplicativo. Neste ponto, o aplicativo pode consultar o leitor para o modo de entrega chamando [**IWMReaderAdvanced2:: Getplaymode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode). Para o conteúdo da rede, esse método retornará o \_ download do modo de reprodução WMT \_ \_ , indicando o conteúdo baixado ou o \_ streaming do \_ modo de reprodução WMT \_ , indicando o conteúdo transmitido.

Para começar a ler o arquivo ou fluxo, chame o método [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) . O leitor envia uma \_ notificação de início de buffer WMT \_ quando começa a armazenar em buffer o conteúdo e uma \_ notificação de parada de buffer WMT quando o \_ buffer é concluído. Embora o leitor esteja armazenando o conteúdo em buffer (ou seja, entre essas duas notificações), talvez você queira exibir o progresso do buffer para o usuário. O método [**IWMReaderAdvanced2:: GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) retorna a porcentagem de dados que foram armazenados em buffer e o tempo estimado restante. Para conteúdo baixado, você também pode chamar [**IWMReaderAdvanced2:: GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) para obter o progresso do download. Chame esses métodos repetidamente para atualizar sua exibição, até que o buffer seja concluído. O armazenamento em buffer pode ocorrer novamente durante a reprodução, devido a fatores como o congestionamento da rede. Se isso ocorrer, o aplicativo receberá outra \_ notificação de início do buffer WMT \_ .

Quando o objeto leitor começa a reproduzir o conteúdo, ele envia uma \_ notificação WMT iniciado. Como cada exemplo é decodificado e fica disponível para renderização, o leitor passa-o para o aplicativo por meio do método de retorno de chamada [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) . Neste ponto, o processo é o mesmo que para a reprodução de arquivo local. Quando a reprodução é interrompida, o leitor envia um WMT \_ fim \_ da \_ notificação de streaming.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




