---
description: Filtro de renderização de vídeo
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Filtro de renderização de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96df49305b357cf4a889d283c64839c13c38e2b8f89b8d4eda35d06260f18c58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083496"
---
# <a name="video-renderer-filter"></a>Filtro de renderização de vídeo

O filtro de renderização de vídeo é um renderizador de vídeo robusto e com todos os propósitos.

> [!Note]  
> no Windows XP e versões posteriores, o processador de vídeo padrão é o [filtro de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7). O VMR-7 e o processador de vídeo têm o nome amigável "processador de vídeo". Em plataformas anteriores, o renderizador de vídeo é o renderizador padrão. Consulte [escolhendo o processador correto](choosing-the-right-renderer.md).

 

O processador de vídeo usa superfícies do DirectDraw e de sobreposição, se a placa de vídeo der suporte a eles. o filtro Graph Manager expõe a interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , que permite que os aplicativos definam e recuperem propriedades no processador de vídeo. Com placas de vídeo mais recentes, o renderizador de vídeo dá suporte à renderização de tela inteira. caso contrário, o filtro Graph Manager alternará automaticamente para o filtro de [processador de tela inteira](full-screen-renderer-filter.md) para o modo de tela inteira. Consulte [**IVideoWindow::p UT \_ fullscreenmode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode) para obter mais informações.

-   \[! Fundamental\]  
    > normalmente, a janela de vídeo desse filtro processa mensagens em um thread de trabalho criado pelo filtro Graph Manager. Entretanto, se um aplicativo criar diretamente o filtro usando **CoCreateInstance**, a janela de vídeo processará mensagens no thread do aplicativo. Nesse caso, o thread do aplicativo deve ter um loop de mensagem para enviar mensagens para a janela de vídeo. além disso, o thread não deve sair até a chamada de **versão** final para o processador de vídeo, que ocorre quando o filtro Graph Manager é desligado. Caso contrário, o aplicativo poderá ser bloqueado.

     



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2), [**IDirectDrawVideo**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo), [**IKsPropertySet**](ikspropertyset.md), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| Tipos de mídia de pino de entrada                    | Formatos de vídeo descompactados.                                                                                                                                                                                                                                                                                                                                                                              |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| Tipos de mídia do pino de saída                   | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                          |
| Interfaces de pino de saída                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID do filtro                             | \_VIDEORENDERER CLSID                                                                                                                                                                                                                                                                                                                                                                                     |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                                                                                                                                                                                                                                                                        |
| Executável                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [Núcleo](merit.md)                       | Windows XP e posterior: **mérito \_ improvável**                                                                                                                                                                                                                                                                                                                                                                |
| [Categoria do filtro](filter-categories.md) | **\_LEGACYAMFILTERCATEGORY CLSID**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentários

Na versão de depuração do Quartz.dll, se o nível de depuração do rastreamento de LOG \_ estiver definido como 5 ou superior, o renderizador de vídeo exibirá os carimbos de data/hora de cada quadro na janela de vídeo. Esses números não aparecem na versão de varejo da DLL. Para obter mais informações, consulte [depurar funções de saída](debug-output-functions.md).

Os comentários a seguir destinam-se a desenvolvedores de filtro:

O processador de vídeo aceita formatos YUV se a placa gráfica de vídeo der suporte a superfícies de sobreposição YUV. No entanto, quando ele se conecta pela primeira vez ao filtro upstream, o processador de vídeo requer um formato RGB que corresponda à intensidade de cor das configurações atuais do monitor. Por exemplo, se a configuração de exibição atual for de 24 bits, o filtro upstream deverá ser capaz de fornecer vídeo RGB de 24 bits. Quando o gráfico de filtro muda para um estado executando, o renderizador de vídeo negocia uma alteração de formato dinâmico para o espaço de cores YUV apropriado.

Conectando-se a um tipo RGB, o renderizador de vídeo garante que ele possa usar GDI caso o DirectDraw não esteja disponível. Ele mudará para GDI se outro aplicativo estiver usando a memória de vídeo, se o retângulo de vídeo abranger dois monitores em um sistema de vários monitores ou se o retângulo de vídeo estiver completamente obscurecido por outra janela.

> [!Note]  
> O processador de mixagem de vídeo não executa esse tipo de alteração de formato dinâmico e não requer um tipo de mídia RGB, porque ele nunca usa GDI para renderização.

 

Para negociar uma alteração de formato, o processador de vídeo chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) com o novo tipo de mídia. Se o filtro upstream retornar S \_ OK, o renderizador de vídeo anexará a nova mídia à próxima amostra. O filtro upstream deve chamar [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) em cada exemplo. Se **GetMediaType** retornar um valor não **nulo** , ele indicará uma alteração de formato e o filtro upstream deverá responder alternando os tipos de saída. (Não alterne os tipos no método **QueryAccept** .) O filtro upstream deve aceitar pelo menos os principais tipos RGB e, idealmente, deve dar suporte aos tipos YUV comuns. Durante o streaming, o processador de vídeo pode alternar entre os tipos YUV e RGB várias vezes. O processador de vídeo não aceita alterações de formato dinâmico iniciadas pelo filtro upstream.

Quando o processador de vídeo se desenha em uma superfície de sobreposição do DirectDraw, ele aloca um único buffer para seu PIN de entrada. Se o filtro upstream tentar forçar uma conexão usando vários buffers, o processador de vídeo não poderá usar a superfície de sobreposição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 



