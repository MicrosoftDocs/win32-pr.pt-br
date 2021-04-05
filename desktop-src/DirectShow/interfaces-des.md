---
description: Interfaces para serviços de edição do DirectShow
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: Interfaces para serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba286a340693407287ed370ed401ac6b039593c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646052"
---
# <a name="interfaces-for-directshow-editing-services"></a>Interfaces para serviços de edição do DirectShow

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Esta seção contém tópicos de referência para as interfaces de [serviços de edição do DirectShow](directshow-editing-services.md) (des).



| Interface                                                  | Descrição                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAMErrorLog**](iamerrorlog.md)                         | Fornece um método de retorno de chamada para log de erros.                                                                                  |
| [**IAMSetErrorLog**](iamseterrorlog.md)                   | Define ou recupera um log de erros.                                                                                                |
| [**IAMTimeline**](iamtimeline.md)                         | Fornece métodos para manipular a linha do tempo.                                                                                |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Insere ou recupera faixas virtuais em uma composição.                                                                          |
| [**IAMTimelineEffect**](iamtimelineeffect.md)             | Fornece métodos para manipular efeitos de linha do tempo.                                                                            |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | Fornece métodos para adicionar efeitos a um objeto de linha do tempo.                                                                      |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Define e recupera propriedades em grupos.                                                                                       |
| [**IAMTimelineObj**](iamtimelineobj.md)                   | Fornece métodos para manipular objetos de linha do tempo.                                                                            |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | Divide um objeto de linha do tempo.                                                                                                      |
| [**IAMTimelineSrc**](iamtimelinesrc.md)                   | Fornece métodos para manipular e definir propriedades em objetos de origem.                                                    |
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Fornece métodos para manipular objetos Track.                                                                               |
| [**IAMTimelineTrans**](iamtimelinetrans.md)               | Fornece métodos para manipular objetos de transição.                                                                          |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | Adiciona transições a um objeto.                                                                                                 |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Fornece métodos para trabalhar com faixas virtuais.                                                                              |
| [**IDxtAlphaSetter**](idxtalphasetter.md)                 | Define propriedades no efeito de [setter alfa](alpha-setter-effect.md) .                                                         |
| [**IDxtCompositor**](idxtcompositor.md)                   | Define propriedades na transição do [compositor](compositor-transition.md) .                                                     |
| [**IDxtJpeg**](idxtjpeg.md)                               | Define propriedades na transição de [apagamento SMPTE](smpte-wipe-transition.md) .                                                     |
| [**IDxtKey**](idxtkey.md)                                 | Define propriedades na transição de [chave](key-transition.md) .                                                                   |
| [**IFindCompressorCB**](ifindcompressorcb.md)             | Não há suporte.                                                                                                                 |
| [**IGrfCache**](igrfcache.md)                             | Não há suporte.                                                                                                                 |
| [**IMediaDet**](imediadet.md)                             | Recupera informações sobre um arquivo de mídia, como o número de fluxos e o tipo, a duração e a taxa de quadros de cada fluxo. |
| [**IMediaLocator**](imedialocator.md)                     | Fornece métodos para validar nomes de arquivo.                                                                                    |
| [**IPropertySetter**](ipropertysetter.md)                 | Define propriedades em um efeito ou transição.                                                                                    |
| [**IRenderEngine**](irenderengine.md)                     | Renderiza um projeto DES construindo um grafo de filtro de uma linha do tempo.                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | Permite que o aplicativo substitua o filtro de redimensionamento de vídeo padrão usado pelo DES.                                              |
| [**IResize**](iresize.md)                                 | Deve ter suporte de qualquer filtro personalizado de redimensionador de vídeo.                                                                          |
| [**ISampleGrabber**](isamplegrabber.md)                   | Recupera exemplos de mídia individuais à medida que eles se movem pelo grafo de filtro.                                                      |
| [**ISampleGrabberCB**](isamplegrabbercb.md)               | Interface de retorno de chamada para a interface [**ISampleGrabber**](isamplegrabber.md) .                                                 |
| [**ISmartRenderEngine**](ismartrenderengine.md)           | Fornece métodos que dão suporte à recompactação inteligente.                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | Salva e carrega arquivos de projeto DES no linguagem XML (XML).                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de C++ dos serviços de edição do DirectShow](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



