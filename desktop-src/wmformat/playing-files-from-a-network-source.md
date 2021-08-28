---
title: Como tocar arquivos de uma fonte de rede
description: Como tocar arquivos de uma fonte de rede
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- Windows SDK de Formato de Mídia, lendo dados ASF
- Windows SDK de Formato de Mídia, reprodução de arquivos de fontes de rede
- ASF (Advanced Systems Format), lendo dados
- ASF (Formato de Sistemas Avançados), lendo dados
- ASF (Advanced Systems Format), reprodução de arquivos de fontes de rede
- ASF (Formato de Sistemas Avançados), reprodução de arquivos de fontes de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8473a2feb4edd567c15d640dfd20e65c2893fe12de6c25a957cc5f730fde0baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027374"
---
# <a name="playing-files-from-a-network-source"></a>Como tocar arquivos de uma fonte de rede

A leitura de uma rede não é fundamentalmente diferente da leitura de um arquivo local. O aplicativo passa a URL para o método [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) do objeto de leitor e o objeto leitor lida com os detalhes dos protocolos de rede. O objeto leitor usa o gerenciamento de buffer inteligente para fornecer a reprodução mais suave possível. Se o aplicativo precisar de mais controle sobre as configurações de rede do objeto de leitor, elas estarão disponíveis por meio das interfaces [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) e [**IWMReaderNetworkConfig2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)

O conteúdo de uma fonte de rede se enquadra em uma das duas categorias a seguir:

-   Streaming. Os dados são transmitidos just-in-time a serem tocadas no computador local. Servidores que executam Windows Media Services podem fornecer dados de streaming. Se o conteúdo da MBR (taxa de bits múltipla) for transmitido, o cliente poderá solicitar uma taxa de bits diferente do servidor à medida que o streaming progride.
-   Baixado. Todos os dados são transmitidos o mais rápido possível para que possam ser salvos como um arquivo no computador local. Os servidores Web fornecem dados baixados. Não há nenhuma comunicação do cliente com o servidor após o início do download.

Quando o objeto leitor baixa um arquivo de um servidor Web, ele usa uma técnica chamada streaming progressivo, que permite que um player comece a renderizar o conteúdo antes de o download ser concluído. Os dados são armazenados em buffer para fornecer um fluxo ininterrupto de dados para o player. Informações como a taxa de transferência e a duração do conteúdo são usadas para determinar por quanto tempo os dados serão armazenados em buffer antes de forra-los ao player.

Para abrir um arquivo ou fluxo em uma rede, chame o método **IWMReader::Open** do objeto de leitor com a URL apropriada. **Open** é uma chamada assíncrona, portanto, ela retorna imediatamente. Quando a origem estiver pronta para leitura, o objeto leitor enviará uma notificação WMT OPENED para o método de retorno de chamada \_ [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) do aplicativo. Neste ponto, o aplicativo pode consultar o leitor para o modo de entrega chamando [**IWMReaderAdvanced2::GetPlayMode.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode) Para conteúdo de rede, esse método retornará DOWNLOAD DO MODO WMT PLAY, indicando conteúdo baixado ou STREAMING DO MODO DE REPRODUÇÃO \_ DO WMT, indicando \_ \_ conteúdo \_ \_ \_ transmitido.

Para começar a ler o arquivo ou fluxo, chame o [**método IWMReader::Start.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) O leitor envia uma notificação START DE BUFFER DO WMT quando ele começa a buffer do conteúdo e uma notificação \_ \_ WMT BUFFERING STOP quando o buffer é \_ \_ concluído. Enquanto o leitor estiver em buffer de conteúdo (ou seja, entre essas duas notificações), talvez você queira exibir o progresso do buffer para o usuário. O [**método IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) retorna a porcentagem de dados armazenados em buffer e o tempo estimado que permanece. Para o conteúdo baixado, você também pode chamar [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) para obter o progresso do download. Chame esses métodos repetidamente para atualizar sua exibição, até que o buffer seja concluído. O buffer pode ocorrer novamente durante a reprodução, devido a fatores como congestionamento de rede. Se isso ocorrer, o aplicativo receberá outra notificação START \_ DE BUFFER DO WMT. \_

Quando o objeto leitor começa a reproduzir o conteúdo, ele envia uma notificação WMT \_ STARTED. Como cada exemplo é decodificado e fica disponível para renderização, o leitor o passa para o aplicativo por meio do método de retorno de chamada [**IWMReaderCallback::OnSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) Neste ponto, o processo é o mesmo que para reprodução de arquivo local. Quando a reprodução é interrompida, o leitor envia uma \_ notificação WMT END \_ OF \_ STREAMING.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




