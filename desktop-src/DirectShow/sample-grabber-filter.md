---
description: O filtro Grabber de Exemplo fornece uma maneira de recuperar exemplos conforme eles passam pelo grafo de filtro.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro grabber de exemplo (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 286348ec102a93697aa413ecfd1886879e7361b54eca48276b5e868be78eee03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633506"
---
# <a name="sample-grabber-filter"></a>Exemplo de filtro de grabber

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O filtro Grabber de Exemplo fornece uma maneira de recuperar exemplos conforme eles passam pelo grafo de filtro. É um filtro de transformação com um pino de entrada e um pino de saída. Ele passa todos os exemplos downstream inalterados, para que você possa inseri-lo em um grafo de filtro sem alterar o fluxo de dados. Seu aplicativo pode recuperar amostras individuais do filtro chamando métodos na interface [**ISampleGrabber.**](isamplegrabber.md)

Se você quiser recuperar exemplos sem renderizar os dados, conecte o filtro Grabber de Exemplo ao [**filtro Renderer**](null-renderer-filter.md) Nulo.



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| Tipos de mídia de pino de entrada                    | Qualquer tipo de mídia.                                                                                                                                    |
| Interfaces de pino de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia de pino de saída                   | Qualquer tipo de mídia. Corresponde ao tipo de mídia de entrada.                                                                                                          |
| Interfaces de pino de saída                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ SampleGrabber                                                                                                                               |
| CLSID da página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                  |
| Executável                               | Qedit.dll                                                                                                                                          |
| [Mérito](merit.md)                       | NÃO USE O NÃO \_ \_ USO \_ DE LIMITED                                                                                                                                |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Para usar esse filtro, adicione-o ao grafo de filtro e chame [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) com o tipo de mídia desejado. Esse método especifica o tipo de mídia para as conexões de pino de entrada e saída do filtro. Em seguida, conecte o filtro a outros filtros no grafo.

Se você chamar [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) com o valor **TRUE**, o filtro colocará em buffer cada amostra que receber antes de passá-la downstream. Chame o [**método ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) para recuperar o conteúdo atual do buffer. Como alternativa, você pode chamar [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) para que o filtro invoque uma função de retorno de chamada sempre que receber um exemplo.

O filtro tem as seguintes limitações para formatos de vídeo:

-   Ele não dá suporte a tipos de vídeo com orientação de cima para **baixo (biHeight negativo).**
-   Ele não dá suporte à estrutura de [**formato VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo de formato igual a **FORMAT \_ VideoInfo2**).
-   Ele rejeita qualquer tipo de vídeo em que a distância da superfície não corresponder à largura do vídeo.

Como resultado, o Sample Grabber não se conectará ao VMR (Video Mixing Renderer) para alguns tipos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Editando objetos de serviços](directshow-editing-services-objects.md)
</dt> <dt>

[Usando o exemplo de grabber](using-the-sample-grabber.md)
</dt> </dl>

 

 




