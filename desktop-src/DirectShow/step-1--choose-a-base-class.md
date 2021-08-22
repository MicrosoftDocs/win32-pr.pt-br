---
description: Escolha uma classe base como parte da escrita de um filtro de transformação. Saiba quais classes são apropriadas para filtros de transformação.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Etapa 1. Escolher uma classe base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140beba3df02ace21d99779c152a79632fe0b4a1a916c4412c467b0f4ac5627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315876"
---
# <a name="step-1-choose-a-base-class"></a>Etapa 1. Escolher uma classe base

Esta é a etapa 1 do tutorial Escrevendo [filtros de transformação.](writing-transform-filters.md)

Supondo que você decida escrever um filtro e não um DMO, a primeira etapa é escolher qual classe base usar. As classes a seguir são apropriadas para filtros de transformação:

-   [**O CTransformFilter**](ctransformfilter.md) foi projetado para transformar filtros que usam buffers de entrada e saída separados. Às vezes, esse tipo de filtro é chamado de filtro de transformação de cópia. Quando um filtro de transformação de cópia recebe um exemplo de entrada, ele grava novos dados em um exemplo de saída e entrega o exemplo de saída para o próximo filtro.
-   [**O CTransInPlaceFilter**](ctransinplacefilter.md) foi projetado para filtros que modificam dados no buffer original, também chamados de filtros trans-in-place. Quando um filtro trans-in-locar recebe um exemplo, ele altera os dados dentro desse exemplo e entrega o mesmo downstream de exemplo. O pino de entrada e o pino de saída do filtro sempre se conectam com tipos de mídia correspondentes.
-   [**CVideoTransformFilter**](cvideotransformfilter.md) foi projetado principalmente para decodificadores de vídeo. Ele deriva de **CTransformFilter,** mas inclui a funcionalidade para soltar quadros se o renderador downstream ficar para trás.
-   [**CBaseFilter é**](cbasefilter.md) uma classe de filtro genérica. As outras classes nesta lista derivam de **CBaseFilter.** Se nenhum deles for adequado, você poderá fazer fall back nessa classe. No entanto, essa classe também requer mais trabalho de sua parte.
-   \[! Importante\]  
    > As transformaçãos de vídeo in-locar podem ter um impacto grave no desempenho da renderização. As transformação in-loquete exigem operações de leitura-modificação/gravação no buffer. Se a memória residir em uma placa gráfica, as operações de leitura serão significativamente mais lentas. Além disso, até mesmo uma transformação de cópia poderá causar operações de leitura não intencionais se você não implementá-la com cuidado. Portanto, você sempre deverá fazer testes de desempenho se escrever uma transformação de vídeo.

     

Para o codificador RLE de exemplo, a melhor opção é **CTransformFilter** ou **CVideoTransformFilter.** Na verdade, as diferenças entre eles são amplamente internas, portanto, é fácil converter de uma para outra. Como os tipos de mídia devem ser diferentes nos dois pinos, a **classe CTransInPlaceFilter** não é apropriada para esse filtro. Este exemplo usará **CTransformFilter**.

Próximo: [Etapa 2. Declare a classe Filter](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



