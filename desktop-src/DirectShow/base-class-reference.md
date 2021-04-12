---
description: Referência de classe base do DirectShow
ms.assetid: 56f3685f-3df8-4358-b04e-3efc04b58008
title: Referência de classe base do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8816656f0ae87224cc95886ad32aaa1a098f177
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456763"
---
# <a name="directshow-base-class-reference"></a>Referência de classe base do DirectShow

Esta seção contém entradas de referência para todas as [classes base](directshow-base-classes.md)do Microsoft DirectShow, seus membros de dados e suas funções.



| Classe                                                                  | Descrição                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**CAggDirectDraw**](caggdirectdraw.md)                               | Preterido.                                                                                                                       |
| [**CAggDrawSurface**](caggdrawsurface.md)                             | Preterido.                                                                                                                       |
| [**CAMEvent**](camevent.md)                                           | Classe wrapper para eventos de redefinição manual e automática.                                                                                  |
| [**CAMMsgEvent**](cammsgevent.md)                                     | Classe de wrapper para objetos de evento que executam o processamento de mensagens.                                                                  |
| [**CAMSchedule**](camschedule.md)                                     | Agendador para relógios de referência.                                                                                                   |
| [**CAMThread**](camthread.md)                                         | Classe Bass para gerenciar threads de trabalho.                                                                                           |
| [**CAutoLock**](cautolock.md)                                         | Mantém uma seção crítica para o escopo de um bloco.                                                                                |
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md) | Obtém e libera o acesso a um objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .                                           |
| [**CBaseAllocator**](cbaseallocator.md)                               | Classe Bass para alocadores.                                                                                                        |
| [**CBaseBasicVideo**](cbasebasicvideo.md)                             | Manipula o componente IDispatch da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .                                              |
| [**CBaseControlVideo**](cbasecontrolvideo.md)                         | Implementa a interface IBasicVideo para uma janela de vídeo genérica.                                                                  |
| [**CBaseControlWindow**](cbasecontrolwindow.md)                       | Implementa a interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .                                                                    |
| [**CBaseDispatch**](cbasedispatch.md)                                 | Classe base para implementar a interface IDispatch.                                                                              |
| [**CBaseFilter**](cbasefilter.md)                                     | Classe base para filtros.                                                                                                           |
| [**CBaseInputPin**](cbaseinputpin.md)                                 | Classe base para Pins de entrada.                                                                                                        |
| [**CBaseList**](cbaselist.md)                                         | Classe base para listas genéricas.                                                                                                     |
| [**CBaseMediaFilter**](cbasemediafilter.md)                           | Implementa a interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) .                                                                    |
| [**CBaseObject**](cbaseobject.md)                                     | Classe base para implementar objetos do DirectShow.                                                                                   |
| [**CBaseOutputPin**](cbaseoutputpin.md)                               | Classe base para Pins de saída.                                                                                                       |
| [**CBasePin**](cbasepin.md)                                           | Classe base para Pins.                                                                                                              |
| [**CBasePropertyPage**](cbasepropertypage.md)                         | Classe base para implementar páginas de propriedades.                                                                                       |
| [**CBaseReferenceClock**](cbasereferenceclock.md)                     | Implementa um relógio de referência.                                                                                                     |
| [**CBaseRenderer**](cbaserenderer.md)                                 | Classe base para implementar filtros de renderizador.                                                                                     |
| [**CBaseStreamControl**](cbasestreamcontrol.md)                       | Implementa a interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) .                                                            |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)                       | Classe base para renderizadores de vídeo.                                                                                                   |
| [**CBaseVideoWindow**](cbasevideowindow.md)                           | Manipula o componente IDispatch da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .                                            |
| [**CBaseWindow**](cbasewindow.md)                                     | Classe base para gerenciar o Windows.                                                                                                  |
| [**CBasicAudio**](cbasicaudio.md)                                     | Manipula o componente de interface IDispatch da interface [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) .                                    |
| [**CCmdQueue**](ccmdqueue.md)                                         | Classe auxiliar para implementar a interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .                                               |
| [**CCritSec**](ccritsec.md)                                           | Fornece um bloqueio de thread.                                                                                                           |
| [**CDeferredCommand**](cdeferredcommand.md)                           | Implementa a interface [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) .                                                            |
| [**CDispParams**](cdispparams.md)                                     | Classe de wrapper para a estrutura DISPPARAMS.                                                                                       |
| [**CDrawImage**](cdrawimage.md)                                       | Classe auxiliar para desenhar em uma janela.                                                                                             |
| [**CDynamicOutputPin**](cdynamicoutputpin.md)                         | Pino de saída que dá suporte a reconexões de dyanamic e alterações de formato.                                                               |
| [**CEnumMediaTypes**](cenummediatypes.md)                             | Enumerador para tipos de mídia preferenciais.                                                                                             |
| [**CEnumPins**](cenumpins.md)                                         | Enumerador para Pins.                                                                                                              |
| [**CFactoryTemplate**](cfactorytemplate.md)                           | Classe que fornece informações para uma fábrica de classes.                                                                              |
| [**CGenericList**](cgenericlist.md)                                   | Modelo de classe que implementa uma lista específica de tipo.                                                                              |
| [**CImageAllocator**](cimageallocator.md)                             | Alocador para seções DIB.                                                                                                       |
| [**CImageDisplay**](cimagedisplay.md)                                 | Classe auxiliar para gerenciar formatos de exibição de imagem.                                                                                  |
| [**CImagePalette**](cimagepalette.md)                                 | Classe auxiliar para gerenciamento de paletas.                                                                                               |
| [**CImageSample**](cimagesample.md)                                   | Exemplo de mídia que usa seções DIB.                                                                                              |
| [**CLoadDirectDraw**](cloaddirectdraw.md)                             | Preterido.                                                                                                                       |
| [**CMediaControl**](cmediacontrol.md)                                 | Manipula os métodos IDispatch da interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .                                            |
| [**CMediaEvent**](cmediaevent.md)                                     | Manipula os métodos IDispatch da interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .                                                |
| [**CMediaPosition**](cmediaposition.md)                               | Manipula os métodos IDispatch da interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .                                          |
| [**CMediaSample**](cmediasample.md)                                   | Exemplo de mídia.                                                                                                                     |
| [**CMediaType**](cmediatype.md)                                       | Classe para gerenciar tipos de mídia.                                                                                                   |
| [**CMemAllocator**](cmemallocator.md)                                 | Alocador de memória.                                                                                                                 |
| [**CMsg**](cmsg.md)                                                   | Classe auxiliar para gerenciar solicitações feitas a um objeto [**CMsgThread**](cmsgthread.md) .                                             |
| [**CMsgThread**](cmsgthread.md)                                       | Thread de trabalho que enfileira solicitações para o thread de enfileiramento para conclusão assíncrona.                                             |
| [**COARefTime**](coareftime.md)                                       | Converte os tempos de referência entre as unidades de segundos e 100-nanossegundos.                                                                |
| [**COutputQueue**](coutputqueue.md)                                   | Objeto que enfileira amostras de mídia para entrega.                                                                                    |
| [**CPersistStream**](cpersiststream.md)                               | Classe base para implementar a interface IPersistStream.                                                                         |
| [**CPosPassThru**](cpospassthru.md)                                   | Manipula comandos de busca para filtros com um PIN de entrada.                                                                             |
| [**CPullPin**](cpullpin.md)                                           | Classe auxiliar que extrai dados de um pino de saída que dá suporte à interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .                 |
| [**CQueue**](cqueue.md)                                               | Modelo de classe que implementa uma fila simples e de tamanho estático.                                                                  |
| [**CReftime**](creftime.md)                                           | Classe auxiliar para gerenciar tempos de referência.                                                                                           |
| [**CRenderedInputPin**](crenderedinputpin.md)                         | Pino de entrada para filtros de processador que dão suporte a várias entradas.                                                                      |
| [**CRendererInputPin**](crendererinputpin.md)                         | Pino de entrada para a classe [**CBaseRenderer**](cbaserenderer.md) .                                                                   |
| [**CRendererPosPassThru**](crendererpospassthru.md)                   | Manipula comandos de busca para filtros de renderizador.                                                                                       |
| [**CSeekingPassThru**](cseekingpassthru.md)                           | Objeto auxiliar que cria objetos [**CPosPassThru**](cpospassthru.md) e [**CRendererPosPassThru**](crendererpospassthru.md) . |
| [**CSource**](csource.md)                                             | Classe base para implementar filtros de origem.                                                                                       |
| [**CSourcePosition**](csourceposition.md)                             | Classe abstrata para implementar a interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) . Obsoleto.                                 |
| [**CSourceSeeking**](csourceseeking.md)                               | Classe abstrata para implementar a busca em filtros de origem com um PIN de saída.                                                    |
| [**CSourceStream**](csourcestream.md)                                 | Pino de saída para a classe [**CSource**](csource.md) .                                                                              |
| [**CSystemClock**](csystemclock.md)                                   | Relógio do sistema.                                                                                                                     |
| [**CTransformFilter**](ctransformfilter.md)                           | Classe base para implementar filtros de transformação.                                                                                    |
| [**CTransformInputPin**](ctransforminputpin.md)                       | PIN de entrada usado pela classe CTransformFilter.                                                                                     |
| [**CTransformOutputPin**](ctransformoutputpin.md)                     | Pino de saída usado pela classe CTransformFilter.                                                                                    |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)                     | Classe para implementar filtros de transformação que não copiam dados.                                                                   |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin.md)                 | Pino de entrada para a classe CTransInPlaceFilter.                                                                                      |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)               | Pino de saída para a classe CTransInPlaceFilter.                                                                                     |
| [**CUnknown**](cunknown.md)                                           | Implementa a interface IUnknown.                                                                                                |
| [**CVideoTransformFilter**](cvideotransformfilter.md)                 | Classe base para filtros de transformação de vídeo.                                                                                           |
| [**FOURCCMap**](fourccmap.md)                                         | Classe auxiliar para converter entre GUIDs e FOURCC.                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes base do DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



