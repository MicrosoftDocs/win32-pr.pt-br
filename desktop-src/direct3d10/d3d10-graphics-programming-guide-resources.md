---
description: Um recurso é uma área na memória que pode ser acessada pelo pipeline de Direct3D.
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: Recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bb064bc771e36335527d68891bc76a1ce4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457092"
---
# <a name="resources-direct3d-10"></a>Recursos (Direct3D 10)

Um recurso é uma área na memória que pode ser acessada pelo pipeline de Direct3D. Para que o pipeline acesse a memória com eficiência, os dados fornecidos ao pipeline (como a geometria de entrada, os recursos do sombreador, as texturas etc.) devem ser armazenados em um recurso. Existem dois tipos de recursos dos quais todos os recursos de Direct3D são derivados: um buffer ou uma textura. Até 128 recursos podem estar ativos para cada estágio do pipeline.

Cada app normalmente criará muitos recursos. Exemplos de recursos incluem: buffers de vértice, buffer de índice, buffer constante, texturas e recursos de sombreador. Existem várias opções que determinam como os recursos podem ser usados. Você pode criar recursos com tipo forte ou sem tipo; você pode controlar se os recursos têm tanto acesso de leitura quanto de gravação; você pode disponibilizar recursos somente para CPU, GPU ou ambas. Naturalmente, haverá compensação entre velocidade versus funcionalidade: quanto maior a funcionalidade que você permitir a um recurso, o menor será o desempenho esperado.

Como um aplicativo geralmente usa muitas texturas, o Direct3D também apresenta o conceito de uma matriz de textura para simplificar o gerenciamento de textura. Uma matriz de textura contém uma ou mais texturas (todas do mesmo tipo e dimensões) que podem ser indexadas de dentro de um app ou por meio de sombreadores. Matrizes de textura permitem que você use uma única interface com vários índices para acessar muitas texturas. Você pode criar quantas matrizes de textura precisar para gerenciar tipos diferentes de textura.

Depois de criar os recursos que seu app usará, conecte ou associe cada recurso aos estágios de pipeline que farão uso deles. Isso é feito chamando uma API de vinculação, que leva um ponteiro para o recurso. Como mais de um estágio de pipeline pode precisar de acesso ao mesmo recurso, o Direct3D 10 apresenta o conceito de uma exibição de recurso. Um modo de exibição identifica a parte de um recurso que pode ser acessada. Você pode criar m modos de exibição, ou um recurso, e associá-los a n estágios, pressupondo que você siga as regras de associação para recurso compartilhado (o tempo de execução irá gerar erros no momento da compilação se você não fizer isso).

Um modo de exibição de recurso fornece um modelo geral para acesso a um recurso (texturas, buffers, etc.). Como você pode usar um modo de exibição para informar o tempo de execução sobre quais dados acessar e como acessá-los, exibições de recursos permitem criar recursos sem tipo. Ou seja, você pode criar recursos para um determinado tamanho no momento da compilação e, em seguida, declarar o tipo de dados dentro do recurso quando o recurso for vinculado ao pipeline. As exibições expõem muitos recursos novos para usar recursos, como a capacidade de ler as superfícies de profundidade/estêncil no sombreador, gerar cubemaps dinâmicos em uma única passagem e renderizar simultaneamente para várias fatias de um volume.

Para saber mais sobre os tipos de recursos básicos, as matrizes de textura e como criar e usar recursos, consulte estes outros tópicos:

-   [Tipos de recursos](d3d10-graphics-programming-guide-resources-types.md)
-   [Escolhendo um recurso](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [Criando recursos de buffer](d3d10-graphics-programming-guide-resources-creating.md)
-   [Criando recursos de textura](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [Copiando e acessando dados de recursos](d3d10-graphics-programming-guide-resources-mapping.md)
-   [Estrutura de memória e exibições](d3d10-graphics-programming-guide-resources-access-views.md)
-   [Compactação de bloco](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [Tabela de limites de recursos](d3d10-graphics-programming-guide-resources-limits.md)
-   [Sistemas de coordenadas](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [Regras de ponto flutuante](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [Regras de conversão de tipo de dados](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [Mapeando formatos herdados](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



