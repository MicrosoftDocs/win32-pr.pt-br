---
description: Windows Filtro de origem de mídia
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Filtro de origem de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb1e617a51095aec7cb409e46ba8f19f14f76fcd6f8d8a9bffeaa13843b1728b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982197"
---
# <a name="windows-media-source-filter"></a>Windows Filtro de origem de mídia

Esse filtro é o filtro de origem herdado para Windows Mídia® conteúdo. Ele é usado pelo Windows Media Player 6.4. Em geral, a maneira mais simples e confiável de usar esse filtro é usar o Windows Media Player 6.4 ActiveX controle. Muitos dos métodos expostos por esse filtro também são expostos por meio do controle ActiveX dados. Consulte o Windows Media Player SDK para obter mais informações.

Quando esse filtro recebe o nome de um arquivo ASF local ou uma URL para um arquivo remoto, ele lê o arquivo, analisado os fluxos compactados e cria um pino de saída para cada um deles. Esse filtro não usa o SDK Windows Formato de Mídia. Ele usa as versões de codec instaláveis dos decodificadores Windows Media, não as versões DMO. O pino de saída de áudio sempre se conecta ao filtro manipulador ACM do ASF e o pino de vídeo sempre se conecta ao manipulador de ICM ASF. (ICM nesse caso refere-se ao nome original do Gerenciador de Compactação de Vídeo.) O filtro não dá suporte à busca.

O diagrama a seguir mostra um grafo de filtro com esse filtro.

![grafo de filtro da fonte de mídia do Windows](images/wms-wmv-graph.png)

Para manter a compatibilidade com compatibilidade com Windows Media Player 6.4, esse filtro é o filtro de origem padrão para arquivos com extensões de arquivo .wma, .wmv e .asf. Para reprodução de arquivo, os aplicativos mais novos devem usar o [filtro Leitor do WM ASF.](wm-asf-reader-filter.md) No entanto, o Leitor do WM ASF não dá suporte à reprodução de conteúdo transmitido.

A maneira mais simples para um aplicativo reproduzir conteúdo Windows baseado em mídia é usar o SDK do Windows Media Player. Outra opção é usar o SDK Windows Formato de Mídia. A tentativa de criar um player personalizado com base no filtro Windows fonte de mídia não é recomendada.



| Rótulo | Valor |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops) [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Tipos de mídia de pino de entrada                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfaces de pino de entrada                     | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipos de mídia de pino de saída                   | Varia dependendo dos fluxos dentro do arquivo ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfaces de pino de saída                    | [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Filtrar CLSID                             | Consulte Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Executável                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | NORMAL DE SEMPRE \_                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

O CLSID do filtro não está definido em qnetwork.h. Use essa macro em seu próprio arquivo de header:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtro de Leitor do WM ASF](wm-asf-reader-filter.md)
</dt> </dl>

 

 



