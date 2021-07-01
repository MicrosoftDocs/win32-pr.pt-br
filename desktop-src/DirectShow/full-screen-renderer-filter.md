---
description: Filtro de renderização de tela inteira
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: Filtro de renderização de tela inteira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d331ff6f31d1c985c7e255b23381a289931da60
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120471"
---
# <a name="full-screen-renderer-filter"></a>Filtro de renderização de tela inteira

O filtro Renderização de Tela Inteira fornece renderização de vídeo de tela inteira em hardware mais antigo. As placas de vídeo mais novas podem ampliar o vídeo com eficiência suficiente para que o Renderização de Tela Inteira não seja necessário. Portanto, o uso desse filtro agora foi preterido.

Não adicione manualmente esse filtro ao grafo de filtro. Se um aplicativo chamar [**IVideoWindow::p ut \_ FullScreenMode,**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode)o Gerenciador do Graph de Filtro selecionará automaticamente o renderador de vídeo apropriado para o modo de tela inteira. A seleção é transparente para o aplicativo. Com as placas de vídeo atuais, é improvável que o Gerenciador de Grafo de Filtros selecione o Renderdor de Tela Inteira.



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFullScreenVideoEx,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| Tipos de mídia de pino de entrada                    | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ Null                                                                                                                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de mídia de pino de saída                   | Não se aplica                                                                                                                                                                                                                                     |
| Interfaces de pino de saída                    | Não se aplica                                                                                                                                                                                                                                     |
| Filtrar CLSID                             | CLSID \_ ModexRenderer                                                                                                                                                                                                                               |
| CLSID da página de propriedades                      | CLSID \_ ModexProperties                                                                                                                                                                                                                             |
| Executável                               | quartz.dll                                                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | IMPROVÁVEL DE \_ VERÃO                                                                                                                                                                                                                                    |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

O Renderdor de Tela Inteira dá suporte a um conjunto estático de modos de exibição. No entanto, a placa de vídeo no sistema do usuário pode não dar suporte a todos os modos. Para determinar se o cartão dá suporte a um modo específico, chame o [**método IFullScreenVideoEx::IsModeAvailable.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) Você também pode desabilitar um modo de exibição específico programaticamente chamando [**IFullScreenVideoEx::SetEnabled.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled) Atualmente, o Renderador de Tela Inteira dá suporte aos modos de exibição mostrados na tabela a seguir:



| Mode | Largura | Altura | Profundidade de bits |
|------|-------|--------|-----------|
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



 

(Todos os modos são RGB.) No entanto, essa lista está sujeita a alterações. Use o [**método IFullScreenVideoEx::GetModeInfo**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) para obter informações sobre os modos. O Renderador de Tela Inteira sempre escolhe o modo de resolução mais baixa disponível, limitado por uma propriedade chamada fator de clipe *,* que determina quanto do vídeo o Renderador de Tela Inteira tem permissão para reclipe. Para obter mais informações, [**consulte IFullScreenVideoEx::GetClipFactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor).

Quando o aplicativo executa ou pausa o grafo de filtro, o Renderdor de Tela Inteira alterna para o modo de exibição escolhido. Quando o grafo é interrompido, o Renderização de Tela Inteira restaura o modo de exibição original.

O Renderdor de Tela Inteira só pode funcionar como a janela ativa de primeiro plano. Se o usuário alterna para outro aplicativo, o Renderdor de Tela Inteira oculta o vídeo minimizando ou ocultando a janela de vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



