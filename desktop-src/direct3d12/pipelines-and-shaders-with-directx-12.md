---
title: Pipelines e sombreadores com o Direct3D 12
description: O pipeline programável do Direct3D 12 aumenta significativamente o desempenho de renderização em comparação com as interfaces de programação de gráficos de geração anteriores.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548239"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>Pipelines e sombreadores com o Direct3D 12

O pipeline programável do Direct3D 12 aumenta significativamente o desempenho de renderização em comparação com as interfaces de programação de gráficos de geração anteriores.

-   [Pipeline de gráficos do Direct3D 12](#direct3d-12-graphics-pipeline)
-   [Objetos de estado do pipeline](#pipeline-state-objects)
-   [Pipeline de computação do Direct3D 12](#direct3d-12-compute-pipeline)
-   [Tópicos relacionados](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Pipeline de gráficos do Direct3D 12

O diagrama a seguir ilustra o pipeline de gráficos do Direct3D 12 e o estado.

![diagrama que ilustra o pipeline e o estado do Direct3D 12](images/pipeline.png)

Um pipeline de gráficos é o fluxo sequencial de entradas de dados e saídas à medida que a GPU renderiza quadros. Considerando o estado do pipeline e as entradas, a GPU executa uma série de operações para criar as imagens resultantes. Um pipeline de gráficos contém sombreadores, que executam efeitos de renderização programáveis e cálculos e operações de função fixas.

Observe o seguinte ao fazer referência ao diagrama de estado do pipeline:

-   As tabelas de descritores e os heaps podem ser organizados arbitrariamente: SRVs, CBVs e UAVs podem ser referenciados e alocados em qualquer ordem.
-   Algumas operações do pipeline são configuráveis. Por exemplo, a mesclagem de saída normalmente opera em uma base de leitura-modificação-gravação com as exibições de destino de renderização e estêncil de profundidade. No entanto, o pipeline pode ser configurado para que qualquer uma dessas exibições seja somente leitura ou somente gravação.
-   Os exemplos estáticos não fazem parte dos argumentos raiz, pois são estáticos.

## <a name="pipeline-state-objects"></a>Objetos de estado do pipeline

O Direct3D 12 apresenta o PSO (objeto de estado de pipeline). Em vez de armazenar e representar o estado do pipeline em um grande número de objetos de alto nível, os Estados dos componentes de pipeline, como o Assembler de entrada, rasterizador, sombreador de pixel e a fusão de saída, são armazenados em um PSO. Um PSO é um objeto de estado de pipeline unificado que é imutável após a criação. O PSO selecionado no momento pode ser alterado de forma rápida e dinâmica, e o hardware e os drivers podem converter diretamente um PSO em instruções de hardware nativo e estado, preparando a GPU para o processamento de gráficos. Para aplicar um PSO, o hardware copia uma quantidade mínima de Estado previamente computado diretamente nos registros de hardware. Isso remove a sobrecarga causada pelo driver de gráficos recomputando continuamente o estado do hardware com base em todas as configurações de pipeline e renderização aplicáveis no momento. O resultado é significativamente reduzido de forma significativa a sobrecarga de chamada, melhor desempenho e mais chamadas de desenho por quadro.

O PSO aplicado atualmente define e conecta todos os sombreadores que estão sendo usados no pipeline de renderização. A [HLSL (linguagem de sombreamento de alto nível) da Microsoft](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) é pré-compilado em objetos de sombreador, que são usados em tempo de execução como entrada para objetos de estado do pipeline. Para obter mais informações sobre como as funções PSO no pipeline de gráficos, consulte [Gerenciando o estado do pipeline de gráficos no Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="direct3d-12-compute-pipeline"></a>Pipeline de computação do Direct3D 12

O diagrama a seguir ilustra o pipeline de computação do Direct3D 12 e o estado.

![Diagrama que mostra o pipeline de computação do Direct3D 12.](images/compute-pipeline.png)

Não há unidades de função fixas nesse pipeline, no entanto, heaps de descritores, heaps de amostra e amostras estáticas ainda estão disponíveis em computação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 