---
title: Funções (referência HLSL)
description: As funções encapsulam instruções HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37086a030ad902f2bfb5deab52ffba620e97890bd13e7c6957170572087ce7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514574"
---
# <a name="functions-hlsl-reference"></a>Funções (referência HLSL)

As funções encapsulam instruções HLSL. Isso permite que você depure um conjunto de funções e as reutilize entre sombreadores ou efeitos. Talvez você queira criar uma função que encapsula a funcionalidade de um sombreador de vértice, sombreador de pixel ou sombreador de textura. Outras vezes, talvez você queira escrever uma função auxiliar que executa alguma tarefa comumente usada e, em seguida, chamar essa função auxiliar de sua função de sombreador. As regras para escrever funções de sombreador para HLSL são muito semelhantes à escrita de funções C.

-   [Sintaxe](dx-graphics-hlsl-function-syntax.md)
-   [Parâmetros](dx-graphics-hlsl-function-parameters.md)
-   [Instrução Return](dx-graphics-hlsl-return.md)
-   [Assinaturas](dx-graphics-hlsl-signatures.md)

O HLSL também tem várias funções intrínsecas [**(DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md). Como todas as funções intrínsecas são testadas e otimizadas para desempenho, é uma boa prática usar uma função intrínseca sempre que possível, em vez de criar sua própria função.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de linguagem (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




