---
description: Gravando filtros de transformação
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Gravando filtros de transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921918"
---
# <a name="writing-transform-filters"></a>Gravando filtros de transformação

Esta seção descreve como escrever um filtro de transformação, definido como um filtro que tem exatamente um PIN de entrada e um pino de saída. Para ilustrar as etapas, esta seção descreve um filtro de transformação hipotético que gera vídeo de RLE (codificação de tamanho de execução). Ele não descreve o próprio algoritmo de codificação RLE, somente as tarefas específicas do DirectShow. (O DirectShow já fornece um codec RLE por meio do filtro de [compressor AVI](avi-compressor-filter.md) .)

Esta seção pressupõe que você usará a biblioteca de classes base do DirectShow para criar filtros. Embora você possa escrever um filtro sem ele, a biblioteca de classes base é altamente recomendável.

> [!Note]  
> Antes de escrever um filtro de transformação, considere se um DMO (objeto de mídia do DirectX) atenderia às suas necessidades. O DMOs pode fazer muitas das mesmas coisas que os filtros, e o modelo de programação para DMOs é mais simples. Os DMOs são hospedados no DirectShow por meio do filtro de [invólucro do DMO](dmo-wrapper-filter.md) , mas também podem ser usados fora do DirectShow. DMOs agora é a solução recomendada para codificadores e decodificadores.

 

Esta seção inclui os tópicos a seguir:

-   [Etapa 1. Escolher uma classe base](step-1--choose-a-base-class.md)
-   [Etapa 2. Declarar a classe de filtro](step-2--declare-the-filter-class.md)
-   [Etapa 3. Suporte à negociação de tipo de mídia](step-3--support-media-type-negotiation.md)
-   [Etapa 4. Definir propriedades de alocador](step-4--set-allocator-properties.md)
-   [Etapa 5. Transformar a imagem](step-5--transform-the-image.md)
-   [Etapa 6. Adicionar suporte para COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando filtros do DirectShow](building-directshow-filters.md)
</dt> <dt>

[Classes base do DirectShow](directshow-base-classes.md)
</dt> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



