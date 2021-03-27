---
title: Controle de fluxo
description: A maioria dos hardwares foi projetada para executar o código do sombreador linha por linha, executando cada instrução HLSL uma vez.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292003"
---
# <a name="flow-control"></a>Controle de fluxo

A maioria dos hardwares foi projetada para executar o código do sombreador linha por linha, executando cada instrução HLSL uma vez. Uma instrução de controle de fluxo determina em tempo de execução qual bloco de instruções HLSL executar em seguida. Usando uma instrução Flow-Control, um sombreador pode executar um loop por meio de um conjunto de instruções ou saltar (Branch) para uma instrução diferente daquela na próxima linha. Algumas instruções de controle de fluxo dão suporte ao controle estático que é especificado no momento da compilação; outros oferecem controle predicado, que é uma decisão por componente feita no tempo de execução, e ainda outros dão suporte a controle dinâmico, que é uma decisão feita em tempo de execução com base no conteúdo de uma variável.

O HLSL dá suporte às seguintes instruções de controle de fluxo.

-   [break](dx-graphics-hlsl-break.md)
-   [continua](dx-graphics-hlsl-continue.md)
-   [carte](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [mesmo](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de linguagem (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




