---
description: Etapa 1.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Etapa 1. Escolher uma classe base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829068"
---
# <a name="step-1-choose-a-base-class"></a>Etapa 1. Escolher uma classe base

Esta é a etapa 1 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).

Supondo que você decida escrever um filtro e não um DMO, a primeira etapa é escolher qual classe base usar. As classes a seguir são apropriadas para filtros de transformação:

-   O [**CTransformFilter**](ctransformfilter.md) foi projetado para filtros de transformação que usam buffers de entrada e saída separados. Esse tipo de filtro, às vezes, é chamado de filtro de cópia/transformação. Quando um filtro de cópia/transformação recebe um exemplo de entrada, ele grava novos dados em um exemplo de saída e entrega o exemplo de saída para o próximo filtro.
-   O [**CTransInPlaceFilter**](ctransinplacefilter.md) é projetado para filtros que modificam dados no buffer original, também chamados de filtros de trans-in-Place. Quando um filtro de trans-in-Place recebe um exemplo, ele altera os dados dentro desse exemplo e entrega o mesmo exemplo downstream. O PIN de entrada do filtro e o PIN de saída sempre se conectam com os tipos de mídia correspondentes.
-   O [**CVideoTransformFilter**](cvideotransformfilter.md) é projetado principalmente para decodificadores de vídeo. Ele deriva de **CTransformFilter**, mas inclui a funcionalidade para descartar quadros se o renderizador downstream estiver para trás.
-   [**CBaseFilter**](cbasefilter.md) é uma classe de filtro genérica. Todas as outras classes nessa lista derivam de **CBaseFilter**. Se nenhuma delas for adequada, você poderá fazer fallback nessa classe. No entanto, essa classe também requer a maioria dos trabalhos de sua parte.
-   \[! Fundamental\]  
    > As transformações de vídeo in-loco podem ter um impacto sério no desempenho da renderização. As transformações in-loco exigem operações de leitura/modificação/gravação no buffer. Se a memória residir em uma placa gráfica, as operações de leitura serão significativamente mais lentas. Além disso, até mesmo uma transformação de cópia poderá causar operações de leitura não intencionais se você não a implementar com cuidado. Portanto, você deve sempre fazer testes de desempenho se escrever uma transformação de vídeo.

     

Para o codificador RLE de exemplo, a melhor opção é **CTransformFilter** ou **CVideoTransformFilter**. Na verdade, as diferenças entre eles são amplamente internas, portanto, é fácil converter de um para o outro. Como os tipos de mídia devem ser diferentes nos dois Pins, a classe **CTransInPlaceFilter** não é apropriada para esse filtro. Este exemplo usará **CTransformFilter**.

Em seguida: [etapa 2. Declare a classe de filtro](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



