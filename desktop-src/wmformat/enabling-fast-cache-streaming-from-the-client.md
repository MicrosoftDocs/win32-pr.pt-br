---
title: Habilitando o streaming de cache rápido do cliente
description: Habilitando o streaming de cache rápido do cliente
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows SDK do formato de mídia, habilitando o streaming de cache rápido
- Windows SDK do formato de mídia, streaming de cache rápido
- ASF (Advanced Systems Format), habilitando o streaming de cache rápido
- ASF (formato de sistemas avançados), habilitando o streaming de cache rápido
- ASF (Advanced Systems Format), streaming de cache rápido
- ASF (formato de sistemas avançados), streaming de cache rápido
- fluxos, habilitando o streaming de cache rápido
- Streaming de cache rápido, habilitando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0f02a571d5fac456d4dbc743e5fb936f98342a0ed8e8739d653b659ab7c6f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447616"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a>Habilitando o streaming de cache rápido do cliente

O cache rápido é uma tecnologia de streaming na qual o servidor transmite de forma oportuna o conteúdo a uma taxa de bits maior do que o necessário para a reprodução.

Se a largura de banda disponível for maior do que a taxa de bits do conteúdo, os fluxos de cache rápidos na taxa mais alta e armazenarão o conteúdo em buffer. Isso ajuda a reduzir as interrupções mais tarde se a rede ficar congestionada. Se a largura de banda da rede for menor do que a taxa de bits do conteúdo, o cache rápido armazenará em uma parte dos dados antes do início da reprodução. O cache rápido é recomendado para redes não confiáveis, como redes sem fio ou redes que experimentam grandes flutuações no tráfego de rede, como modems a cabo. Ele também é recomendado para conteúdo de taxa de bits variável (VBR). Os requisitos de largura de banda para o conteúdo da VBR não são constantes, e o cache rápido permite que o leitor armazene em buffer o fluxo durante as partes de taxa de bits inferiores.

O streaming de cache rápido tem suporte apenas para conteúdo sob demanda. Além disso, o servidor deve ser configurado para usar o streaming de cache rápido.

Para habilitar o cache rápido no objeto leitor, chame os métodos [**IWMReaderNetworkConfig2:: SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) e [**IWMReaderNetworkConfig2:: SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) com o valor **true**. O primeiro método permite que o leitor armazene em cache o conteúdo transmitido. A segunda habilita o uso de cache rápido em particular.

Com essas configurações, o leitor ativará o cache rápido por padrão se a largura de banda da rede for significativamente maior ou menor do que a taxa de bits do conteúdo e se o servidor oferecer suporte a ele. O usuário também pode controlar se o objeto leitor usa o cache rápido adicionando um ou mais dos seguintes modificadores à URL.



| Modificador         | Descrição                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMCache          | Se esse modificador estiver presente, o valor ' 0 ' desabilitará explicitamente o cache rápido, enquanto o valor ' 1 ' o habilita explicitamente.                                                                                                                                                                                                                            |
| WMBitrate        | Esse modificador especifica a taxa máxima de bits do servidor. Esse modificador pode ser usado para restringir o cache rápido a um determinado limite de largura de banda. Esse modificador será ignorado se uma largura de banda de conexão explícita já estiver definida com uma chamada para [**IWMReaderNetworkConfig:: SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth). |
| WMContentBitrate | Esse modificador especifica a taxa de bits para o conteúdo. O leitor usa esse modificador, se presente, quando seleciona fluxos de um arquivo de taxa de bits múltipla (MBR). Isso pode fazer com que o leitor receba conteúdo de alta taxa de bits em uma conexão lenta, o que resulta em tempos de buffer e atrasos muito longos.                                          |



 

O modificador WMCache = 1 força o leitor a usar o streaming de cache rápido, independentemente da banda de rede ou da taxa de bits do conteúdo, independentemente de quaisquer chamadas anteriores para **SetEnableFastCache**. No entanto, ele não substitui a configuração **SetEnableContentCaching** no leitor; nem substitui a configuração do servidor.

Os modificadores de URL têm o seguinte formato:

*URL*? *modificador* = *valor* do

Por exemplo:

mms://MyServer/MyVideo.wmv? WMCache = 1

Mais de um modificador pode ser especificado; Use um e comercial (&) para separá-los:

mms://MyServer/MyVideo.wmv? WMCache = 1&WMContentBitrate = 56000

 

 




