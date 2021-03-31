---
description: Filtro de origem de mídia do Windows
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Filtro de origem de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe60a038cfd5109a5c55ca6c40640d39b2426d3a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172463"
---
# <a name="windows-media-source-filter"></a>Filtro de origem de mídia do Windows

Esse é o filtro de origem herdado para conteúdo de® de mídia do Windows. Ele é usado pelo Windows Media Player 6,4. Em geral, a maneira mais simples e confiável de usar esse filtro é usar o controle ActiveX do Windows Media Player 6,4. Muitos dos métodos expostos por esse filtro também são expostos por meio do controle ActiveX. Consulte o SDK do Windows Media Player para obter mais informações.

Quando esse filtro recebe o nome de um arquivo ASF local ou uma URL para um arquivo remoto, ele lê o arquivo, analisa os fluxos compactados e cria um PIN de saída para cada um. Esse filtro não usa o Windows Media Format SDK. Ele usa as versões de codec instaláveis dos decodificadores de mídia do Windows, não as versões DMO. O PIN de saída de áudio sempre se conecta ao filtro do manipulador do ACM do ASF e o PIN do vídeo sempre se conecta ao manipulador do ASF ICM. (Nesse caso, o ICM se refere ao nome original do Gerenciador de compactação de vídeo.) O filtro não dá suporte à busca.

O diagrama a seguir mostra um gráfico de filtro com este filtro.

![Grafo de filtro de origem do Windows Media](images/wms-wmv-graph.png)

Para manter a compatibilidade com versões anteriores com o Windows Media Player 6,4, esse filtro é o filtro de origem padrão para arquivos com extensões de arquivo. WMA,. wmv e. ASF. Para a reprodução de arquivos, os aplicativos mais recentes devem usar o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) . No entanto, o leitor ASF do WM não oferece suporte à reprodução de conteúdo transmitido.

A maneira mais simples de um aplicativo reproduzir conteúdo baseado no Windows Media é usar o SDK do Windows Media Player. Outra opção é usar o Windows Media Format SDK. Não é recomendável tentar criar um player personalizado baseado no filtro de origem de mídia do Windows.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Tipos de mídia de pino de entrada                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfaces de pino de entrada                     | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipos de mídia do pino de saída                   | Varia dependendo dos fluxos dentro do arquivo ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfaces de pino de saída                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| CLSID do filtro                             | Ver comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Executável                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Núcleo](merit.md)                       | MÉRITO \_ normal                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

O CLSID do filtro não está definido em Qnetwork. h. Use esta macro em seu próprio arquivo de cabeçalho:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtro de leitor ASF do WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



