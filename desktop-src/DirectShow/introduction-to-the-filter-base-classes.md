---
description: Introdução às classes base de filtro
ms.assetid: db6324d7-1914-44a8-a202-dff752b61c1a
title: Introdução às classes base de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c0682a5ba9f6a051506911cf143474d9958f1caa926464d9a4c236366e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952555"
---
# <a name="introduction-to-the-filter-base-classes"></a>Introdução às classes base de filtro

Este artigo descreve a biblioteca de classes DirectShow base da Microsoft. Essa biblioteca destina-se a desenvolvedores de filtros, mas os criadores de aplicativos podem achar úteis algumas das classes auxiliares e utilitários de depuração. No entanto, a biblioteca de classes base não é necessária DirectShow programação.

As seções a seguir resumem as classes base mais importantes na biblioteca.

**Classes de objeto COM**

As classes a seguir suportam a criação de objetos COM:



| Classe                              | Descrição                            |
|------------------------------------|----------------------------------------|
| [**Cbaseobject**](cbaseobject.md) | Classe de objeto base.                     |
| [**Cunknown**](cunknown.md)       | Implementa a interface **IUnknown.** |



 

A maioria das classes DirectShow são derivadas **de CBaseObject.** Essa classe fornece assistência de depuração mantendo uma contagem de todos os objetos ativos na DLL em tempo de executar. Em builds de depuração, a DLL declara se ela é descarregada enquanto a contagem de objetos é maior que zero. Isso facilita o controle de vazamentos causados por problemas de contagem de referências.

Todas as classes base que suportam interfaces COM derivam **de CUnknown**, que herda **CBaseObject**. A **classe CUnknown** dá suporte à contagem de referências, **a QueryInterface** e à agregação. Para obter mais informações, [consulte How to Implement IUnknown](how-to-implement-iunknown.md).

**Filtrar e fixar classes**

As classes a seguir suportam a criação de objetos DirectShow filtro e pino:



| Classe                                    | Descrição                                                                                                                                                     |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cbasefilter**](cbasefilter.md)       | Classe base para filtros. Implementa a interface [**IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                            |
| [**Cbasepin**](cbasepin.md)             | Classe base para pinos. Implementa as interfaces [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**e IQualityControl.**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| [**Cbaseinputpin**](cbaseinputpin.md)   | Classe base para pinos de entrada que usam o transporte de memória local. Implementa a interface [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Essa classe deriva de **CBasePin.** |
| [**Cbaseoutputpin**](cbaseoutputpin.md) | Classe base para pinos de saída que usam **conexões IMemInputPin.** Essa classe deriva de **CBasePin.**                                                         |



 

As classes a seguir são úteis para criar tipos mais especializados de filtros:



| Classe                                                  | Descrição                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Csource**](csource.md)                             | Classe base para filtros de origem. Essa classe foi projetada para criar fontes push. Ele não é adequado para fontes de pull, como leitores de arquivo. Para criar pinos de saída para essa classe, use a [**classe CSourceStream.**](csourcestream.md)                                                                   |
| [**Ctransformfilter**](ctransformfilter.md)           | Classe base para filtros de transformação. Essa classe executa uma cópia nos dados. Os pinos dessa classe são [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin.**](ctransformoutputpin.md)                                                                                            |
| [**Ctransinplacefilter**](ctransinplacefilter.md)     | Classe base para filtros de transformação que não copiam dados. Essa classe executa o processamento de dados diretamente nos dados de entrada antes de passá-los downstream. Os pinos dessa classe são [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin.**](ctransinplaceoutputpin.md) |
| [**Cvideotransformfilter**](cvideotransformfilter.md) | Classe base para filtros de transformação de vídeo. Essa classe deriva de **CTransformFilter** e adiciona suporte para controle de qualidade.                                                                                                                                                                                |
| [**Cbaserenderer**](cbaserenderer.md)                 | Classe base para filtros de renderização. O pino de entrada para essa classe [**é CRendererInputPin.**](crendererinputpin.md)                                                                                                                                                                                          |
| [**Cbasevideorenderer**](cbasevideorenderer.md)       | Classe base para renderadores de vídeo. Essa classe deriva de **CBaseRenderer.**                                                                                                                                                                                                                                |



 

Para usar essas classes, você deve derivar sua própria classe e escrever código para dar suporte à funcionalidade específica ao filtro. Quanto mais especializada a classe base, menos código você precisará escrever em sua classe derivada.

**Objetos auxiliares**

As classes a seguir implementam objetos auxiliares usados por filtros e pinos. A maioria dessas classes pode ser usada sem derivar novas classes delas:



| Classe                                              | Descrição                                                                                                                                                        |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cpullpin**](cpullpin.md)                       | Objeto auxiliar para pinos de entrada em filtros do analisador. Dá [**suporte a conexões IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) com fontes de pull.                                       |
| [**Coutputqueue**](coutputqueue.md)               | Objeto auxiliar para pinos de saída que enfileram amostras para entrega em um thread de trabalho.                                                                                  |
| [**Csourceseeking**](csourceseeking.md)           | Objeto de ajuda para implementar a busca em um filtro de origem com exatamente um pino de saída. (Essa classe não foi projetada para filtros com vários pinos, como analisadores.) |
| [**Cenumpins**](cenumpins.md)                     | Objeto enumerador para enumerar pinos em um filtro. Implementa a interface [**IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)                                                       |
| [**CEnumMediaTypes**](cenummediatypes.md)         | Objeto enumerador para enumerar tipos de mídia preferenciais em um pin. Implementa a interface [**IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)                             |
| [**Cmemallocator**](cmemallocator.md)             | Objeto alocador de memória. Implementa a interface [**IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)                                                                          |
| [**Cmediasample**](cmediasample.md)               | Objeto de exemplo de mídia. Implementa a interface [**IMediaSample2.**](/windows/desktop/api/Strmif/nn-strmif-imediasample2)                                                                              |
| [**Cbasereferenceclock**](cbasereferenceclock.md) | Classe base para relógios de referência. Implementa a interface [**IReferenceClock.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)                                                              |
| [**Cmediatype**](cmediatype.md)                   | Objeto auxiliar para manipular estruturas [**AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                |



 

 

 



