---
description: Filtro de processador de tela inteira
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: Filtro de processador de tela inteira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c175907ef0f60c3b1fe183eb0941b5118d24c9f2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908604"
---
# <a name="full-screen-renderer-filter"></a>Filtro de processador de tela inteira

O filtro de processador de tela inteira fornece renderização de vídeo de tela inteira em hardware mais antigo. Placas de vídeo mais recentes podem ampliar o vídeo com eficiência suficiente para que o processador de tela inteira não seja necessário. Portanto, o uso desse filtro agora é preterido.

Não adicione esse filtro manualmente ao gráfico de filtro. Se um aplicativo chamar [**IVideoWindow::p UT \_ fullscreenmode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode), o Gerenciador de gráfico de filtro selecionará automaticamente o processador de vídeo apropriado para o modo de tela inteira. A seleção é transparente para o aplicativo. Com as placas de vídeo atuais, o Gerenciador de gráfico de filtro é improvável de selecionar o processador de tela inteira.



| Label | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFullScreenVideoEx**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| Tipos de mídia de pino de entrada                    | \_Vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                                                                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de mídia do pino de saída                   | Não aplicável                                                                                                                                                                                                                                     |
| Interfaces de pino de saída                    | Não aplicável                                                                                                                                                                                                                                     |
| CLSID do filtro                             | \_MODEXRENDERER CLSID                                                                                                                                                                                                                               |
| CLSID de página de propriedades                      | \_MODEXPROPERTIES CLSID                                                                                                                                                                                                                             |
| Executável                               | quartz.dll                                                                                                                                                                                                                                         |
| [Núcleo](merit.md)                       | MÉRITO \_ improvável                                                                                                                                                                                                                                    |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

O processador de tela inteira dá suporte a um conjunto estático de modos de exibição. No entanto, a placa de vídeo no sistema do usuário pode não dar suporte a todos os modos. Para determinar se o cartão dá suporte a um modo específico, chame o método [**IFullScreenVideoEx:: IsModeAvailable**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) . Você também pode desabilitar um modo de exibição específico programaticamente, chamando [**IFullScreenVideoEx:: sethabilitado**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled). O processador de tela inteira atualmente dá suporte aos modos de exibição mostrados na tabela a seguir:



| Label | Valor |
|------|-------|--------|-----------|
| Modo | Largura | Altura | Profundidade de bits |
| 0    | 320   | 200    | 16        |
| 1    | 320   | 200    | 8         |
| 2    | 320   | 240    | 16        |
| 3    | 320   | 240    | 8         |
| 4    | 640   | 400    | 16        |
| 5    | 640   | 400    | 8         |
| 6    | 640   | 480    | 16        |
| 7    | 640   | 480    | 8         |
| 8    | 800   | 600    | 16        |
| 9    | 800   | 600    | 8         |
| 10   | 1024  | 768    | 16        |
| 11   | 1024  | 768    | 8         |
| 12   | 1152  | 864    | 16        |
| 13   | 1152  | 864    | 8         |
| 14   | 1280  | 1024   | 16        |
| 15   | 1280  | 1024   | 8         |



 

(Todos os modos são RGB.) No entanto, essa lista está sujeita a alterações. Use o método [**IFullScreenVideoEx:: GetModeInfo**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) para obter informações sobre os modos. O processador de tela inteira sempre escolhe o modo de resolução mais baixa disponível, limitado por uma propriedade chamada *clip factor*, que determina a quantidade de vídeo que o processador de tela inteira pode recortar. Para obter mais informações, consulte [**IFullScreenVideoEx:: GetClipFactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor).

Quando o aplicativo executa ou pausa o gráfico de filtro, o renderizador de tela completo alterna para o modo de exibição que foi escolhido. Quando o grafo para, o processador de tela inteira restaura o modo de exibição original.

O processador de tela inteira só pode funcionar como a janela ativa em primeiro plano. Se o usuário alternar para outro aplicativo, o processador de tela inteira ocultará o vídeo, minimizando ou ocultando a janela de vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



