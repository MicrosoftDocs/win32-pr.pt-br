---
description: O filtro de apoio de exemplo fornece uma maneira de recuperar amostras à medida que elas passam pelo gráfico de filtro.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro de apoio de exemplo (QEdit. h)
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
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909664"
---
# <a name="sample-grabber-filter"></a>Filtro de apoio de exemplo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O filtro de apoio de exemplo fornece uma maneira de recuperar amostras à medida que elas passam pelo gráfico de filtro. É um filtro de transformação com um PIN de entrada e um PIN de saída. Ele passa todas as amostras downstream inalteradas, para que você possa inseri-la em um grafo de filtro sem alterar o fluxo de dados. Em seguida, seu aplicativo pode recuperar exemplos individuais do filtro chamando métodos na interface [**ISampleGrabber**](isamplegrabber.md) .

Se você quiser recuperar amostras sem renderizar os dados, conecte o filtro de apoio de exemplo ao filtro de [**renderizador nulo**](null-renderer-filter.md) .



| Label | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| Tipos de mídia de pino de entrada                    | Qualquer tipo de mídia.                                                                                                                                    |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia do pino de saída                   | Qualquer tipo de mídia. Corresponde ao tipo de mídia de entrada.                                                                                                          |
| Interfaces de pino de saída                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | \_SAMPLEGRABBER CLSID                                                                                                                               |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                  |
| Executável                               | Qedit.dll                                                                                                                                          |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Para usar esse filtro, adicione-o ao grafo de filtro e chame [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) com o tipo de mídia desejado. Esse método especifica o tipo de mídia para as conexões de entrada e de pino de saída do filtro. Em seguida, conecte o filtro a outros filtros no grafo.

Se você chamar [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) com o valor **true**, o filtro armazenará em buffer cada exemplo que ele receber antes de passá-lo downstream. Chame o método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) para recuperar o conteúdo atual do buffer. Como alternativa, você pode chamar [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md) para que o filtro invoque uma função de retorno de chamada sempre que receber um exemplo.

O filtro tem as seguintes limitações para formatos de vídeo:

-   Ele não dá suporte a tipos de vídeo com orientação de cima para baixo ( **semialtura** negativa).
-   Ele não dá suporte à estrutura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo de formato igual ao **formato \_ VideoInfo2**).
-   Ele rejeita qualquer tipo de vídeo em que o stride da superfície não corresponde à largura do vídeo.

Como resultado, o exemplo de apoio não se conectará ao VMR (Video mixagem Renderer) para alguns tipos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de serviços de edição do DirectShow](directshow-editing-services-objects.md)
</dt> <dt>

[Usando o exemplo de apoio](using-the-sample-grabber.md)
</dt> </dl>

 

 




