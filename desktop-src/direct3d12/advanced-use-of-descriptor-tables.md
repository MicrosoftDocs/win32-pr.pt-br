---
title: Uso avançado de tabelas de descritores
description: As seções a seguir fornecem informações sobre o uso avançado de tabelas de descritores.
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 044c02b87591f7ad53212ce37d7549ade68308a648092a260a67c97395959c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632586"
---
# <a name="advanced-use-of-descriptor-tables"></a>Uso avançado de tabelas de descritores

As seções a seguir fornecem informações sobre o uso avançado de tabelas de descritores.

-   [Alterando as entradas da tabela de descritores entre chamadas de renderização](#changing-descriptor-table-entries-between-rendering-calls)
-   [Indexação fora de limites](#out-of-bounds-indexing)
-   [Derivações de sombreador e indexação divergente](#shader-derivatives-and-divergent-indexing)
-   [Tópicos relacionados](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a>Alterando as entradas da tabela de descritores entre chamadas de renderização

Depois que as listas de comandos que definem tabelas de descritores foram enviadas para uma fila para execução, o aplicativo não deve editar da CPU as partes dos heaps de descritores que a GPU pode referenciar até que o aplicativo saiba que a GPU terminou de usar as referências.

A conclusão do trabalho pode ser determinada em um limite rígido usando limites de API para acompanhar o progresso da GPU, ou mecanismos mais grossos como aguardar para ver que a renderização foi enviada para exibição, o que for adequado para o aplicativo. Se um aplicativo sabe que apenas um subconjunto da região que uma tabela de descritores apontará será acessado (digamos devido ao controle de fluxo no sombreador), os outros descritores não referenciados ainda estão livres para serem alterados. Se um aplicativo precisar alternar entre diferentes tabelas de descritores entre chamadas de renderização, há algumas abordagens entre as quais o aplicativo pode escolher:

-   Controle de versão de tabela de descritor: crie (ou reutilize) uma tabela de descritor separada para cada coleção exclusiva de descripdores que deve ser referenciada por uma lista de comandos. Ao editar e reutilizar áreas previamente populadas em heaps de descritor, os aplicativos devem primeiro garantir que a GPU tenha terminado de usar qualquer parte de um heap de descritor que será reciclado.
-   Indexação dinâmica: os aplicativos podem organizar objetos que variam de acordo com o empate/expedição (ou até mesmo variam em um empate) em um intervalo de heap de descritores, definem uma tabela de descritores que abrange todos eles e, do sombreador, usam a indexação dinâmica da tabela durante a execução do sombreador para selecionar qual objeto usar.
-   Colocando descritores na assinatura raiz diretamente. Apenas um número muito pequeno de descritores pode ser gerenciado dessa forma porque o espaço de assinatura raiz é limitado.

A implicação de usar o controle de versão de tabela de descritor é que a memória do descritor fora de um heap de descritor deve ser gravada para cada conjunto exclusivo de descripdores referenciados pelo pipeline de gráficos para cada lista de comandos que pode estar em execução, na fila para execução ou ser gravada em um determinado momento.

D3D12 deixa a responsabilidade de gerenciar o controle de versão para o aplicativo para os tipos de objeto gerenciados por meio de heaps de descritor e tabelas de descritores. Um dos benefícios disso é que os aplicativos podem optar por reutilizar o conteúdo da tabela do descritor o máximo possível, em vez de sempre definir uma nova versão da tabela de descritores para cada envio da lista de comandos. A assinatura raiz é um espaço que o driver D3D12 automaticamente versões.

A capacidade de associar várias tabelas de descritores à assinatura raiz (e, assim, ao pipeline) de cada vez permite que os aplicativos agrupem e alternem conjuntos de referências de descritores em frequências diferentes, se desejado. Por exemplo, um aplicativo pode usar um pequeno número (talvez apenas um) de grandes tabelas de descritores estáticos que raramente mudam ou em quais regiões na memória heap do descritor subjacente estão sendo populadas conforme necessário, com o uso de indexação dinâmica do sombreador para selecionar texturas. Ao mesmo tempo, o aplicativo pode manter outra classe de recursos em que o conjunto referenciado por cada chamada de desenho é alternado da CPU usando a técnica de controle de versão da tabela de descritores.

## <a name="out-of-bounds-indexing"></a>Indexação fora de limites

A indexação fora dos limites de qualquer tabela de descritores do sombreador resulta em um acesso de memória amplamente indefinido, incluindo a possibilidade de ler memória arbitrária em processo como se fosse um descritor de estado de hardware e viver com a conseqüência do que o hardware faz com ele. Isso pode produzir uma redefinição de dispositivo, mas não falhará Windows.

## <a name="shader-derivatives-and-divergent-indexing"></a>Derivações de sombreador e indexação divergente

Se invocações de sombreador de pixel que estão sendo executadas em um carimbo 2x2 (para dar suporte a cálculos derivados), escolha índices de textura diferentes para amostrar de uma tabela de descritor e, se a configuração de amostra e a textura selecionadas para qualquer pixel especificado exigir um cálculo de LOD de derivações de coordenadas de textura, o processo de amostragem de LOD e de textura será feito pelo hardware  o que afetará o desempenho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabelas de descritores](descriptor-tables.md)
</dt> </dl>

 

 




