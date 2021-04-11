---
description: O pipeline de gráficos do Direct3D 10 representa uma mudança fundamental na arquitetura, recriada a partir do início em hardware e software para capacitar a próxima geração de jogos e de aplicativos multimídia 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Recursos de API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163963"
---
# <a name="api-features-direct3d-10"></a>Recursos de API (Direct3D 10)

O pipeline de gráficos do Direct3D 10 representa uma mudança fundamental na arquitetura, recriada a partir do início em hardware e software para capacitar a próxima geração de jogos e de aplicativos multimídia 3D. Ele usa o WDDM (modelo de driver de vídeo) do Windows, que permite aprimoramentos de desempenho e comportamento, como a memória da GPU virtual.

Os desenvolvedores familiarizados com o Direct3D 9 descobrirão uma série de aprimoramentos funcionais e melhorias de desempenho no Direct3D 10, incluindo:

-   A capacidade de processar primitivos inteiros no novo [estágio Geometry-Shader](/previous-versions//bb205146(v=vs.85)).
-   A capacidade de produzir dados de vértice gerados por pipeline para a memória usando o [estágio Stream-output](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).
-   Organização do estado do pipeline em 5 [objetos de estado](d3d10-graphics-programming-guide-api-features-state-objects.md)imutáveis, permitindo a configuração rápida do pipeline.
-   Organização de constantes de sombreador em [buffers constantes](d3d10-graphics-programming-guide-resources-types.md), minimizando a sobrecarga de largura de banda para fornecer dados de sombreador-constante.
-   A capacidade de executar a troca de material por primitivo e a configuração usando um sombreador de geometria.
-   Novos [tipos de recursos](d3d10-graphics-programming-guide-resources-types.md) (incluindo matrizes de textura que podem ser indexados de sombreadores) e formatos de recurso.
-   Maior generalização de acesso a recursos usando uma [exibição](d3d10-graphics-programming-guide-resources-access-views.md).
-   Os bits de capacidade de hardware herdados (CAPS) foram removidos em favor de um conjunto avançado de funcionalidade garantida, que tem como alvo o hardware de classe Direct3D 10 (mínimo).
-   [Tempo de execução em camadas](d3d10-graphics-programming-guide-api-features-layers.md) – a API do Direct3D 10 é construída com camadas, começando com a funcionalidade básica no núcleo e compilando a funcionalidade opcional e auxiliar de desenvolvedor (Debug, etc.) em camadas externas.
-   Integração total do HLSL-todos os sombreadores do Direct3D 10 são escritos em HLSL e implementados com o [núcleo do sombreador comum](../direct3dhlsl/dx-graphics-hlsl-common-core.md).
-   Um aumento no número de destinos de renderização, texturas e amostras. Também não há nenhum limite de comprimento de sombreador.
-   Operações de sombreador de inteiros e de bits.
-   Readback de uma superfície de profundidade/estêncil ou um recurso de uma amostra, uma vez que ele não está mais associado como um destino de renderização.
-   Suporte de Alpha-to-Coverage com uma amostra.

Há diferenças de comportamento adicionais que os desenvolvedores do Direct3D 9 também devem conhecer (consulte [considerações do Direct3D 9 para o Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).

Aqui está uma lista de recursos do Direct3D 9 que não têm mais suporte ou que foram revisados no Direct3D 10 (consulte [recursos preteridos](d3d10-graphics-programming-guide-api-features-deprecated.md)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
