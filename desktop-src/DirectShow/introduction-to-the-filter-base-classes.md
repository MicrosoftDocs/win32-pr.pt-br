---
description: Introdução às classes base de filtro
ms.assetid: db6324d7-1914-44a8-a202-dff752b61c1a
title: Introdução às classes base de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44c104d8fe155a7c9f0edba72770a508c8ec43d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370041"
---
# <a name="introduction-to-the-filter-base-classes"></a>Introdução às classes base de filtro

Este artigo descreve a biblioteca de classes base do Microsoft DirectShow. Essa biblioteca destina-se a desenvolvedores de filtro, mas os gravadores de aplicativos podem encontrar algumas das classes auxiliares e utilitários de depuração úteis. No entanto, a biblioteca de classes base não é necessária para a programação do DirectShow.

As seções a seguir resumem as classes base mais importantes na biblioteca.

**Classes de objeto COM**

As classes a seguir dão suporte à criação de objetos COM:



| Classe                              | Descrição                            |
|------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject.md) | Classe de objeto base.                     |
| [**CUnknown**](cunknown.md)       | Implementa a interface **IUnknown** . |



 

A maioria das classes do DirectShow deriva de **CBaseObject**. Essa classe fornece assistência de depuração mantendo uma contagem de todos os objetos ativos na DLL em tempo de execução. Em compilações de depuração, a DLL é declarada se for descarregada enquanto a contagem de objetos for maior que zero. Isso torna mais fácil rastrear vazamentos causados por problemas de contagem de referência.

Todas as classes base que oferecem suporte a interfaces COM derivam de **CUnknown**, que herda **CBaseObject**. A classe **CUnknown** dá suporte à contagem de referência, **QueryInterface** e agregação. Para obter mais informações, consulte [como implementar IUnknown](how-to-implement-iunknown.md).

**Filtrar e fixar classes**

As classes a seguir dão suporte à criação de objetos de filtro e de PIN do DirectShow:



| Classe                                    | Descrição                                                                                                                                                     |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBaseFilter**](cbasefilter.md)       | Classe base para filtros. Implementa a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .                                                                            |
| [**CBasePin**](cbasepin.md)             | Classe base para Pins. Implementa as interfaces [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) e [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) .                                             |
| [**CBaseInputPin**](cbaseinputpin.md)   | Classe base para Pins de entrada que usam o transporte de memória local. Implementa a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Essa classe deriva de **CBasePin**. |
| [**CBaseOutputPin**](cbaseoutputpin.md) | Classe base para Pins de saída que usam conexões **IMemInputPin** . Essa classe deriva de **CBasePin**.                                                         |



 

As classes a seguir são úteis para a criação de tipos mais especializados de filtros:



| Classe                                                  | Descrição                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CSource**](csource.md)                             | Classe base para filtros de origem. Essa classe foi projetada para criar fontes de push. Ele não é adequado para fontes de pull, como leitores de arquivo. Para criar Pins de saída para essa classe, use a classe [**CSourceStream**](csourcestream.md) .                                                                   |
| [**CTransformFilter**](ctransformfilter.md)           | Classe base para filtros de transformação. Essa classe executa uma cópia nos dados. Os Pins para essa classe são [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md).                                                                                            |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)     | Classe base para filtros de transformação que não copiam dados. Essa classe executa o processamento de dados diretamente nos dados de entrada antes de passá-lo downstream. Os Pins para essa classe são [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md). |
| [**CVideoTransformFilter**](cvideotransformfilter.md) | Classe base para filtros de transformação de vídeo. Essa classe deriva de **CTransformFilter** e adiciona suporte para controle de qualidade.                                                                                                                                                                                |
| [**CBaseRenderer**](cbaserenderer.md)                 | Classe base para filtros de renderizador. O pino de entrada para essa classe é [**CRendererInputPin**](crendererinputpin.md).                                                                                                                                                                                          |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)       | Classe base para renderizadores de vídeo. Essa classe deriva de **CBaseRenderer**.                                                                                                                                                                                                                                |



 

Para usar essas classes, você deve derivar sua própria classe e escrever código para dar suporte à funcionalidade específica ao seu filtro. Quanto mais especializado for a classe base, menor será o código que você precisará escrever em sua classe derivada.

**Objetos auxiliares**

As classes a seguir implementam objetos auxiliares que são usados por filtros e Pins. A maioria dessas classes pode ser usada sem derivar novas classes a partir delas:



| Classe                                              | Descrição                                                                                                                                                        |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPullPin**](cpullpin.md)                       | Objeto auxiliar para Pins de entrada em filtros do analisador. Dá suporte a conexões [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) com fontes de pull.                                       |
| [**COutputQueue**](coutputqueue.md)               | Objeto auxiliar para Pins de saída que enfileiram amostras para entrega em um thread de trabalho.                                                                                  |
| [**CSourceSeeking**](csourceseeking.md)           | Objeto de ajuda para implementar a busca em um filtro de origem com exatamente um pino de saída. (Essa classe não é projetada para filtros com vários Pins, como analisadores.) |
| [**CEnumPins**](cenumpins.md)                     | Objeto enumerador para enumerar Pins em um filtro. Implementa a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .                                                       |
| [**CEnumMediaTypes**](cenummediatypes.md)         | Objeto enumerador para enumeração de tipos de mídia preferenciais em um PIN. Implementa a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .                             |
| [**CMemAllocator**](cmemallocator.md)             | Objeto de alocador de memória. Implementa a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .                                                                          |
| [**CMediaSample**](cmediasample.md)               | Objeto de exemplo de mídia. Implementa a interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) .                                                                              |
| [**CBaseReferenceClock**](cbasereferenceclock.md) | Classe base para relógios de referência. Implementa a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .                                                              |
| [**CMediaType**](cmediatype.md)                   | Objeto auxiliar para manipular estruturas [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .                                                                                |



 

 

 



