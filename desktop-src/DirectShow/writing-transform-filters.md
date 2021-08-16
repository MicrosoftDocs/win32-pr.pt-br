---
description: Gravando filtros de transformação
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Gravando filtros de transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe8329809b6fe93ea33a9842f57733d7539a56e2ac21abfcf304d2ed780e6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816833"
---
# <a name="writing-transform-filters"></a>Gravando filtros de transformação

Esta seção descreve como escrever um filtro de transformação, definido como um filtro que tem exatamente um PIN de entrada e um pino de saída. Para ilustrar as etapas, esta seção descreve um filtro de transformação hipotético que gera vídeo de RLE (codificação de tamanho de execução). Ele não descreve o próprio algoritmo de codificação RLE, somente as tarefas específicas para DirectShow. (DirectShow já fornece um codec RLE por meio do filtro de [compressor AVI](avi-compressor-filter.md) .)

esta seção pressupõe que você usará o DirectShow biblioteca de classes base para criar filtros. Embora você possa escrever um filtro sem ele, a biblioteca de classes base é altamente recomendável.

> [!Note]  
> antes de gravar um filtro de transformação, considere se um objeto de mídia DirectX (DMO) atenderia às suas necessidades. O DMOs pode fazer muitas das mesmas coisas que os filtros, e o modelo de programação para DMOs é mais simples. os DMOs são hospedados em DirectShow por meio do filtro de [invólucro de DMO](dmo-wrapper-filter.md) , mas também podem ser usados fora do DirectShow. DMOs agora é a solução recomendada para codificadores e decodificadores.

 

Esta seção inclui os tópicos a seguir:

-   [Etapa 1. Escolher uma classe base](step-1--choose-a-base-class.md)
-   [Etapa 2. Declarar a classe de filtro](step-2--declare-the-filter-class.md)
-   [Etapa 3. Suporte à negociação de tipo de mídia](step-3--support-media-type-negotiation.md)
-   [Etapa 4. Definir propriedades de alocador](step-4--set-allocator-properties.md)
-   [Etapa 5. Transformar a imagem](step-5--transform-the-image.md)
-   [Etapa 6. Adicionar suporte para COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[criando filtros de DirectShow](building-directshow-filters.md)
</dt> <dt>

[DirectShow Classes base](directshow-base-classes.md)
</dt> <dt>

[gravando filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



