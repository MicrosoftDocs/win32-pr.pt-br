---
title: Controle de fluxo
description: A maioria dos hardwares foi projetada para executar o código de sombreador linha por linha, executando cada instrução HLSL uma vez.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aebaf63613aeb3a1d14607971db16602745883ab6b7b9db4723dfa2367f9bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120280"
---
# <a name="flow-control"></a>Controle de fluxo

A maioria dos hardwares foi projetada para executar o código de sombreador linha por linha, executando cada instrução HLSL uma vez. Uma instrução flow-control determina em tempo de execução qual bloco de instruções HLSL executar em seguida. Usando uma instrução de controle de fluxo, um sombreador pode fazer um loop por meio de um conjunto de instruções ou pular (branch) para uma instrução diferente da da próxima linha. Algumas instruções de controle de fluxo são suportadas pelo controle estático especificado em tempo de compilação; outros oferecem controle predicado, que é uma decisão por componente tomada em runtime e ainda outras oferecem suporte ao controle dinâmico, que é uma decisão tomada em tempo de execução com base no conteúdo de uma variável.

O HLSL dá suporte às seguintes instruções de controle de fluxo.

-   [break](dx-graphics-hlsl-break.md)
-   [Continuar](dx-graphics-hlsl-continue.md)
-   [Descartar](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [Enquanto](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de linguagem (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




